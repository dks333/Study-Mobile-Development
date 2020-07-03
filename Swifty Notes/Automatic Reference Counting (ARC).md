# Automatic Reference Counting (ARC)



## How it works

- Keeping counting the number of strong references
- The instance is not deallocated until the last strong reference is broken

## Retain Cycle (Strong Reference Cycle)

- Problem: Memory Leak
- Cause: two strong references pointing to each other
- Solution:
  - Weak references
  - Unowned References
    - Alwasys refers to an instance that has not been deallocated
    - Runtime error occurs when access unwed reference after the instance has been deallocated
    - An unowed optional reference can be nil



