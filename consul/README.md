# Consul KV Migration utility

Key-value store is one of the important feature provided by Consul which is used by multiple Engineers for multiple use-cases.
Migration is one of the challenging task which user faces while using consul. So, We created python script will helps user to migrate key-value data from one consul server to another and also helps user to get information about migration by getting different types of output like in JSON & Table.

## prerequisite
- Two consul servers
- python3
- libraries
  - from consul_kv import Connection
  - json
  - ast
  - prettytable
  - getopt
  - sys

## Get help using -h tag

```
python3 consul.py -h
```
output:
```
Usage: python <NAME-OF-SCRIPT>.py ... [ -<OPTIONS> <VALUES>]

Mendatory Option and arguments

-s : Provide source consul URL
     FORMAT: -s <VALUE>

-d : Provide destination consul URL
     FORMAT: -d <VALUE>

-o : Provide database hostname

     FORMAT: -o <VALUE>
     SUPPORTED TAGS:
         - json
         - table

AUTHOR: https://github.com/b44rawat
```

## Format

```
python3 consul.py  -s <SOURCE-ADDRESS> -d <DESTINATION-ADDRESS> -o table
```

## Output types

- table
- json

## Example 

```
 python3 consul.py  -s http://192.168.1.x:8500/v1/ -d http://192.168.0.x:8500/v1/ -o table
```

## Upcoming

- YAML Output
- Token support
