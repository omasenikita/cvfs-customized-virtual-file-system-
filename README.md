# 📂 Customised Virtual File System (CVFS)

CVFS is a **Linux-like file system simulator** implemented in **C/C++**, designed to mimic the **core functionalities of the Linux file system**.  
It provides a **custom shell interface**, simulates **system calls**, and manages **file system data structures** such as the **SuperBlock, Incore Inode Table, File Table, UAREA, and User File Descriptor Table**.  

This project is both a **learning tool for operating system concepts** and a **practical showcase of system-level programming**.  

---

## ✨ Features

### 🔹 Custom Shell Interface
- Interactive shell with Linux-style commands:
  - `creat` – Create new file  
  - `open` – Open existing file  
  - `write` – Write data into file  
  - `read` – Read data from file  
  - `lseek` – Change file offset  
  - `stat` – Show file information  
  - `ls` – List all files  
  - `rm / unlink` – Delete file  
  - `close` – Close opened file  
  - `help` – Display command usage  
  - `man` – Manual for commands  
  - `clear` – Clear the terminal  
  - `exit` – Exit CVFS shell  

### 🔹 System Call Simulation
- Implements core Linux file system calls in **C/C++**:
  - `open`, `read`, `write`, `lseek`, `close`, `unlink`  

### 🔹 File System Data Structures
- **SuperBlock** – Tracks free inodes and blocks  
- **Incore Inode Table (I-Node)** – Metadata of files  
- **File Table** – File offset & mode for opened files  
- **UAREA (User Area)** – User-level file descriptor table  

### 🔹 Error Handling
- Uses **custom macros** for error codes:
  - `ERR_FILE_ALREADY_EXIST`  
  - `ERR_FILE_NOT_FOUND`  
  - `ERR_PERMISSION_DENIED`  
  - `ERR_INVALID_PARAMETER`  

### 🔹 Platform Independent
- Runs on **any OS with GCC/G++ compiler**.  

---

## 🎯 Learning Outcomes
By working with **CVFS**, you will gain:
- Deep understanding of **Linux File System internals**.  
- Practical knowledge of **OS data structures**.  
- Strong grasp of **system-level programming** in **C/C++**.  
- Hands-on experience with **command interpreters**.  
- Error-handling techniques using **macros**.  

---

## 🖥️ Example Usage
```bash
$ ./Myexe
Marvellous CVFS > creat Demo.txt 3
File is succesfully created with FD : 0

Marvellous CVFS > write 0
Please enter the data that you want to write into the file :
Hello World
11 bytes gets succesfully written into the file

Marvellous CVFS > read 0 11
Read operation is successfull
Data from file is : Hello World

Marvellous CVFS > stat Demo.txt
------------ Statistical Information of file -----------
File name : Demo.txt
File size on Disk : 100
Actual File size : 11
Link count : 1
File permission : Read + Write
File type : Regular file
--------------------------------------------------------

Marvellous CVFS > unlink Demo.txt
Unlink Operation is succesfully performed

Marvellous CVFS > exit
Thank you for using Marvellous CVFS
Deallocating all resources...
