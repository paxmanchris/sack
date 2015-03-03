# Name
	sack - Quick and dirty backup tool for linux configuration files
# Synopsis
	sack <command> [<args>]
	sack save [<args>] filename
	sack restore [<args>] filename.0.gz filename
	sack history [<args>] filename
	sack diff backupfile filename
# Description
This tool is a quick and dirty method of backing up a file before you make changes. It creates a directory on root /sack/. If you run sack save /etc/filename, it will save to /sack/etc/filename.0.gz, and then filename.1.gz and so on.

# Usage

```
__save the file__
$ sack save /etc/apache/apache.conf 

__make a change__
$ sack /etc/apache/apache.conf

__oops! changes messed things up__
$ sack history /etc/apache/apache.conf
-rw-r--r--. 1 root root 98655 Feb 18 18:27 /bak/root/revisr.zip.0.tar.gz
-rw-r--r--. 1 root root 98655 Feb 18 18:27 /bak/root/revisr.zip.1.tar.gz
-rw-r--r--. 1 root root 98655 Feb 18 18:29 /bak/root/revisr.zip.2.tar.gz

$ fbak restore apache.conf.0.gz /etc/apache/apache.conf


# Arguments

-h      Show this help




