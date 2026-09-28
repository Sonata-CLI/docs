# <code><a href="../sonata">sonata</a>::luau</code> (namespace)
The namespace for the Sonata Luau API.

!!! note

    This namespace currently only contains utility for parsing/generating project manifest files.

## Overview

The `sonata::luau` namespace provides functionality for representing Luau
values, parsing Sonata manifests, serializing values, and managing globals
available to manifests.

It provides type-safe runtime values, manifest parsing and serialization,
parse error reporting, and manifest environments.

## Classes

| Class | Description |
|---|---|
| [`Value`](../classes/value.md) | Represents a dynamically typed Luau value. |
| [`Environment`](../classes/environment.md) | Defines globals available while parsing manifests. |

## Structs

| Struct | Description |
|---|---|
| [`Global`](../classes/global.md) | Represents a reference to a manifest global. |
| [`ParseError`](../classes/parse-error.md) | Describes an error encountered while parsing a manifest. |
| [`ParseResult`](../classes/parse-result.md) | Contains the result of parsing a manifest, including either a value or an error. |

## Enums

| Enum | Description |
|---|---|
| [`ValueType`](../enums/value-type.md) | Describes the type of a [`Value`](../classes/value.md). |

## Type Aliases

| Alias | Description |
|---|---|
| `Array` | A sequence of [`Value`](../classes/value.md) objects. |
| `Table` | A string-keyed collection of [`Value`](../classes/value.md) objects. |

## Functions

| Function | Description |
|---|---|
| [`parseManifest()`](../functions/parse-manifest.md) | Parses a Sonata manifest without creating a VM or executing Luau code. |
| [`serializeManifest()`](../functions/serialize-manifest.md) | Serializes a [`Value`](../classes/value.md) into Sonata manifest source. |
| [`parse()`](../functions/parse.md) | Convenience function for parsing manifest source. |
| [`serialize()`](../functions/serialize.md) | Convenience function for serializing a [`Value`](../classes/value.md). |