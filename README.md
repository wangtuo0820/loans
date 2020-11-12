## 开始
用面积堆叠图比较直观的显示 等额本息和等额本金的区别
```
    基础信息：
    贷款期限 30 年 
    等额本息： 需要每月还5368.22, 还款总额为 1932559.2000000002；
    等额本金： 需要第一月还6944.44 每月递减 11.57， 还款总额为 1752345.00。
    利滚利定投：
    投资利率 5%
    等额本息 去掉 等额本金后期投资(机会成本) 共赚取 180669.0900000002 定投利息；
    等额本金比等额本息少交利息 180214.20；
    个人总收益  454.89
```

## Available Scripts

In the project directory, you can run:

### `yarn start`


### `yarn test`

Launches the test runner in the interactive watch mode.<br />

### `yarn build`

## 计算方法
1. 总额 a
2. 月利息 r （ 贷款利率/12）
3. 期数 n （年限*12） 
### 等额本金
 月还款：
   第1月 a / n + a * r
   第2月 a / n + a * （n-1）/ n * r
   ...
   第n月 a/n + a / n * r

### 等额本息
 假设月还款 为 X
 则每月剩余金额:
 初始 a0 = a
 第1个月 a1 = a0 * （1+r） - X
 第2个月  a2 = a1 * （1+r） - X 
 第3个月  a3 = a2 * （1+r） - X
 ...
 第n个月  a_n = a_n-1 * （1+r） - X = 0

 X = a(1+r)^n*r / ((1+r)^n - 1)
 
 B站看到的，视频原地址 https://www.bilibili.com/video/BV1GA411E7Pm?from=search&seid=6358258909542788281
 
 UP主的公网IP http://118.126.115.169
