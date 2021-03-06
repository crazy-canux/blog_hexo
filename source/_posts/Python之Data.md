---
layout: post
title: Python之Data
comments: true
date: 2016-08-14 20:57:36
updated:
tags:
categories:
- Python
permalink:
---

# Data Types

## datetime

    import datetime

    datetime.datetime.strptime(string, format)
    format_time = datetime.datetime.strptime('20160824161431', '%Y%m%d%H%M%S') # return: datetime.datetime(2016, 8, 24, 16, 14, 31)
    format_time = datetime.datetime.strptime('24 August 2016 16:14:31', '%Y%m%d%H%M%S') # return: datetime.datetime(2016, 8, 24, 16, 14, 31)

    datetime.datetime.strftime(format[, tuple])
    string_datetime = format_datetime.strftime("%d %B %Y %H:%M:%S") # return: '24 August 2016 16:14:31'

## calendar

## collections

## heapq

## bisect

## array

## sched

## Queue

## weakref

## UserDict

## UserList

## UserString

## types

## copy

## pprint

## repr

***

# Data Persistence

## pickle

## cPickle

## cope_reg

## pickletools

## shelve

## marshal

## anydbm

## whichdb

## dbm

## gdbm

## dumbdbm

***

# Data Compression and Archiving

## gzip

## bz2

## zlib

## zipfile

## tarfile

***

# Database

python访问数据库两种方式：
1. ORM
2. DB-API

ORM是对象-关系管理器，相关模块有SQLAlchemy, SQLObject.

DB-API参考PEP249,PEP249定义了Database的API。

<https://www.python.org/dev/peps/pep-0249/>

## sqlite

    import sqlite3
    cxn = sqlite3.connect(r'/path/to/file')
    cur = cxn.cursor()
    cur.execute(<sql>)
    ...
    cur.close()
    cxn.close()
