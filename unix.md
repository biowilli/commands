# Unix commands

lsb_release -a

| Command        | Description                                                                               |
| -------------- | ----------------------------------------------------------------------------------------- |
| lsb_release -a | version of a Linux distribution in general. For Ubuntu, Debian and related distributions. |

## Listing files

| Command | Description                                                                              |
| ------- | ---------------------------------------------------------------------------------------- |
| ls      | list files in current directory                                                          |
| ls -l   | list files in a long format                                                              |
| ls -a   | list all files (including hidden files) in current directory                             |
| ls -F   | adds indicators to the list output to identify directories and different types of files. |

## Files

| Command        | Description                                  |
| -------------- | -------------------------------------------- |
| cp file1 file2 | Makes a copy of `file1` and names it `file2` |
| mv file1 file2 | Moves (renames) `file1` to `file2`           |
| rm file1       | Removes (deletes) `file1`                    |
| rm -i file1    | Asks for confirmation to delete `file1`      |

## Text Files

| Command        | Description                                                              |
| -------------- | ------------------------------------------------------------------------ |
| cat file1      | Writes the contents of `file1` to the terminal                           |
| more file1     | Displays the contents of `file1` one page at a time                      |
| less file1     | A more versatile version of `more`, but less common                      |
| head -30 file1 | Shows the first 30 lines of `file1`                                      |
| tail -25 file1 | Shows the last 25 lines of `file1`                                       |
| tail -f file1  | Shows the last few lines of `file1` and keeps updating as the file grows |
| wc file1       | Counts the number of lines, words, and characters in `file1`             |

Source: https://www-users.york.ac.uk/~pjh503/linux/commands.html
