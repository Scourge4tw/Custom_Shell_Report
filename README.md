# 🐧 LinusOS - Custom Linux Shell

A simple **C++ custom shell** built for the **Linux Operating System** as part of a capstone project.  
This shell provides basic command execution, process management, redirection, and piping functionalities — emulating essential features of Unix shells like `bash`.

---

## 🚀 Features

- ✅ **Command Parsing** – Tokenizes user input and executes commands  
- ✅ **Built-in Commands** – Supports `cd`, `mkfifo`, `history`, `!!`, and `!N`  
- ✅ **I/O Redirection** – Handles input (`<`), output (`>`), and error (`2>`) redirection  
- ✅ **Piping (`|`)** – Supports chaining multiple commands with pipes  
- ✅ **Background Execution (`&`)** – Runs processes in the background  
- ✅ **Command History** – Stores the last 10 executed commands with recall support  

---

## 🧠 Implementation Overview

The shell is built using:

- **C++ standard libraries** (`iostream`, `vector`, `string`)
- **UNIX system calls**:
  - `fork()`, `execvp()`, `pipe()`, `dup2()`, `waitpid()`
  - `open()`, `close()`, `chdir()`, `mkfifo()`
- **Custom helper functions**:
  - Tokenize commands
  - Separate piped commands
  - Manage command history (`!!` and `!N`)

---

## 🧩 Code Structure

| File | Description |
|------|--------------|
| `main.cpp` | Core shell implementation including parsing, redirection, and process handling |
| `README.md` | Project documentation (this file) |
| `Makefile` *(optional)* | For compiling and running easily using `make` |

---

## ⚙️ How to Run

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/LinusOS-Custom-Shell.git
cd LinusOS-Custom-Shell

2️⃣ Compile the shell
g++ main.cpp -o linus_shell

3️⃣ Run the shell
./linus_shell

4️⃣ Exit the shell
exit
