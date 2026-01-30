# Chapter 2 — Navigation and File System Commands  
*(Linux Fundamentals — Semester 1, Academic Year 2025/2026)*

---

##  Introduction  

In this chapter, we focus on one of the most important skills for any Linux user:  
**navigating the file system efficiently using the terminal**.

Linux provides powerful commands that allow users to move through directories, measure disk usage, and understand how storage is organized.

Mastering these tools is essential for future work in:

- System administration  
- Networking environments  
- Server management  

---

##  1. Changing Directories with `cd`

The command **cd** stands for:

> Change Directory

It allows you to move from one folder to another.

### Basic Syntax

> cd directory_name

### Example:
> cd Documents

### Going to the Root Directory
 To move directly to the root of the Linux file system:
> cd /

### You can verify your location with:
> pwd

### Moving to the Parent Directory:
 To go back one level:
> cd ..
 To go back two levels:
> cd ../..
 This is useful when navigating deep folder structures.
 

## 2.Relative vs Absolute Paths
 Linux supports two ways of specifying paths.

### Relative Paths:
 A relative path depends on your current directory.
### Exemple:
> cd games
This works only if games is inside the current folder.

### Absolute Paths:
 An absolute path always starts from the root /.
 ### Example:
> cd /usr/games
 Absolute paths work from anywhere in the system.

 ## 3.Returning to the Home Directory
  Your personal home folder is located in:
/home/username
  There are three easy ways to return home:
> cd /home/username
> cd ~
> cd
  The symbol ~ is a shortcut for the home directory.

 ## 4.Path Autocompletion (Tab Key)
  Linux provides a very useful feature called autocompletion.

Instead of typing long paths manually:
 > cd /usr/ga[TAB]

 The system automatically completes the folder name.

This helps:

Save time

Avoid spelling mistakes

Work faster in the terminal

## 5.Measuring Disk Usage with du
 The command du stands for:
 **Disk Usage**
 It shows how much space a directory occupies.

 ### Basic Usage:
 > du
  This displays the size of folders in the current directory.

### Human-Readable Format:
> du -h
  Displays sizes in KB, MB, or GB.

### Summary Only:
  To display only the total size:
> du -sh

### Including Files:
  To show both files and directories:
> du -ah

## Summary — What to Remember :
By the end of this chapter, you should know that:

cd is used to navigate between directories.

cd .. moves to the parent directory.

Paths can be relative or absolute.

~ represents the home directory.

Tab autocompletion improves efficiency.

du helps measure disk space usage.


## Skills Gained from This Chapter

After completing this chapter, I gained the ability to:

Navigate the Linux file system confidently.

Understand directory structures and path types.

Use shortcuts like ~ and autocompletion.

Monitor storage usage using du.

Build essential command-line skills for networking and OS studies.


  
 
 
 

  
