## ✅ Python Mutable & Immutable Data Types – Full Explanation

Python classifies objects into mutable (changeable) and immutable (unchangeable).
But many subtleties exist:
- A container (tuple) can be immutable even if it holds mutable items.
- Mutability applies to the object, not the variable name.
- Some operations look like modifications but actually create new objects (strings, ints).
- Some immutables allow you to mutate referenced mutable children (special case!).

✅ 1. Data Type Mutability Table
---

  | Data Type        | Mutable?         | Can Contain Mutable Items?     | Can Contain Immutable Items? | Notes                                                |
| ---------------- | ---------------- | ------------------------------ | ---------------------------- | ---------------------------------------------------- |
| **int**          | ❌ No             | N/A                            | N/A                          | Completely immutable                                 |
| **float**        | ❌ No             | N/A                            | N/A                          | Immutable                                            |
| **bool**         | ❌ No             | N/A                            | N/A                          | Immutable                                            |
| **str**          | ❌ No             | N/A                            | N/A                          | Indexed but cannot modify characters                 |
| **tuple**        | ❌ No             | ✔ Yes                          | ✔ Yes                        | Immutable *structure* but mutable *contents* allowed |
| **frozenset**    | ❌ No             | ❌ No                           | ✔ Yes                        | Cannot contain mutable items                         |
| **bytes**        | ❌ No             | N/A                            | N/A                          | Immutable sequence of bytes                          |
| **list**         | ✔ Yes            | ✔ Yes                          | ✔ Yes                        | Fully mutable                                        |
| **dict**         | ✔ Yes            | Keys must be hashable          | Values: ✔ Yes                | Keys must be hashable                                |
| **set**          | ✔ Yes            | ❌ No                           | ✔ Yes                        | Set elements must be immutable                       |
| **bytearray**    | ✔ Yes            | N/A                            | N/A                          | Mutable form of bytes                                |
| **custom class** | ✔ Yes by default | ✔ Yes                          | ✔ Yes                        | Unless implemented otherwise                         |
---

✅ Container Compatibility Table
---
| Put This → Into This            | list | tuple | dict key | dict value | set | Notes                |
| ------------------------------- | ---- | ----- | -------- | ---------- | --- | -------------------- |
| **int**                         | ✔    | ✔     | ✔        | ✔          | ✔   | Immutable → hashable |
| **float**                       | ✔    | ✔     | ✔        | ✔          | ✔   |                      |
| **str**                         | ✔    | ✔     | ✔        | ✔          | ✔   |                      |
| **tuple (all immutable items)** | ✔    | ✔     | ✔        | ✔          | ✔   | Hashable             |
| **tuple (with mutable inside)** | ✔    |✔     | ❌        |  ✔         | ❌   | Not hashable         |
| **list**                        | ✔    | ✔     | ❌        | ✔          | ❌   | Lists are unhashable |
| **dict**                        | ✔    | ✔     | ❌        | ✔          | ❌   |                      |
| **set**                         | ✔    | ✔     | ❌        | ✔          | ❌   | Sets unhashable      |
| **frozenset**                   | ✔    | ✔     | ✔        | ✔          | ✔   | Hashable             |
| **bytearray**                   | ✔    | ✔     | ❌        | ✔          |  ❌   | Mutable              |

---
