# Unix commands


| Command        | Description                                                                               |
| -------------- | ----------------------------------------------------------------------------------------- |
| lsb_release -a | version of a Linux distribution in general. For Ubuntu, Debian and related distributions. |
| cat /etc/issue | version of a distribution.|


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

## CRON

| Command                  | Description                                                |
|--------------------------|------------------------------------------------------------|
| `crontab -l`             | Displays the current Cron jobs for the user.              |
| `crontab -l -u USERNAME`  | Displays the Cron jobs of another user.                    |
| `crontab -e`             | Opens the text editor for editing Cron jobs.              |
| `crontab -e -u USERNAME`  | Opens the text editor for editing Cron jobs of another user. |
| Crontab File Format:
* * * * Command to be executed      | Here is an explanation for each field:

    Minute (0 - 59): The first field indicates in which minute the job will be executed. An asterisk (*) means that the job will be executed in every minute.

    Hour (0 - 23): The second field indicates at what hour the job will be executed. An asterisk (*) means that the job will be executed every hour.

    Day of the month (1 - 31): The third field indicates on which day of the month the job will be executed. An asterisk (*) means that the job will be executed on every day of the month.

    Month (1 - 12 or Jan - Dec): The fourth field indicates in which month the job will be executed. An asterisk (*) means that the job will be executed in every month. You can use either numbers (1-12) or the first three letters of the month name (Jan - Dec).

    Day of the week (0 - 6 or Sunday - Saturday): The fifth field indicates which day of the week the job will run. An asterisk (*) means that the job will be executed on any day of the week. You can use either numbers (0-6, where 0 stands for Sunday) or the full weekday names (Sunday - Saturday). 
    |

# User

In summary, as a sysadmin, you can choose between useradd and adduser based on your system's conventions and your specific needs. If you want a more streamlined and user-friendly approach for adding user accounts, adduser is often a better choice, especially on Debian-based systems.

However, if you need more control over the user account creation process, useradd provides a lower-level and more scriptable method. The availability and behavior of these commands may vary between different Linux distributions, so it's essential to be familiar with the conventions of the system you are working on.


| Command        | Description                                                                               |
| -------------- | ----------------------------------------------------------------------------------------- |
| useradd <username> | is a low-level command used for adding user accounts. |
| adduser <username> | is a higher-level command designed to simplify the process of adding user accounts. |
| su <username>  | change user |
| whoami | Displays the username of the current user. |

nur cd geht mi to home s:~$ 
