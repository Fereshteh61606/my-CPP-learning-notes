# Map

Let's break down the concepts of `std::map` and atomic variables step by step.

### 1. `std::map`

#### What is a `std::map`?
- `std::map` is a part of the Standard Template Library (STL) in C++. It is an associative container that stores elements in key-value pairs. The keys are unique, and each key is associated with a value.

#### Characteristics of `std::map`:
- **Key-Value Pairs**: Each element in a map consists of a key and a value. The key is used to identify the element, and the value is the data associated with that key.
- **Ordered**: Elements are sorted based on the keys when they are inserted. The sorting is done according to the key's comparison function (by default, it uses the less-than operator).
- **Unique Keys**: Each key in a map must be unique; if a new element is inserted with a key that already exists, the old value will be replaced.
- **Dynamic Size**: Maps can grow and shrink in size as you insert or remove elements.

#### Common Operations:
- **Insertion**: You can insert elements using `insert()` or the subscript operator (`[]`).
  
  ```cpp
  std::map<std::string, int> myMap;
  myMap["A"] = 1; // Using subscript operator
  myMap.insert(std::make_pair("B", 2)); // Using insert
  ```

- **Access**: You can access the value associated with a key using the subscript operator or `at()`.

  ```cpp
  int aValue = myMap["A"]; // Access value for key "A"
  ```

- **Iteration**: You can iterate over the elements using a range-based for loop or iterators.

  ```cpp
  for (const auto& pair : myMap) {
      std::cout << pair.first << ": " << pair.second << std::endl; // Prints key-value pairs
  }
  ```
