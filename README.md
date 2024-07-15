# Linux-Shell

  # Basic Shell Loop:

    * The shell continuously prompts the user for input and processes the commands entered.
    * It displays the current working directory using getcwd().
    
  # Reading and Tokenizing Input:

    * User input is read using the readline() function from the GNU Readline library, which provides a convenient way to handle command-line input.
    * The input is tokenized using strtok() to separate the command and its arguments.
    
  # Handling Internal Commands:

    cd: Changes the current directory using chdir().
    pwd: Prints the current working directory. Supports -L (logical) and -P (physical) options.
    echo: Prints the given arguments to the standard output. Supports -E (disable interpretation of backslash escapes) and -n (do not output the trailing newline) options.
    
  # Handling External Commands:

    The shell identifies external commands (ls, cat, date, rm) and executes them using the fork() and execvp() system calls.
    
  # Multithreading: If a command ends with &t, it is executed in a separate thread using pthread_create() and system().
  
  # Process Control:
    * Uses fork() to create a new process for external commands.
    * Uses wait() to wait for the child process to finish execution.
