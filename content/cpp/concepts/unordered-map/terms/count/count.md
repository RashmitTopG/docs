---
Title: '.count()'
Description: 'Checks if a key exists in an unordered map.'
Subjects:
  - 'Computer Science'
  - 'Game Development'
Tags:
  - 'Objects'
  - 'OOP'
  - 'Classes'
CatalogContent:
  - 'learn-c-plus-plus'
  - 'paths/computer-science'
---

Elements can be checked in a map using the **`.count()`** method, which returns 1 if the key exists and 0 if it does not.

## Syntax

The .count() method is called on an unordered map object using the following syntax:

```pseudo
mapName.count(key);
```

- `mapName`: The name of the unordered map.
- `key`: The key to check for existence in the map.

## Codebyte Example 1

The following codebyte example demonstrates the use of the .count() method with an unordered_map to check for mammals and display their lifespans:

```codebyte/cpp
#include <iostream>
#include <unordered_map>

int main() {
    // Initializing unordered_map
    std::unordered_map<std::string, int> lifeSpan = {
        {"Giraffe", 26},
        {"Goat", 15},
        {"Lion", 10},
        {"Tiger", 8}
    };

    // Checking the existence of elements using .count()
    std::string mammals[] = {"Giraffe", "Elephant", "Lion", "Zebra"};

    for (const auto& mammal : mammals) {
        if (lifeSpan.count(mammal) > 0) {
            std::cout << mammal << " exists in the map with an average lifespan of " << lifeSpan[mammal] << " years.\n";
        } else {
            std::cout << mammal << " does not exist in the map.\n";
        }
    }

    return 0;
}
```

## Codebyte Example 2

The following codebyte example demonstrates the use of the .count() method with an unordered_map to check for the presence of various fruits and their prices:

```codebyte/cpp
#include <iostream>
#include <unordered_map>

int main() {
    // Initializing unordered_map with fruits and their prices
    std::unordered_map<std::string, double> fruitPrices = {
        {"Apple", 0.99},
        {"Banana", 0.59},
        {"Cherry", 2.99},
        {"Date", 3.49}
    };

    // Checking the existence of fruits using .count()
    std::string fruits[] = {"Apple", "Mango", "Cherry", "Pineapple"};

    for (const auto& fruit : fruits) {
        if (fruitPrices.count(fruit) > 0) {
            std::cout << fruit << " is available at $" << fruitPrices[fruit] << " each.\n";
        } else {
            std::cout << fruit << " is not available.\n";
        }
    }

    return 0;
}
```