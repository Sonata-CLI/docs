# <code><a href="../sonata">sonata</a>::luau</code> (namespace)
The namespace for the Sonata Luau API.

## Overview

The `sonata::luau` namespace provides functionality for Luau-related tasks, such as:
- Creating, managing and running a Luau VM
- Parsing, creating and serializing Luau tables
- Module and multi-file importing
- Managing a global Luau environment
- Compiling Luau files

## Classes & Structs
| Class | Description |
|---|---|
| [`Bytecode`](../classes/luau_bytecode.md) | Represents the execution-ready data gotten from compiling Luau. |
| [`Environment`](../classes/luau_environment.md) | For storing and loading globals such as `require()`. |
| [`Compiler`](../classes/luau_compiler.md) | For turning Luau source code into execution-ready [`Bytecode`](../classes/luau_bytecode.md). |
| [`VM`](../classes/luau_vm.md) | Allows easier management and executing of Lua states. |
| [`DataFile`](../classes/luau_datafile.md) | Used for parsing or creating static Luau tables. |
| [`DataFileError`](../classes/luau_datafileerror.md) | Inherited from std::runtime_error, represents an error from a [`DataFile`](../classes/luau_datafile.md) operation. |
| [`DataValue`](../classes/luau_datavalue.md) | A very flexible class that represents a value inside of a [`DataFile`](../classes/luau_datafile.md). |
| [`ModuleError`](../classes/luau_moduleerror.md) | Inherited from std::runtime_error, represents an error raised by the module system. |
| [`ModuleSource`](../classes/luau_modulesource.md) | Abstract interface for retrieving module bytecode. |
| [`FileSystemSource`](../classes/luau_filesystemsource.md) | Implements [`ModuleSource`](../classes/luau_modulesource.md) to read and compile `.luau` files directly from disk. |
| [`MemorySource`](../classes/luau_memorysource.md) | Implements [`ModuleSource`](../classes/luau_modulesource.md) to hold and load precompiled bytecode in memory. |
| [`ModuleLoader`](../classes/luau_moduleloader.md) | Implements path resolution, path aliasing, and `require()` functionality for a [`VM`](../classes/luau_vm.md). |