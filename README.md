# C++ Shell Project 🚀

A feature-rich, Unix-like shell developed in C++ that supports command execution, pipelines, I/O redirection, history management, and tab completion.

-----

## \#\# Features

### **Core Functionality**

  * **Interactive Command Line**: Full readline support with command history navigation.
  * **Built-in Commands**: `exit`, `echo`, `type`, `pwd`, `cd`, and `history`.
  * **External Command Execution**: Run any executable from your system's `$PATH`.
  * **Pipelines**: Chain multiple commands together using the `|` operator.
  * **I/O Redirection**: Redirect output of commands using `>` and `>>`.
  * **Tab Completion**: Autocomplete commands and file paths by pressing the `Tab` key.
  * **Quote Handling**: Properly handles single (`'`) and double (`"`) quotes.

### **Advanced Capabilities**

  * **Persistent History**: Command history is saved to a file (`~/.cpp_shell_history`) and loaded on startup.
  * **Tilde Expansion**: The `~` character is automatically expanded to the home directory.
  * **Signal Handling**: Gracefully handles `Ctrl+D` (EOF) to exit the shell.
  * **Robust Error Handling**: Provides clear error messages for common issues like command not found.

-----

## \#\# Getting Started

### **Prerequisites**

  * A Unix-like operating system (Linux, macOS).
  * A C++17 compatible compiler (e.g., GCC 7+ or Clang 5+).
  * The GNU Readline library for interactive input.

### **Installation**

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```
2.  **Install dependencies (on Debian/Ubuntu):**
    ```bash
    sudo apt-get update
    sudo apt-get install build-essential libreadline-dev
    ```
3.  **Compile the project:**
    ```bash
    g++ -std=c++17 -o cpp-shell src/*.cpp -lreadline
    ```
4.  **Run the shell:**
    ```bash
    ./cpp-shell
    ```

-----

## \#\# Usage Examples

### **Basic Commands**

```sh
$ pwd
/home/user/CPP-SHELL

$ echo "Hello from the C++ Shell!"
Hello from the C++ Shell!

$ cd ~
$ pwd
/home/user
```

### **Pipelines and Redirection**

```sh
# Find all C++ source files
$ ls -l src | grep .cpp

# Save output to a file
$ echo "This is a test." > output.txt
```

### **History Management**

```sh
# Display the last 10 commands
$ history 10

# Search history
$ history | grep "cd"
```

-----

## \#\# Built-in Commands

| Command   | Description                                         | Usage Example             |
| :-------- | :-------------------------------------------------- | :------------------------ |
| `cd`      | Change the current directory                        | `cd /path/to/dir` or `cd ~` |
| `pwd`     | Print the working directory                         | `pwd`                     |
| `echo`    | Display a line of text                              | `echo Hello World`        |
| `exit`    | Exit the shell                                      | `exit`                    |
| `type`    | Display how a command name would be interpreted     | `type ls`                 |
| `history` | Show command history                                | `history` or `history 5`  |

-----

## \#\# Limitations

This project is an educational implementation and currently lacks some advanced shell features, including:

  * Job control (`&`, `jobs`, `fg`, `bg`).
  * Variable expansion (`$VAR`) and command substitution.
  * Wildcard/glob expansion (`*`, `?`).
  * Complex control structures (`if`, `while`, `for`).

-----

## \#\# Future Enhancements

  * [ ] Add support for job control.
  * [ ] Implement variable expansion and substitution.
  * [ ] Introduce command aliases and a configuration file (e.g., `.cppshellrc`).
  * [ ] Add syntax highlighting for a better user experience.

