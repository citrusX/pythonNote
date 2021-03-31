# 元组
Tuple可以看做是一种“不变”的List，访问也是通过下标，用小括号（）表示：
```python
dimensions(200, 50)
```
但是不能重新赋值替换,也没有```pop()```和```insert()```、```append()```方法。
若要修改需要重新定义元组
```python
dimensions(200, 50)

dimensions(400, 100)

```