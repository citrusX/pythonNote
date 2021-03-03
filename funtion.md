# 传递实参
```
def describe_pet(animaltype, animalname):
    """宠物信息"""
    print("I have a " + animaltype + "." )
    print("The name is "+ animalname.title() + ".")
    ##   .title() 返回"标题化"的字符串,所有单词都是以大写开始，其余字母均为小写
```
## 位置实参

```
#按照顺序传入参数
describe_pet(dog, willie)
```
## 关键字实参
```
#顺序不重要
describe_pet(animalname = 'willie', animaltype = 'dog')
```
## 默认值
```
def describe_pet(animaltype = 'dog', animalname):
     """宠物信息"""
    print("I have a " + animaltype + "." )
    print("The name is "+ animalname.title() + ".")
```
调用时
```
describe_pet('willie')
#输出 dog willie

describe_pet(animaltype = 'cat', animalname = 'harry')
#输出 cat harry
```

# 返回值
## 让实参变为可选值
```
def describe_pet(animaltype, animalname, animalage=''):
    if animalage:
        animaldata = animaltype +': '+ animalname + ', '+ animalage +' years old.'
    else:
        animaldata = animaltype + ': ' + animalname + '. No age details.'
    return animaldata  
```
输出为
```
print(describe_pet("dog", "willie"))
dog: willie. No age details.

print(describe_pet("cat", "harry", "2"))
cat: harry, 2 years old.
```

# 传递任意数量的实参
```
def make_pizza(*toppings):
    print(toppings)

make_pizza('mushroom', 'green pepper', 'onion')
```
输出为
```
('mushroom', 'green pepper', 'onion')
```