# **Linux System Monitoring Tools**  🧰


1. top: It allows you  to see through all your system, all the processes.  **NOTE** : *B-*
     

2. Htop: pro's much more clearer than "*top*" command ( with colors) with  filters ( apt install) **NOTE** :A

3. glances : cross plateform - much infos more than htop       ( apt install) **NOTE** : A+

4. Whowatch : list of logos & more **NOTE**  A+

5. bpytop : “bpytop” tool is also one such tool. Its functionality  is very much similar 
            to  “top” and “Htop" (python3 install)





 # **Storage Space Utilization**

There are 2 well-known commands in Linux that are used to inspect storage space usage:

    # df 
    # du

The first one, df (which stands for disk free), is typically used to report overall disk space usage by file system.

    Example 1: Reporting disk space usage in bytes and human-readable format
    # df
    # df -h

    Without options, "*df*" reports disk space usage in bytes. With the -h flag it will display the same information using MB or GB instead. Note that this report also includes the total size of each file system (in 1-K blocks), the free and available spaces, and the mount point of each storage device.


    Example 2: Inspecting *inode usage by file system in        human-readable  
    # df -hTi

**The inode (index node) is a data structure in a Unix-style file system that describes a file-system object such as a file or a directory. Each inode stores the attributes and disk block locations of the object's data.*

Example 3: Finding and / or deleting empty files and directories

     to find empty files or directories:
        # find  /home -type f -empty
        # find  /home -type d -empty
Also, you can add the -delete flag at the end of each command if you also want to delete those empty files and directories:

    # find  /home -type f -empty --delete
    # find  /home -type f -empty

    Example 4: Examining disk usage by directory




    # du -sch /home/*


 




# **Memory and CPU Utilization**


The classic tool in Linux that is used to perform an overall check of CPU / memory utilization and process management is "top" command. In addition, top displays a real-time view of a running system. There other tools that could be used for the same purpose, such as "htop"

 ![image](https://www.tecmint.com/wp-content/uploads/2015/01/List-of-Running-Linux-Processes.png)

1. The current time 

2. Currently there are 121 processes running

3. us (time running user processes with unmodified priority), sy (time running kernel processes), ni (time running user processes with modified priority), wa (time waiting for I/O completion), hi (time spent servicing hardware interrupts), si (time spent servicing software interrupts), st (time stolen from the current vm by the hypervisor – only in virtualized environments).

4. Physical memory usage.

5. Swap space usage.

6. Inspecting physical memory usage

         you can also use free command.
        # free




you can also use the -m (MB) or -g (GB) switches to display the same information in human-readable form:

               # free -m



There are two tools that we will use to monitor processes closely:
                         
                # ps and pstree.

Using the *-e* and *-f* options combined into one (-ef) you can list all the processes that are currently running on your system. You can pipe this output to other tools, such as grep

![image](https://www.tecmint.com/wp-content/uploads/2015/01/Monitor-Linux-Processes.png)


#ps -eo user,comm,pid,ppid,%mem --sort -%mem

![image](https://www.tecmint.com/wp-content/uploads/2015/01/Monitor-Linux-Processes-by-Memory-Utilization.png)







# **How to View & Read Linux Log Files**




The "w" command is a built-in tool that allows administrators to view information about users that are currently logged in. This includes their username, where they are logged in from, and what they are currently doing.

   
the first thing to be done, when a problem arises, is to view the logs.


        # cd /var/log
    


"*whowatch*" is a simple, easy-to-use interactive who-like command line program for monitoring processes and users on a Linux system. It shows who is logged on to your system and what they are doing, in a similar fashion as the w command in real-time.





# Network Configuration, Troubleshooting, and Debugging Tools


Linux based distributions have featured set of commands which provide way to configure networking in easy and powerful way through command-line. These set of commands are available from net-tools package which has been there for a long time on almost all distributions, and includes commands like: 

- ifconfig
- route
- nameif
- iwconfig
- iptunnel,
- netstat
- arp
- mtr
- ping...






