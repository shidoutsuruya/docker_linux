# redis

## data structure

1. key-string
2. key-hash
3. key-list
4. key-set
5. key-zset

### string

1. `set [key] [value]` set key and value
2. `mset [key] [value]...` set multi key and value
3. `get [key]` get value
4. `get [key]...` get multi key and value
5. `incr [key]` increase key by 1
6. `decr [key]` decrease key by 1
7. `incrby [key] [num]` increase key by num
8. `decrby [key] [num]` decrease key by num
9. `setex [key] [second] [num]` set value with survival time
10. `append [key] [value]` append value content by specified key
11. `strlen [key]` string len of key
