# linux-access
### A few sample files to introduce Access Queries

The file systems on Mac, PC, and Linux operating systems are essentially database systems. In this short demo I will ```gitclone``` the files in this repository into my opal account and use the ``ls`` command with some wildcards. You will need to use wildcards in Access, so the purpose of this demo is to show how the same query concepts can work across multiple operation systems and applications. 

I am only going to spend a few minutes on this. If you are comfortable logging into opal you can git clone the repository and work along with me. If you can't get this done now, just watch me and don't try to follow along.

**This git clone is not required, but I will check opal accounts at the end of the semester and if you need to improve your value added grade because of absences it will help your cause to have this directory in opal. (You can do it after class.)**

```
Mac > 
terminal > 
ssh onyen@opal.ils.unc.edu 
password > enter it
cd into public_html > 
git clone https://github.com/ljonesdesign/linux-access
cd linux (hit tab to complete)

PC > 
Secure shell client >
onyen@opal.ils.unc.edu 
password > enter it
cd into public_html > 
cd git clone https://github.com/ljonesdesign/linux-accessinux (hit tab to complete)
```

here are some commands to try:

## Find files with Martha in the name:
```
ls -l *martha*
```
this will list all files that contain the string LIKE martha:

```
[lblakej@opal linux-access]$ ls -l *martha*
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 martha.jpg
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 martha.txt
```

## Find files that have a capital M:
```
ls -l *M*
```
Remember that Linux is case sensitive. Capital M will only yield the readme file which contains a capital M:
```
[lblakej@opal linux-access]$ ls -l *M*
-rw-rw-r-- 1 lblakej lblakej 463 Apr 10 09:04 README.md
```

## Sort all files by file extension (e-**X**-tension)

```
ls -lX
```

Sorted by extension ascending (ASC):
```
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 kathy.jpg
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 kelly.jpg
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 martha.jpg
-rw-rw-r-- 1 lblakej lblakej 463 Apr 10 09:04 README.md
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 jackie.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 jake.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 janice.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 karen.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 kathy.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 kelly.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 martha.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 sam.txt
-rw-rw-r-- 1 lblakej lblakej   9 Apr 10 09:04 william.txt
```
## Find all files that start with ma OR ka and sort them by file extension.

```
[lblakej@opal linux-access]$ ls -lX {ma*,ka*}
```
result:

```
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 kathy.jpg
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 martha.jpg
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 karen.txt
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 kathy.txt
-rw-rw-r-- 1 lblakej lblakej 9 Apr 10 09:04 martha.txt
```
