---
title: 'Using duckbd on WSL'
date: 2024-05-28
permalink: /posts/2024/05/Using_duckdb_on_WSL/
tags:
  - Computers
  - Windows
  - WSL
  - Linux
---

Updates 2025/05/28

My colleagues strongly recommended duckdb for (spatial) data analysis. Therefore, I started to install and learn duckdb. 

This note would keep a record of how I installed and used duckdb on Windows WSL.

# What is DuckDB

My understanding (and questions) of DuckDB is -- 

* A lightweight database tool on local machine (Q: can duckdb read a file from a remote machine?)
* Using SQL for data query and analysis
* Can work as a command line tool (CLI) or with Python or with R
* Much more efficient than pandas as it can read a subset of data into memory rather than the whole dataset; can replace pandas
* Support geospatial operations (GIS!)

# Installing duckdb

Installing DuckDB as a Python library is straightforward. If you use *pip*, then simply run this line: `pip install duckdb`.

Installing DuckDB as CLI takes several steps. According to [this page](https://duckdb.org/docs/installation/index?version=stable&environment=cli&platform=win&download_method=package_manager):

```
DuckDB is currently not available via apt/yum.
Please use one of the following binaries:
https://github.com/duckdb/duckdb/releases/download/v0.10.3/duckdb_cli-linux-amd64.zip
https://github.com/duckdb/duckdb/releases/download/v0.10.3/duckdb_cli-linux-aarch64.zip
```

It took three steps to install DuckDB on WSL:

Step 1: download the installer. Run the following command in WSL command line.

```
wget https://github.com/duckdb/duckdb/releases/download/v0.10.3/duckdb_cli-linux-amd64.zip
```

Step 2: unzip it. Again, run the following in command line (if you don't have unzip installed, install it). Then, you will get a file called duckdb in the current folder.

```
unzip https://github.com/duckdb/duckdb/releases/download/v0.10.3/duckdb_cli-linux-amd64.zip
```

Step 3: move the duckdb file to the /usr/local/bin folder so that you can call duckdb in any path of the computer.

```
sudo mv duckdb /usr/local/bin
```

I was interested in *what duckdb file really is*, so I ran this command to check it:

```
file /usr/local/bin/duckdb
```

You will get this result: `/usr/local/bin/duckdb: ELF 64-bit LSB executable, x86-64, version 1 (GNU/Linux), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=690a4b7267ddcc1f7584b8b12570ae8d965ae276, for GNU/Linux 2.6.32, not stripped`

Simply speaking, this is a file that can be executed.

# Testing DuckDB on CLI



# Reference

1. DuckDB installation: https://duckdb.org/docs/installation/index?version=stable&environment=cli&platform=linux&download_method=package_manager
2. DuckDB tutorial for beginners: https://motherduck.com/blog/duckdb-tutorial-for-beginners/

