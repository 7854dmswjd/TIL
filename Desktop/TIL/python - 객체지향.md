# python - 객체지향

## 1. Class

#### - Class and Method

```python
class Person:    # Class 이름은 대문자로 시작
  def greeting(self): #greeting이라는 메소드
    print('Hello')
    
# 인스턴스를 만들어야  클래스를 사용할 수 있다.
james = Person()
maria = Person()
james.greeting()
```

```Hello```

#### - 속성(Attribute)

```python
class Person:
  def __init__(self):
    self.hello = '안녕하세요'   # hello 속성값을 갖게 됨
  
  def greeting(self):
    print(self.hello)
```



####  - 비공개 속성

```python
class Person:
  def __init__(self, name, age, addr, wallet):
    self.name = name
    self.age  = age
    self.addr = addr
    self.__wallet = wallet   
    #  비공개 속성 __wallet 속성은 비공개
```



##  2. 정적 메서드

#### - 인스턴스 X, self X :  @staticmethod

```python
class Calc:
    @staticmethod    
    # 정적 메서드는 매개변수에 self를 지정하지 않습니다.
    def add(a, b):
        print(a + b)
 
    @staticmethod
    def mul(a, b):
        print(a * b)
 
Calc.add(10, 20)    # 클래스에서 바로 메서드 호출
Calc.mul(10, 20)    # 클래스에서 바로 메서드 호출
```



## 3. 클래스 메서드

#### -인스턴스 X, cls O :  @classmethod

```python
class Person:
    count = 0    # 클래스 속성
 
    def __init__(self):
        Person.count += 1    # 인스턴스가 만들어질 때
                             # 클래스 속성 count에 1을 더함
 
    @classmethod
    def print_count(cls):
        print('{0}명 생성되었습니다.'.format(cls.count))    # cls로 클래스 속성에 접근
 
james = Person()
maria = Person()
 
Person.print_count()    # 2명 생성되었습니다.
```

