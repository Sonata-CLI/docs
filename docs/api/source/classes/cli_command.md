# <code><a href="../../namespaces/sonata">sonata</a>::<a href="../../namespaces/cli">cli</a>::Command</code> (Struct)

A struct that stores information about a command (inside a [CLI](cli.md) object, like `init` or `pkg`) which gets read by
the [CLI](cli.md) while running the command, or printing its help message.

## Definition

```cpp
struct Command {
    std::string name;
    std::string description;
    std::vector<Argument> args;
    std::vector<std::string> usage;
    std::vector<std::string> examples;
    std::function<int(int argc, char** argv)> execute;
    std::vector<Command> children;
};
```

### Members

## `std::string name`
The command's name/subcommand.

This string is what is supplied after `sn`, like `sn init`.

## `std::string description`
A brief explanation of what the command does.

Used while printing the command's help message.

## `std::vector<Argument> args`
nigga