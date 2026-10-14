# Day 5 + Day 6：while、input、字典与函数

> 覆盖时间：10/14 – 10/15 凌晨

## 第一部分：while 循环与死循环

### 学到的
- while：条件成立就一直转（for 管"次数已知"，while 管"条件说了算"）
- 循环体里必须有"让条件变化"的代码（`count = count + 1` 是刹车）
- 死循环：亲眼见过（`1` 无限刷屏）+ `Ctrl + C` 急停
- `KeyboardInterrupt`：不是报错，是"被叫停"的痕迹

## 第二部分：input 与交互循环

### 学到的
- `input()`：程序暂停等待、接住输入——第一次"程序等人类说话"
- **input 接到的永远是字符串**——要计算就得 `int()` 转换
- 拼接型 TypeError 重逢 → 自己动手修复（`int(num) + 1`）
- `ValueError`：输入非数字时 `int("你好")` 的报错——"用户输入不可信"
- `while True` + `break`：交互循环骨架（输入 exit 退出）

## 第三部分：字典

### 学到的
- 字典：键值对（"名字当钥匙"）；`{}` 花括号；"查字典"式查找
- 取值 `device["name"]`；**改 / 增是同一种写法**（钥匙存在=改，不存在=增）
- 键的规则：必须"钉得死"（文字、数字可以；列表不行）
- `in` 运算符：探路保险——用于防 KeyError
- `KeyError`：字典找不到钥匙
- 总纪律：**结构听语言的（半角、逗号、冒号），内容听你的**

### 产出
- `device_query.py`：设备信息查询脚本（字典 + while True + input + if/break + in + str()）
- 手打暴露真实盲区：字典缺逗号 → SyntaxError

## 第四部分：函数

### 学到的
- 定义与调用：`def` 定义 ≠ 执行——带括号调用才干活
- 参数：`def greet(name)`——"占位盒子"接不同的原料
- **return 第一职责：交还结果**（能落进变量、继续参与计算：8 → 108）
- **return 第二职责：立即退场**（执行到它，函数当场结束，后面全部跳过）
- print vs return："喊出来" ≠ "交出去"（print 版调用处接到 None）
- 多条 return：每次调用只执行"第一条到达的"
- 参数数量对不上会报 TypeError（缺 / 多两个方向都试过）

### 产出
- `day6_func.py`：五组实验（定义 / 参数 / return / 接不住 / 提前结束）

## 报错家族（累计 7 位成员）
NameError / TypeError / SyntaxError / IndentationError / IndexError / ValueError / KeyError
（另有 KeyboardInterrupt：不是错误，是按下 Ctrl+C 叫停的痕迹）

## 补课清账（4 项）
- `and` / `or` / `not`（组合条件）
- `%`（取模：算余数、判奇偶）
- 列表按索引修改（`devices[1] = 新值`）
- E02 对比实验（条件不成立 → 归 if 管的行全部消失）

## 下一篇
- 文件读写：open / 读 / 写 / 逐行（进行中）
