---
title: "Stream Class"
description: "Stream is a feature introduced in Java 8 that provides a more efficient and concise way to process data collections in a declarative and functional manner"
pubDate: "Feb 07 2024"
heroImage: "/post_img.webp"
badge: "Most Recent"
tags: ["Java", "Stream"]
---

## Using Stream in Java

### Introduction

`Stream` is a feature introduced in Java 8 that provides a more efficient and concise way to process data collections in a declarative and functional manner. With `Stream`, you can perform filtering, mapping, sorting, and reduction operations on collections of elements without having to write explicit loops.

### Basic Example

Suppose we have a list of numbers and we want to filter only the even numbers and print them to the console. Here's how we would do it using `Stream`:

```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // Creating a list of numbers
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

        // Using Stream to filter even numbers
        numbers.stream()
               .filter(num -> num % 2 == 0) // Filter only even numbers
               .forEach(System.out::println); // Print each number to the console
    }
}
```

### Code Explanation

1. **Creating the List**: First, we create a list of numbers using `Arrays.asList()`. This list will contain numbers from 1 to 10.

2. **Obtaining the Stream**: We call the `stream()` method on the `numbers` list. This gives us a `Stream<Integer>` object representing a sequence of elements from the list.

3. **`filter()` Method**: After obtaining the stream, we call the `filter()` method to filter the even numbers. The `filter()` method takes a predicate (a lambda expression in this case) that specifies the filtering criterion. In this example, the predicate is `num -> num % 2 == 0`, which returns `true` if the number is even.

4. **`forEach()` Method**: Finally, we call the `forEach()` method to print each even number to the console. The `forEach()` method takes a consumer (in this case, a reference to the `System.out.println` method) that will be applied to each element of the stream.

### Common Stream Methods

After calling `.stream()` on a collection, you can chain a variety of methods to manipulate the stream elements. Some common methods include:

- **`filter(Predicate<T>)`**: Filters the stream elements based on the specified predicate.
- **`map(Function<T, R>)`**: Transforms each stream element by applying a function to it.
- **`sorted()`**: Sorts the stream elements according to their natural order.
- **`distinct()`**: Removes duplicate elements from the stream.
- **`limit(long)`**: Limits the size of the stream to a maximum number of elements.
- **`forEach(Consumer<T>)`**: Performs an operation for each element of the stream.
- **`collect(Collector<T, A, R>)`**: Collects the stream elements into a collection or aggregate value.

These are just some of the methods available in `Stream`. There are other methods you can explore based on your specific needs.

### Conclusion

Using `Stream` in Java simplifies data processing by providing a functional and declarative API. It allows you to write cleaner, more concise, and efficient code for manipulating collections of elements. As you become more familiar with `Stream`, you'll be able to perform more advanced and complex operations on your data in an easy and elegant way.
