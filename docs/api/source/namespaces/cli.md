# <code><a href="../sonata">sonata</a>::cli</code> (namespace)

The <code><a href="../sonata">sonata</a>::cli</code> namespace contains classes for interacting with the `sn` command.

## Classes & Structs

| Class | Description |
|---|---|
| [`CLI`](../classes/cli.md) | Represents a new CLI command e.g. `sn`. |
| [`Command`](../classes/cli_command.md) | Represents a command e.g. `init` or `build`. |
| [`Argument`](../classes/cli_argument.md) | Represents an argument for a [Command](../classes/cli_command.md), like `--help`. |

!!! note "help_argument"

    When making a new command, do not manually declare the --help argument.
    Instead, pass `sonata::cli::help_argument` in the arguments of the command.
    
    ```cpp
    inline const Argument help_argument{
        .name = "--help",
        .aliases = {"-h"},
        .description = "Shows help information about the command or subcommand"
    };
    ```