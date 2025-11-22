# How to Convert String To Char Array in C#

## Description
Converting a string into a char[] is useful when you need to inspect or manipulate individual characters.
C# provides a built-in method, ToCharArray(), which returns an array containing each character from the string in order.

This is commonly used in algorithms, text parsing, encoding conversions, and validation logic.

## Sample Code
```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        string text = "hello world";

        // Convert the string to a character array
        char[] characters = text.ToCharArray();

        // Print characters separated by commas
        Console.WriteLine(string.Join(",", characters));
    }
}

```

## Output
```
h,e,l,l,o, ,w,o,r,l,d

```

## Best Practices
1. Use ToCharArray() when you need an independent, modifiable copy of the characters.
2. For performance-critical scenarios (large strings), consider ReadOnlySpan<char> to avoid extra allocations.
3. When only reading characters, prefer iterating directly over the string instead of creating an array.
