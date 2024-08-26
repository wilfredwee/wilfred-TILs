# Bash Learnings

Some things I'm learning/refreshing on Bash:

- Executing commands `$(COMMAND)` and  `` `COMMMAND` `` are equivalent. But `$(COMMAND)` is the [preferred way](https://stackoverflow.com/questions/22709371/backticks-vs-braces-in-bash).

- [Prefer](https://www.baeldung.com/linux/bash-single-vs-double-brackets) double brackets in `if` conditions to allow for easier operators.

- Use `-z` to test if `$VAR` is empty.
  
  ```bash
  if [[ -z "${VAR}" ]]; then
  fi
  ```

- `var=$(( a + b ))` is [shell arithmetic](https://www.gnu.org/software/bash/manual/bash.html#Shell-Arithmetic).

- `echo -n` to echo without newline
