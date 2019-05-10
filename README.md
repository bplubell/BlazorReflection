# Blazor trouble with reflection

Blazor (or more likely its underlying wasm runtime) is not emitting all the members of types. I have only specifically tested `System.Math`.

If you try accessing a missing member, such as PI, it is still correctly computed and returned.

# Results for System.Math

| Expected         | Actual      |
|:--               |:--          |
| Abs              | Abs         |
| Acos             |             |
| Acosh            |             |
| Asin             |             |
| Asinh            |             |
| Atan             |             |
| Atan2            |             |
| Atanh            |             |
| BigMul           |             |
| BitDecrement     |             |
| BitIncrement     |             |
| Cbrt             |             |
| Ceiling          |             |
| Clamp            | Clamp       |
| CopySign         |             |
| Cos              |             |
| Cosh             |             |
| DivRem           |             |
| E                |             |
| Equals           | Equals      |
| Exp              |             |
| Floor            |             |
| FusedMultiplyAdd |             |
| GetHashCode      | GetHashCode |
| GetType          | GetType     |
| IEEERemainder    |             |
| ILogB            |             |
| Log              |             |
| Log10            |             |
| Log2             |             |
| Max              | Max         |
| MaxMagnitude     |             |
| Min              | Min         |
| MinMagnitude     |             |
| PI               |             |
| Pow              | Pow         |
| Round            | Round       |
| ScaleB           |             |
| Sign             | Sign        |
| Sin              |             |
| Sinh             |             |
| Sqrt             | Sqrt        |
| Tan              |             |
| Tanh             |             |
| ToString         | ToString    |
| Truncate         |             |
