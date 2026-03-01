# tds - Tiny Data Structures

Header-only data structures implementation in C.

## Features

- header-only
- type-safe
- educational purposes

## Examples

Use of the dynamic array:
```code
#include "tds.h"

int main(void) {
  int* numbers = NULL;

  da_push_back(numbers, 10);
  da_push_back(numbers, 20);

  for (size_t i = 0; i < da_count(numbers); ++i) {
    printf("%d\n", numbers[i]);
  }

  da_free(numbers);
}
```
You can also use your own structs:
```code
#include "tds.h"

typedef struct {
  int x;
  float y;
} item_t;

int main(void) {

  item_t* items = NULL;
  
  for (int i = 0; i < 5; ++i) {
      da_push_back(items, ((item_t){i, i + 0.5f}));
  }
  
  da_free(items);
}
```
