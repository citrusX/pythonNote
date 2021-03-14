# 列表
字面意思就是一个集合，在Python中List中的元素用中括号[ ]来表示，可以这样定义一个List:
```
L = [12, 'China', 19.998]
```
可以看到并不要求元素的类型都是一样的。当然也可以定义一个空的。

```
print(L)
len(L)

[12, 'China', 19.998]
3
```

## 修改，添加，删除元素

### 修改元素
```
L[0] = 15

[15, 'China', 19.998]
```
### 添加元素
1. 在列表末尾添加元素
```
L.append('honda')

[15, 'China', 19.998, 'honda']
```
2. 在列表中插入元素
```
L.insert(0, 'yamaha')

['yamaha', 15, 'China', 19.998, 'honda']
```
### 删除元素
1. 使用```del(index)```语句
标注位置
```
L.del(0)

[15, 'China', 19.998, 'honda']
```
2. 使用```pop()```
删除末尾元素并可使用
```
pop_element = L.pop()
print(L)

[15, 'China', 19.998]

print(pop_element)
honda
```
3. 弹出任何位置元素
```pop(index)```
```
pop_element = L.pop(0)
print(L)

['China', 19.998]


print(pop_element)
15
```
4. 根据值删除元素
```remove(value)```
```
L = ['yamaha', 15, 'China', 19.998, 'honda']
L.remove(15)


['yamaha', 'China', 19.998, 'honda']
```

### 组织列表
1. 使用```sort()``` 进行永久性排序
```
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
print(cars)

['audi', 'bmw', 'subaru', 'toyota']

cars.sort(reverse = True)
print(cars)

['toyota', 'subaru', 'bmw', 'audi']
```
2. 使用```sorted()``` 进行临时排序
```
cars = ['bmw', 'audi', 'toyota', 'subaru']

print(sorted(cars))
['audi', 'bmw', 'subaru', 'toyota']


print(cars)
['bmw', 'audi', 'toyota', 'subaru']
```
3. 反转打印```reverse()```

将原列表顺序反转而不是排序
```
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.reverse()
print(cars)

['subaru', 'toyota', 'audi', 'bmw']
```


## 列表切片
取头不取尾
```
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

### 复制列表
1. 创建列表的副本
```
cars = ['bmw', 'audi', 'toyota', 'subaru', 'honda']
new_cars = cars[:]
cars.append('benz')

print(cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']

print(new_cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda']
```

2. 指向同一个列表(复制失败)
```
cars = ['bmw', 'audi', 'toyota', 'subaru', 'honda']
new_cars = cars
cars.append('benz')

print(cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']

print(new_cars)
['bmw', 'audi', 'toyota', 'subaru', 'honda', 'benz']
#此时new_cars 与cars 指向同一个列表
```