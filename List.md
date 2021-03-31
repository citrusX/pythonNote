# 列表
字面意思就是一个集合，在Python中List中的元素用中括号[ ]来表示，可以这样定义一个List:
```python
L = [12, 'China', 19.998]
```
可以看到并不要求元素的类型都是一样的。当然也可以定义一个空的。

```python
print(L)
len(L)

[12, 'China', 19.998]
3
```

## 修改，添加，删除元素

### 修改元素
```python
L[0] = 15

[15, 'China', 19.998]
```
### 添加元素
1. 在列表末尾添加元素
```python
L.append('honda')

[15, 'China', 19.998, 'honda']
```
2. 在列表中插入元素
```python
L.insert(0, 'yamaha')

['yamaha', 15, 'China', 19.998, 'honda']
```
### 删除元素
1. 使用```del(index)```语句
标注位置
```python
L.del(0)

[15, 'China', 19.998, 'honda']
```
2. 使用```pop()```
删除末尾元素并可使用
```python
pop_element = L.pop()
print(L)

[15, 'China', 19.998]

print(pop_element)
honda
```
3. 弹出任何位置元素
```pop(index)```
```python
pop_element = L.pop(0)
print(L)

['China', 19.998]


print(pop_element)
15
```
4. 根据值删除元素
```remove(value)```
```python
L = ['yamaha', 15, 'China', 19.998, 'honda']
L.remove(15)


['yamaha', 'China', 19.998, 'honda']
```

### 组织列表
1. 使用```sort()``` 进行永久性排序
```python
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
print(cars)

['audi', 'bmw', 'subaru', 'toyota']

cars.sort(reverse = True)
print(cars)

['toyota', 'subaru', 'bmw', 'audi']
```
2. 使用```sorted()``` 进行临时排序
```python
cars = ['bmw', 'audi', 'toyota', 'subaru']

print(sorted(cars))
['audi', 'bmw', 'subaru', 'toyota']


print(cars)
['bmw', 'audi', 'toyota', 'subaru']
```
3. 反转打印```reverse()```

将原列表顺序反转而不是排序
```python
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.reverse()
print(cars)

['subaru', 'toyota', 'audi', 'bmw']
```


## 列表切片
取头不取尾
```python
cars = ['bmw', 'audi', 'toyota', 'subaru', 'honda']

print(cars[1:4])
['audi', 'toyota', 'subaru']

print(cars[:4])
['bmw', 'audi', 'toyota', 'subaru']

print(cars[2:])
['toyota', 'subaru', 'honda']

print(cars[-2:])
#打印后两个
['subaru', 'honda']
```
一种神奇的用法：
```python
import numpy as np
a=np.random.rand(5)
print(a)
[ 0.64061262  0.8451399   0.965673    0.89256687  0.48518743]
 
print(a[-1]) ###取最后一个元素
[0.48518743]
 
print(a[:-1])  ### 除了最后一个取全部
[ 0.64061262  0.8451399   0.965673    0.89256687]
 
print(a[::-1]) ### 取从后向前（相反）的元素
[ 0.48518743  0.89256687  0.965673    0.8451399   0.64061262]
 
print(a[2::-1]) ### 取从下标为2的元素翻转读取
[ 0.965673  0.8451399   0.64061262]
```

按奇偶拆分list
```python
range_data = ['m', 'M', 'h', 'c', 'X', 'Z', 'A', 'o']
print range_data[::2]
print range_data[1::2]


['m', 'h', 'X', 'A']
['M', 'c', 'Z', 'o']
```



### 复制列表
1. 创建列表的副本
```python
cars = ['bmw', 'audi', 'toyota', 'subaru', 'honda']
new_cars = cars[:]
cars.append('benz')

print(cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']

print(new_cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda']
```

2. 指向同一个列表(复制失败)
```python
cars = ['bmw', 'audi', 'toyota', 'subaru', 'honda']
new_cars = cars
cars.append('benz')

print(cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']

print(new_cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']
#此时new_cars 与cars 指向同一个列表
```

## 列表最大值

```max(list)```
```python
list1, list2 = ['123', 'xyz', 'zara', 'abc'], [456, 700, 200]

print "Max value element : ", max(list1);
print "Max value element : ", max(list2);
```
结果为
```python
Max value element :  zara
Max value element :  700
```

## 赋值
全为0或1
```python
a = [1 for _ in range(10)] 
b = [0 for _ in range(10)]

```
