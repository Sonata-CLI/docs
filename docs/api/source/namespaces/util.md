# <code><a href="../sonata">sonata</a>::util</code> (namespace)

The <code><a href="../sonata">sonata</a>::util</code> namespace contains generic utility functions.

## Functions

### `parse_path_arg`

```cpp
std::optional<fs::path> parse_path_arg(
    const std::string& arg,
    bool& pathspecified
);
```

Parses a single positional path argument.

If `arg` contains a path, the path is returned as an `std::optional<fs::path>`.
If no path was supplied, `std::nullopt` is returned.

The function does not throw exceptions.

#### Parameters

- `arg` (`std::filesystem::path` or `std::nullopt`) — The positional argument to parse.
- `pathspecified` — Set to indicate whether a path was specified.

#### Returns

An `std::optional<fs::path>` containing the parsed path, or `std::nullopt`
if no path was supplied.

---

### <code>validate_directory_path</code>

```cpp
bool validate_directory_path(
    const fs::path& path,
    std::string& error
);
```

Checks whether a path can safely be treated as a directory path.

Every existing component of the path is checked. If any existing component
is a regular file, the path is considered invalid.

Non-existent path components are allowed, so the function can be used to
validate paths for directories that have not yet been created.

#### Parameters

- `path` (`std::filesystem::path`) — The path to validate.
- `error` — A string that is populated with an error description when the
  path is invalid.

#### Returns

`true` if the path can safely be treated as a directory path, or `false`
if an existing component of the path is a regular file.