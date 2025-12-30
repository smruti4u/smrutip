<div style="float: right; width: 260px; padding: 15px; border-left: 1px solid #ccc; background: #f9f9f9;">
<h3 style='margin-top:0;'>Related Topics</h3>
- [Create Array](./create-array.md)
- [Sort Array](./sort-array.md)
- [Reverse Array](./reverse-array.md)
- [Find In Array](./find-in-array.md)
- [Resize Array](./resize-array.md)

</div>

# How to Convert Array To List in C#

## Description
This guide explains how to convert array to list in C# with simple examples.

## Sample Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;

class Program
{
    static void Main()
    {
        // Sample array
        int[] arr = { 1, 2, 3, 4, 5 };

        // Convert array to List
        List<int> list = arr.ToList();

        // Display the List
        foreach (var item in list)
        {
            Console.WriteLine(item);
        }
    }
}

```

## Output
```
Converted List:
1
2
3
4
5

```

## Best Practices

1. **Keep Things Simple!**

   * When you don’t need to change the data type (like an array to a list), **only convert it when you need to**. If all you need is to go through the values or do basic operations, there’s no need to convert it.
   * Example: If you just want to print the items in the array, you can do that **directly** with `foreach`:

     ```csharp
     foreach (var item in arr)
     {
         Console.WriteLine(item);  // Prints each number in the array
     }
     ```

2. **Don’t Overuse `ToList()` If You Don’t Need It!**

   * If you’re just going to loop through the array, you don’t need to convert it into a `List`. Arrays are already iterable, so you can loop through them directly without converting them.
   * `ToList()` is useful when you need to use `List`-specific features like `Add()`, `Remove()`, or other list-specific methods, but for simple looping, the array works fine.

3. **Be Careful With Memory:**

   * **Avoid creating unnecessary copies**. If you don’t need to change the array into a `List` or need extra features from a `List`, don’t waste memory and time creating that extra list. For example:

     ```csharp
     // Don't convert if you don't need to modify the data
     List<int> list = arr.ToList();  // Only use this if you need to use list-specific methods
     ```

4. **Check for Null Before You Use the Array (Safety First!):**

   * Sometimes, the array might be empty or `null`, which can cause errors in your program. So, it’s a good idea to check that the array is **not null** before trying to work with it.
   * Example:

     ```csharp
     if (arr != null)
     {
         List<int> list = arr.ToList();  // This is safe now
         // Proceed with your work...
     }
     else
     {
         Console.WriteLine("Array is empty or not initialized.");
     }
     ```

5. **Arrays and Lists Are Different – Know When to Use Which!**

   * **Arrays** are a fixed size, meaning once you create them, you can’t change the number of elements. They are good for when you know the number of items in advance.
   * **Lists** are flexible. You can add and remove items as needed, which is great for situations where you’re not sure how many items you’ll need.
   * If you know the number of items and don’t need flexibility, **use an array**. If you need flexibility to change the list later, **use a List**.

6. **Naming Things Clearly:**

   * Give your arrays and lists clear names so you and others can easily understand what they hold. For example, `arr` is a short name, but it could be better if it was named `numbers` if it's an array of numbers.
   * Example:

     ```csharp
     int[] numbers = { 1, 2, 3, 4, 5 };
     ```

---

### **Summary:**

* **Use arrays** when you don’t need to add/remove items frequently.
* **Use lists** if you need flexibility, like adding or removing items.
* **Don’t convert to a list unless you really need to** (arrays can often do the job just fine).
* Always **check for null** before using an array or list to avoid errors.
* Keep your code simple and readable – **clear names** for arrays and lists go a long way!

---



## SEO Keywords
how to array to list in c#, array to list, c# how to, c# tutorial
