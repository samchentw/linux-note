# ln(todo)

# 建立硬連結
```
ln temp.txt temp_test.txt

# 查看 inode
ls -i temp.txt temp_test.txt
```


# 建立軟連結
```
ln -s temp.txt temp_test.txt
# 查看 inode
ls -i temp.txt temp_test.txt
```