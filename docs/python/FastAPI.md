# 异常

## 1、具体异常类

适用场景，异常非常明确，不会有多种情况导致该异常

```python
class TaskNotExistException(Exception):
    def __init__(self):
        super().__init__("task not find")



if __name__ == '__main__':
    try:
        raise TaskNotExistException()
    except TaskNotExistException as e:
        print(e)
```


## 2、大体异常类

```python
# 在未定义初始化函数时，调用父类的init

class TaskCheckException(Exception):
    pass



if __name__ == '__main__':
    try:
        raise TaskCheckException("任务不存在")
        raise TaskCheckException("任务默字段异常")
        ...
    except TaskNotExistException as e:
        print(e)
```
