## 

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