# How to Convert Char Array To String in C#

## Description
This guide explains how to convert char array to string in C# with simple examples.

## Sample Code
```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        char[] letters = new char[] { 'H', 'e', 'l', 'l', 'o' };

        // Convert char[] to string using constructor
        string result = new string(letters);

        Console.WriteLine(result);
    }
}
```

## Output
```
Hello
```

## Best Practices
1. Use the new string(char[]) constructor — it is fast, simple, and idiomatic.
2. If you are converting only part of a char array, use the new string(char[], int start, int length) overload.
3. Avoid manually concatenating characters in a loop — it is slower and allocates multiple intermediate strings.
