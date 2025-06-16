# 🐚 myshell — Operating Systems Project

---

## 📅 Submission Details

* **Course:** Operating Systems
* **Instructor:** Eng. Amal Mahfouz
* **Submission Date:** June 16, 2025
* **Project Title:** `myshell` – A Custom Command-Line Shell

---

## 👩‍💻 Authors

* **Aseel Khalil Omar Hodhod** (220200323)
* **Amal Yasser Farouq Anan** (220201122)
* **Dalia Jamal Taher Abu Sharekh** (220200747)

---

## 📄 Overview

**myshell** is a robust, custom-built command-line shell developed in **C** for **Ubuntu Linux** environments. This project aims to replicate the core functionalities of standard Unix shells, offering users a familiar yet insightful experience into operating system fundamentals. It supports a suite of internal commands, seamless execution of batch files, flexible input/output redirection, and efficient background process management.

---

## 🚀 Key Features

* **📂 Internal Command Execution:** Efficiently handles built-in shell commands directly within `myshell`, ensuring quick and reliable core functionalities.
* **💡 External Program Support:** Seamlessly executes external programs and utilities available on the system, extending `myshell`'s capabilities beyond its internal commands.
* **📜 Batch File Processing (`myshell script.bat`):** Enables automated execution of a sequence of commands from a script file, ideal for task automation and repetitive operations.
* **🔄 Input/Output Redirection (`<`, `>`, `>>`):** Provides powerful control over data flow, allowing command input to be sourced from files and output to be directed to files (overwriting or appending).
* **🧵 Background Process Execution (`&`):** Allows long-running commands to execute in the background, freeing up the shell for immediate interactive use and improving user productivity.

---

## ✨ Project Significance

`myshell` serves as an invaluable learning tool, demonstrating fundamental concepts in operating systems such as process management, inter-process communication, file I/O, and command parsing. Developing `myshell` has provided practical experience in:

* **System Programming:** A deep dive into low-level C programming for system-level interactions.
* **Concurrency:** Understanding and implementing background processes.
* **Resource Management:** Efficiently handling file descriptors and process resources.
* **Command Line Interface (CLI) Design:** Gaining insights into the architecture and user interaction of a shell.

---

## 🧰 Supported Internal Commands

| Command   | Description                                     |
| :-------- | :---------------------------------------------- |
| `cd`      | Change the current working directory            |
| `pwd`     | Print the current working directory             |
| `clr`     | Clear the terminal screen                       |
| `dir`     | List contents of a directory                    |
| `environ` | Show all environment variables                  |
| `echo`    | Display a line of text or file content          |
| `help`    | Display user manual and command help            |
| `pause`   | Pause shell until Enter key is pressed          |
| `quit`    | Exit the shell                                  |
| `myshell` | Execute commands from a batch file              |

---

## ▶️ Usage

### Interactive Mode

Launch `myshell` in interactive mode to enter commands directly:

```bash
./myshell
```

### Batch Mode

Execute commands from a specified batch file. `myshell` will process each command line by line and then exit automatically.

```bash
./myshell test.bat
```

---

## 📚 Getting Help Inside the Shell

* **View all available internal commands:**

    ```bash
    help commands
    ```

* **Get detailed help for a specific topic or command:**

    ```bash
    help cd
    help redirection
    help path
    ```

* **Display the full `myshell` user manual:**

    ```bash
    help more
    ```

---

## ✍️ Batch File Example (`test.bat`)

Create a file named **`test.bat`** with the following content:

```bash
echo Welcome to myshell!
pwd
dir
cd /home
pause
quit
```

Then, run it using `myshell`:

```bash
./myshell test.bat
```

---

## 🔄 I/O Redirection

`myshell` supports standard input and output redirection:

| Symbol | Function                 |
| :----- | :----------------------- |
| `<`    | Input from file          |
| `>`    | Output to file (overwrite) |
| `>>`   | Output to file (append)  |

Examples:

```bash
echo < input.txt > output.txt
dir > list.txt
cd < dir_path.txt
```

---

## 🔧 Background Execution

To run a command in the background, append an ampersand (`&`) to the command. This allows `myshell` to continue accepting new commands without waiting for the background process to complete.

```bash
long_task &
```

---

## 📂 Path Formats

`myshell` supports various path formats for flexibility:

* **Relative paths:** (`./folder`, `../folder`)
* **Absolute paths:** (`/home/user`)
* **Special tokens:**
    * `..` → parent directory
    * `.` → current directory
    * `~` → home directory (resolves to the user's home directory)

⚠️ **Important:** Use a backslash (`\`) to escape spaces in file or directory names:

```bash
echo < file\ name.txt
```

---

## 📘 Example Commands

| Action                    | Command                         |
| :------------------------ | :------------------------------ |
| Change directory          | `cd /home/user`                 |
| Show current directory    | `pwd > pwd.txt`                 |
| Display file content      | `echo < input.txt > output.txt` |
| List files                | `dir > list.txt`                |
| Pause execution           | `pause`                         |
| Run batch file            | `myshell script.bat`            |
| Background command        | `sleep 5 &`                     |

---

## 📌 Notes

* If a redirection operation fails, `myshell` will report either "Path Error" or "Open Error."
* In a sequence of multiple output redirections (e.g., `cmd > file1 > file2`), only the last specified output file (`file2`) will be used.
* Background processes execute asynchronously and do not block further input to the shell.

---

## 💡 Future Enhancements

We envision several potential improvements for `myshell`, including:

* **Piping (`|`):** Support for redirecting the output of one command as the input to another.
* **Job Control:** More advanced management of background processes (e.g., `fg`, `bg`, `jobs`).
* **Command History:** Ability to recall previous commands using arrow keys.
* **Tab Completion:** Autocompletion for commands and file paths.
* **Scripting Language Features:** Basic control flow (if/else, loops) for more complex batch files.

---
