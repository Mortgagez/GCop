﻿# GCop 404

> *"Multiple `if` and `else if` on the same variable can be replaced with a 'switch'"*

## Rule description

Where multiple subsequent `if` conditions are checking the same variable against different values, prefer `switch` over `if`, because it is more readable and faster to run.

A `switch` has a semantic meaning. It's saying *"pick one of these based on this variables value"* (using a lookup table or a hash list for more than five items) but an `if` statement is just a series of boolean checks with no explicit semantic connection.

## Example

```csharp
if (foo == 0)
{
    ...
}
else if (foo == 1)
{
    ...
}
else if (foo == 2)
{
    ...
}
```

*should be* 🡻

```csharp
switch (foo)
{
    case 0:
       ...
       break;
    
    case 1:
       ...
       break;
    
    case 2:
       ...
       break;
    
    default: 
       throw new NotSupportedException("...");
}
```