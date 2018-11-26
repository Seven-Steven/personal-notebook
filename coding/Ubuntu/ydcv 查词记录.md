# ydcv 查词记录
写一个 shell 脚本, 内容如下: 
```shell
#!/bin/sh
dir="/home/seven/.ydcv/"
# check dir
if [ ! -e $dir ]
then
    mkdir $dir -p
fi

# record
for i in $*
do
    echo $i >> $dir"wordlist.md"
done

# use ydcv to translate
/opt/ydcv/ydcv.py $*
```
