# 🚀 Dynamic Array Class in C++ (OOP)

A robust, header-only generic implementation of a **Dynamic Array** built from scratch in **C++** using Object-Oriented Programming (OOP) principles and templates. This project mimics core functionalities of standard data structures like `std::vector`.

---

## ✨ Features

* **Generic/Template Support (`template <class T>`)**: Works with any data type (`int`, `string`, `float`, custom classes, etc.).
* **Dynamic Resizing**: Automatically handles memory allocation and resizing (`Resize`).
* **Comprehensive Operations**:
  * **Access & Modification**: `SetItem`, `GetItem`, `ItemAt`
  * **Insertion**: `InsertAt`, `InsertAtBeginning`, `InsertAtEnd`, `InsertAfter`, `InsertBefore`
  * **Deletion**: `DeleteItemAt`, `DeleteFirstItem`, `DeleteLastItem`, `DeleteItem`
  * **Utility**: `Find`, `Reverse`, `Clear`, `IsEmpty`, `Size`, `PrintList`

---

## 📂 Code Structure

* **Generic Support**: Built with templates (`template <class T>`) to work with any data type.
* **Bounds Checking**: Built-in validation for indices on all operations to prevent segmentation faults.
* **Clean API**: Intuitive methods for adding, removing, finding, and printing elements.

The project consists of a single template class `clsDynamicArray` encapsulated safely with proper memory management (destructors to prevent memory leaks).

---

## 🛠 Technical Details & Implementation

This implementation focuses on safety, efficiency, and fundamental C++ concepts:

### 1. Dynamic Memory Management
* **Constructor & Destructor**: Implements RAII (Resource Acquisition Is Initialization). The constructor allocates memory on the heap, while the destructor ensures no memory leaks by properly freeing memory when the object goes out of scope.
* **`Clear()` Method**: Safely deallocates memory and resets the array pointer to `nullptr`, preventing dangling pointers.

### 2. Resizing & Data Integrity
* **`Resize(size_t NewSize)`**: Efficiently handles memory reallocation. It creates a temporary array, copies the data up to the minimum of the old and new sizes, and seamlessly replaces the original array.

### 3. Advanced Insertion & Deletion
* **Insertion (`InsertAt`, `InsertAfter`, etc.)**: Handles boundary checks and shifts elements dynamically to accommodate new data without losing existing values.
* **Deletion (`DeleteItemAt`, `DeleteFirstItem`, etc.)**: Performs manual memory re-allocation to shrink the array size by one after removing an element, ensuring memory is optimized.

### 4. Utilities & Search
* **`Find(T Item)`**: A linear search algorithm returning the index of the first occurrence or `-1` if not found.
* **`Reverse()`**: Implements an in-place reversal algorithm using `std::swap`, optimizing performance by reducing the number of iterations to `_Size / 2`.

---

## 🌐 Platform

Programming Advices
https://programmingadvices.com

Instructor: Dr. Mohammed Abu-Hadhoud

## 👨‍💻 Author

Developed by Mohamed Ahmed to master C++ memory management and data structure implementation.
