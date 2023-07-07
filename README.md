directory structure
==
```bash
    .
    ├── CMakeLists.txt
    ├── README.md
    ├── includes
    │   └── test.hpp
    ├── lib
    │   ├── CMakeLists.txt
    │   ├── includes
    │   │   └── lib_test.hpp
    │   └── src
    │       └── lib_test.cpp
    └── src
        ├── main.cpp
        └── test.cpp
```

How to build
==
```bash
cmake -S . -B build
cmake --build build
```
