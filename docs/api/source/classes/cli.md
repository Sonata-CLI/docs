# <code><a href="../../namespaces/sonata">sonata</a>::<a href="../../namespaces/cli">cli</a>::CLI</code> (Class)
A barebones class representing the CLI command, `sn`.

!!! warning

    This class and/or its properties were meant to be used
    only once, while defining the `sn` command.
    
    It is **not recommended** to create a new CLI object if
    there already is one, which might lead to conflict.

## Definition

```cpp
class CLI {
public:
    int run(int argc, char** argv);
};
```

## Methods

### `int run(int argc, char** argv)`
Runs the command, which loops through all the registered sub-commands
and executes the entry function for that subcommand.

Prints the root help message if no subcommand or argument is supplied.