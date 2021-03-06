﻿# GCop 203

> *"Use meaningful names instead of single character for foreach identifier"*

## Rule description

A single character variable name isn't descriptive enough. Sometimes it's acceptable, e.g. in a lambda expression or in a very short loop. But in most cases it's better to use a descriptive name to reveal its meaning, purpose and role in that context.

## Example

```csharp
foreach (var i in items)
{
    ... (many lines of code)
}
```

*should be* 🡻

```csharp
foreach (var item in items)
{
    ... (many lines of code)
}
```