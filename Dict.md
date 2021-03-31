# 字典
Dict是Python中非常重要的数据类型，就像它的字面意思一样，它是个活字典，其实就是Key-Value键值对，类似于HashMap，可以用花括号{}定义。
```python
alien_0 = {'color': 'green', 'points': 5}
```

## 字典操作
### 访问
List和Tuple用下标来访问内容，而Dict用Key来访问。

(字符串、整型、浮点型和元组tuple都可以作为dict的key)

```python
alien_0 = {'color': 'green', 'points': 5}
print(alien_0['color'])

green
```
### 添加键值对
```python
alien_0['height': 2]
print(alien_0)

{'color': 'green', 'points': 5, 'height': 2}
```

### 删除键值对
```python
del alien_0['points']
print(alien_0)

{'color': 'green', 'height': 2}
```

## 字典遍历

1. 全部遍历

字典的遍历的顺序与存储顺序不同。
```python
for key, value in alien_0.items():
    print("\nk: " +key + "v: " + value)

```

2. 遍历所有键

```python
for key in alien_0.keys():
    print("\nk: " +key )
```
或 
```python
#python遍历字典时， 默认遍历所有的键
for key in alien_0:
    print("\nk: " +key )
```
方法```keys()```实际上返回一个包含所有键的列表 所以可以用来判断该键是否存在
```python
if 'color' not in alien_0.keys()
    print("There is no defined color.")
```

3. 按顺序遍历所有键
```python
for key in sorted(alien_0.keys()):
    print("\nk: " +key )
```

4. 遍历所有值
```python
for value in alien_0.values():
    print("\nv: " + value )
```
该方法不考虑重复，可使用```set()```去重
```python
for value in set(alien_0.values()):
    print("\nv: " + value )
```

## 特点

1. 查找速度快。

    无论是10个还是10万个，速度都是一样的，但是代价是耗费的内存大。List相反，占用内存小，但是查找速度慢。这就好比是数组和链表的区别，数组并不知道要开辟多少空间，所以往往开始就会开辟一个大空间，但是直接通过下标查找速度快；而链表占用的空间小，但是查找的时候必须顺序的遍历导致速度很慢。

2. 没有顺序。

    Dict是无顺序的，而List是有序的集合，所以不能用Dict来存储有序集合
    Key不可变，Value可变。一旦一个键值对加入dict后，它对应的key就不能再变了，但是Value是可以变化的。所以List不可以当做Dict的Key，但是可以作为Value。