# Binary File Record Manager (C++)

This C++ application is a specialized tool for managing structured records using **Binary Files**. Unlike text files, binary storage allows for direct memory-to-disk serialization of structures, making data access faster and more compact.

###  Logic & Binary I/O
The program manages a collection of records (e.g., student or product data) using a custom `struct`. The key technical highlight is the use of **binary mode** for file operations:
* **Serialization:** The program writes the entire structure to the file as a raw block of bytes using `file.write()`.
* **Deserialization:** It reads data back into memory using `file.read()`, preserving the exact state of the object.
* **Efficiency:** Binary files do not require parsing (like converting strings to numbers), which significantly improves performance for large datasets.



###  Key Features
* **Binary Persistence:** Stores data in a non-human-readable binary format to ensure data integrity and speed.
* **Record Management:** Includes functionality to add new records to an existing file without overwriting old data (append mode).
* **Search Algorithm:** Features a lookup mechanism to find specific records based on a key (e.g., ID or Name).
* **Robust Stream Handling:** Utilizes `std::fstream` with `ios::binary`, `ios::in`, and `ios::out` flags.

###  Technical Stack
* **Language:** C++
* **Header:** `<fstream>` (Binary file streams), `<iostream>`, `<cstring>`.
* **Concepts:** Binary I/O, Struct Serialization, Record-based storage.

###  How to Use
1. Run the application.
2. Select "Add Record" to enter new data into the binary file.
3. Use the "Display All" option to read and visualize the stored binary data in a readable format.
4. Use the "Search" function to locate a specific entry within the binary database.
