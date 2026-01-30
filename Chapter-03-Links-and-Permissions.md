# Chapter 3 — Links and File Permissions  
*(Linux Fundamentals — Semester 1, Academic Year 2025/2026)*

---

## Introduction  

In this chapter, we explore two essential Linux concepts:

- **Links between files**
- **Access permissions and user rights**

These topics are fundamental for understanding how Linux manages files securely and efficiently.

Mastering links and permissions is crucial for system administration, multi-user environments, and server security.

---

## 1. Creating Links Between Files (`ln`)

Linux allows the creation of links, which are similar to shortcuts in other operating systems.

The command used is:
> ln

### Linux supports two types of links:
   Hard Links
   Symbolic Links

## 2.Understanding Inodes
  ### In Linux, every file is stored with two main components:
        File name
        File content
The content is identified internally by a number called an inode.
This inode is what Linux uses to locate the real data on disk.

##3.Hard Links
  ###A hard link creates another filename that points to the same inode, meaning:
         Both files share the exact same content.
         Editing one edits the other.
         The file exists as long as at least one link remains.
  ###Creating a Hard Link:
  > ln file1 file2
  ###Example:
  > touch fichier1
  > ln fichier1 fichier2
Both names now refer to the same file content.

  ###Key Properties of Hard Links;
Hard links cannot be created for directories.
Deleting one name does not remove the data.
The inode disappears only when all links are deleted.

##4. Symbolic Links (Soft Links)
A symbolic link is more flexible.
Instead of pointing directly to the inode, it points to the filename.
 ###Creating a Symbolic Link:
 > ln -s file1 file2
 ###Example:
 > ln -s fichier1 fichier2
  ###Symbolic links are easy to recognize:
   fichier2 -> fichier1
  
###Key Properties of Symbolic Links
  Works with directories and files.
  If the original file is deleted, the link becomes broken.
  More commonly used than hard links.

##5. File Permissions in Linux
Linux is a multi-user operating system, so every file has permissions that define:
   Who can read it
   Who can modify it
   Who can execute it
   
Permissions are displayed using:
> ls -l

Example:
> -rw-r--r--

##6. Permission Groups
Permissions are divided into three categories:
| Category   | Meaning                 |
| ---------- | ----------------------- |
| User (u)   | Owner of the file       |
| Group (g)  | Users in the same group |
| Others (o) | Everyone else           |

##7. Permission Types
Each permission letter represents:
| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |
###Example:
  rw-  → read + write
  r--  → read only
  rwx  → full access

##8. Changing Permissions with Numbers (Absolute Mode):
Permissions can be represented using numbers:
  r = 4
  w = 2
  x = 1

###Total values:
| Rights | Value |
| ------ | ----- |
| ---    | 0     |
| r--    | 4     |
| rw-    | 6     |
| r-x    | 5     |
| rwx    | 7     |

###Example: Owner Only Access
 chmod 600 rapport.txt
 
Meaning:
  Owner: read + write
  Group: no access
  Others: no access

###Full Access for Everyone (Not Recommended)
chmod 777 file.sh

##9. Changing Permissions with Letters (Relative Mode)
 Linux also supports symbolic permission changes:
| Symbol | Meaning           |
| ------ | ----------------- |
| u      | user              |
| g      | group             |
| o      | others            |
| +      | add permission    |
| -      | remove permission |

Examples:
 chmod g+w file.txt     # add write to group
 chmod o-r file.txt     # remove read from others
 chmod +x script.sh     # make executable for all

## 10. Recursive Permissions
 To apply permissions to an entire directory and its contents:
chmod -R 700 /home/user
 This is useful for securing personal folders.

##Summary — What to Remember
By the end of this chapter, you should remember:

Linux supports hard and symbolic links.
Hard links share the same inode.
Symbolic links point to file names and work with directories.
Permissions control file access in multi-user systems.
chmod modifies rights using numbers or letters.
Recursive permissions apply changes to full directories.


##Skills Gained from This Chapter

After completing this chapter, I gained the ability to:
Understand Linux file linking mechanisms.
Create hard and symbolic links using ln.
Interpret permission strings with ls -l.
Secure files using chmod.
Manage access rights in Linux environments.




  







 



