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

## User

In summary, as a sysadmin, you can choose between useradd and adduser based on your system's conventions and your specific needs. If you want a more streamlined and user-friendly approach for adding user accounts, adduser is often a better choice, especially on Debian-based systems.

However, if you need more control over the user account creation process, useradd provides a lower-level and more scriptable method. The availability and behavior of these commands may vary between different Linux distributions, so it's essential to be familiar with the conventions of the system you are working on.


| Command        | Description                                                                               |
| -------------- | ----------------------------------------------------------------------------------------- |
| useradd <username> | is a low-level command used for adding user accounts. |
| adduser <username> | is a higher-level command designed to simplify the process of adding user accounts. |
| su <username>  | change user |
| whoami | Displays the username of the current user. |

## ssh-keygen

| Command               | Description                                                      |
|-----------------------|------------------------------------------------------------------|
| `ssh-keygen`          | Generates an SSH key pair for secure authentication and encryption. |
| `ssh-keygen -t type`  | Specifies the type of key to create (e.g., RSA, ECDSA, ED25519).  |
| `ssh-keygen -b bits`  | Specifies the key size in bits (e.g., 2048, 4096 for RSA keys).  |
| `ssh-keygen -f file`  | Specifies the output file for the generated key pair.           |
| `ssh-keygen -N passphrase` | Sets a passphrase for the key (optional but recommended for added security). |
| `ssh-keygen -p`       | Changes the passphrase of an existing private key.              |
| `ssh-keygen -i`       | Converts an SSH key from OpenSSH to the SSH-2 format.            |
| `ssh-keygen -e`       | Converts an SSH key from SSH-2 to the OpenSSH format.            |
| `ssh-keygen -l`       | Display the fingerprint and size of the specified public key.   |

## rsync
nano ~/.ssh/authorized_keys
authorized_keys wird der öffentliche key gespeichert

## rsync

| Command           | Description                                        |
|-------------------|----------------------------------------------------|
| `rsync source destination` | Synchronizes files and directories from the source to the destination. |
| `rsync -a`        | Archive mode; preserves permissions, ownership, and more. |
| `rsync -v`        | Verbose mode; provides detailed output during synchronization. |
| `rsync -z`        | Compresses data during transfer to save bandwidth. |
| `rsync -r`        | Recursive mode; synchronizes directories and subdirectories. |
| `rsync -u`        | Update mode; skips files that are newer on the destination. |
| `rsync -n`        | Dry-run mode; shows what would be transferred without making changes. |
| `rsync -e 'ssh'`  | Specifies the remote shell to use (e.g., SSH for secure transfers). |
| `rsync --delete`  | Deletes files on the destination that are no longer in the source. |
| `rsync --exclude` | Excludes specified files or patterns from synchronization. |

## IP-Related Commands

|Command                 | Description
------------------------|------------------------------------------------|
|ifconfig                | Displays network interface configuration.|
|ping host               | Tests network connectivity to a host.|
|traceroute host         | Traces the route to a host and displays network hops.|
|netstat -r              | Shows the routing table.|
|dig domain              | Performs DNS lookups for a domain.|
|nslookup host           | Queries DNS servers for host information.|
|ip addr show          | Shows IP addresses associated with network interfaces.|
|ip link show          | Displays network interface information.|
|ip route show         | Shows the routing table.|
|ip route add          | Adds a route to the routing table.|
|ip route delete       | Deletes a route from the routing table.|
|ip neigh show         | Displays the neighbor table (ARP cache).|
|ip neigh add          | Adds an entry to the neighbor table.|
|ip neigh delete       | Deletes an entry from the neighbor table.|
|ip tunnel add         | Creates a tunnel device.|
|ip tunnel delete      | Deletes a tunnel device.|

## iptables

|Command                 | Description
|------------------------|------------------------------------------------|
|iptables -L             | Lists current firewall rules and chains.|
|iptables -A chain rule  | Appends a rule to a specified chain.|
|iptables -D chain rule  | Deletes a rule from a specified chain.|
|iptables -P chain target | Sets the default policy for a chain.|
|iptables -N chain       | Creates a new user-defined chain.|
|iptables -F chain       | Flushes (deletes) all rules in a chain.|
|iptables-save           | Saves current firewall rules to a file.|
|iptables-restore        | Restores firewall rules from a file.|
|iptables -S             | Displays a saveable rule set (all tables).|
|iptables -I chain rule  | Inserts a rule to a specified chain.|
|iptables -R chain rule  | Replaces a rule in a specified chain.|
|iptables -X chain       | Deletes a user-defined chain.|
|iptables -Z chain       | Zeroes the packet and byte counters in a chain.|

## telnet

|Command                 | Description
|------------------------|------------------------------------------------|
|telnet host             | Initiates a Telnet session to a remote host.|
|telnetd                 | Telnet server daemon for remote access.|
|telnet localhost        | Connects to the local host via Telnet.|

## Logfiles

|Log File                 | Description|
|-------------------------|-----------------------------------------------------|
|/var/log/syslog           | Records system logs and messages.|
|/var/log/auth.log         | Contains authentication-related logs.|
|/var/log/kern.log         | Kernel logs and messages.|
|/var/log/nginx/access.log | Logs HTTP access requests in Nginx.|
|/var/log/nginx/error.log  | Contains error messages for Nginx.|
|/var/log/apache2/access.log | Logs HTTP access requests in Apache.|
|/var/log/apache2/error.log | Contains error and warning messages for Apache.|
|/var/log/secure           | Security logs, including authentication events (Red Hat-based systems).|
|/var/log/ufw.log          | Logs for the Uncomplicated Firewall (UFW) on Ubuntu systems.|
|/var/log/firewalld        | Logs for FirewallD on CentOS and Fedora systems.|
|/var/log/dmesg            | Kernel logs generated during system boot and hardware detection.|
|/var/log/boot.log         | Logs information about system startup.|
|/var/log/mail.log         | Logs email-related events and messages (e.g., Postfix mail server).|

nur cd geht mi to home s:~$ 
