# Minishell

A minimal Unix shell written in C as part of the 42 curriculum. The project recreates some of the core behaviour of Bash, including command execution, pipes, redirections, environment variables and built-in commands.

## My contribution

This was a collaborative project. I was primarily responsible for the parsing subsystem, working on how user input is interpreted and prepared before execution.

This involved handling commands, arguments, quotes, environment variables and shell operators, ensuring that the input could be correctly processed by the execution part of the shell.

## Features

- Command execution using `PATH` or absolute and relative paths
- Pipes to connect multiple commands
- Input, output and append redirections
- Here-documents
- Single and double quote handling
- Environment variable expansion, including the exit status (`$?`)
- Shell operators
- Built-in commands: `echo`, `cd`, `pwd`, `export`, `unset`, `env` and `exit`
- Command history and interactive prompt
- Signal handling for interactive use

## Memory management

The project was designed to avoid memory leaks, with the exception of known leaks originating from the GNU Readline library.

## Technologies

- C
- Unix processes and file descriptors
- Pipes and redirections
- Signals
- GNU Readline
- Make

## Compilation and usage

Clone the repository and compile the project:

```bash
make
```

Run the shell:

```bash
./minishell
```

Example commands:

```bash
ls -la | grep .c > files.txt
echo $PATH
cd ~/projects && make
```

## Context

Minishell was developed as a team project at 42, with the goal of understanding how a Unix shell processes user input and manages command execution.
