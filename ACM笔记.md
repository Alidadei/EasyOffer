

# 输入输出Python

## 多组数据输入

多行输入，每行两个整数

```python
import sys
# 接收输入
for line in sys.stdin:
    a, b = line.split(' ')
    # 输出
    print(int(a) + int(b))
    # 输出换行
    print()
```



第一行为n, 之后输入n行两个整数

```py
while 1:
    try:
        N = int(input())
        for i in range(N):
            l = list(map(int,input().split()))
            print(sum(l))
    except:
        break
        
```

若干行输入，每行输入两个整数，遇到特定条件终止

```python
import sys

while True:
    s = input().split() # 一行一行读取
    a, b = int(s[0]), int(s[1])
    if not a or not b: # 遇到 0, 0 则中断
        break
    print(a + b)
```