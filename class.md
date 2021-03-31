# 创建类

Dog.py
```python
class Dog():
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
    def sit(self):
        print(self.name.title() + "is sitting.")
        
    def roll_over(self):
        print(self.name.title() + "rolled over.")

```
创建类时
```python
my_dog = Dog('willie', 6)
```

---
*java中创建类*
```java
public class Person{
    private String name;
    private int age;
    
    public Person(String name,int age){  
        this.name=name;
        this.age=age;
    }

    public void setName(String name){
        this.name=name;
    }
    public void setAge(int age){
        this.age=age;
    }
}
```
创建实例
```java
public class Tom{
    public static void main(String[] args) {
        Person pe=new Person("Tom",16);
    }
}

```
---

# 从父类继承
1. 父类在当前文件中且位于子类之前
2. 使用```super().__init__()``` 从父类中继承。
3. 可在子类中重写父类中同名方法。

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def get_descip(self):
        long_name = str(self.year) + ' ' + self.make + ' ' + self.model
        return long_name.title()


class ElectricCar(Car):
    def __init__(self, make, model, year):
        super().__init__(make, model, year)
        self.battery_size = 70

    def describe_battery(self):
        print("the battery size is " + str(self.battery_size))


my_tesla = ElectricCar('tesla', 'model s', 2016)
print(my_tesla.get_descip())
my_tesla.describe_battery()
```

# 导入类
1. 导入单个或多个类
```python
from 文件名 import 类名

from car import Car
from car import ElectricCar

from car import Car, ElectricCar
```

2. 导入整个模块
```python
import 文件名

import car
```

# self 的功能
**<font size=5><font color=Orange>self代表类的实例，而非类。</font></font>**

一旦产生了一个实例，那么self就会一直是传入的那个实例。这样也保证了即使生成多个新的实例，也不会把原来的实例和新的实例弄乱了。