# 🐚 myshell — Operating Systems Project

## 👩‍💻 Authors

* **Aseel Khalil Omar Hodhod** — 220200323
* **Amal Yasser Farouq Anan** — 220201122
* **Dalia Jamal Taher Abu Sharekh** — 220200747

---

## 📄 Overview

**myshell** is a custom command-line shell developed in **C** for **Ubuntu Linux** systems. It replicates essential features of traditional Unix shells, supporting internal commands, batch file execution, input/output redirection, and background process handling.

---

## 🚀 Features

* 📂 Internal command support
* 🧩 External program execution
* 📜 Batch file processing (`myshell script.bat`)
* 🔄 Input and output redirection (`<`, `>`, `>>`)
* 🧵 Background process execution using `&`

---

## 🧰 Internal Commands

| Command   | Description                           |
| --------- | ------------------------------------- |
| `cd`      | Change current working directory      |
| `pwd`     | Show current working directory        |
| `clr`     | Clear the terminal screen             |
| `dir`     | List directory contents               |
| `environ` | Display all environment variables     |
| `echo`    | Print text or file content            |
| `help`    | Show user manual and help information |
| `pause`   | Pause shell until Enter is pressed    |
| `quit`    | Exit the shell                        |
| `myshell` | Execute commands from a batch file    |

---

## ▶️ Usage

### Interactive Mode:

```bash
./myshell
```

### Batch Mode:

```bash
./myshell test.bat
```

myshell reads and executes commands from the batch file, then exits automatically.

---

## 📘 Batch File Example — `test.bat`

```bash
echo Welcome to myshell!
pwd
dir
cd /home
pause
quit
```

Run it with:

```bash
./myshell test.bat
```

---

## 🔄 Input & Output Redirection

| Symbol | Function                            |
| ------ | ----------------------------------- |
| `<`    | Redirect input from file            |
| `>`    | Redirect output to file (overwrite) |
| `>>`   | Redirect output to file (append)    |

Examples:

```bash
echo < input.txt > output.txt
dir > list.txt
cd < dir_path.txt
```

---

## 🧵 Background Execution

To run a command in the background, add `&`:

```bash
sleep 10 &
```

This allows myshell to continue receiving input without waiting for the command to finish.

---

## 📂 Path Formats

myshell supports:

* Relative paths: `./folder`, `../folder`
* Absolute paths: `/home/user`
* Special tokens:

  * `.` → current directory
  * `..` → parent directory
  * `~` → home directory

⚠️ Escape spaces in file or folder names using `\`:

```bash
echo < file\ name.txt
```

---

## 🧪 Example Commands

| Action               | Command                         |
| -------------------- | ------------------------------- |
| Change directory     | `cd /home/user`                 |
| Show current path    | `pwd > pwd.txt`                 |
| Display file content | `echo < input.txt > output.txt` |
| List directory files | `dir > list.txt`                |
| Pause the shell      | `pause`                         |
| Execute batch file   | `myshell script.bat`            |
| Run in background    | `sleep 5 &`                     |

---

## 📌 Notes

* If redirection fails, messages like "Path Error" or "File Error" will be shown.
* Only the last output file is considered if multiple redirections are chained.
* Background processes do not block the shell from receiving more commands.

---

## 📅 Submission Details

* **Course:** Operating Systems
* **Instructor:** Eng. Amal Mahfouz
* **Submission Date:** June 15, 2025
* **Project Title:** myshell – A Custom Command-Line Shell
