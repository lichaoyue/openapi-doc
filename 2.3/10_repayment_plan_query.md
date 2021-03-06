#还款计划查询
## 描述
贷款发放后，平台方按照合同号和合同号查询从当前日期后的还款计划（单次最多50条）
## API代码
loan\_app:repayment\_plan:query

## 请求参数
| 名称 | 类型 | 是否必须 | 描述 | 示例值 |
| --- | --- | --- | --- | --- |
| contractNo | String | 是 | 合同编号 |  |
| acctNo | String | 是 | 贷款账号 |  ||

## 响应参数
| 名称 | 类型 | 描述 |示例值 |
| --- | --- | --- | --- |
| termNo | Number | 期数 | |  
| dtRepay | Date | 还款日期 |  |
| repayAmt | Number | 还款本金金额 | |  
| repayInterestAmt | Number | 还款利息金额 | |  
| feeAmt | Number | 管理费金额 | |  |

## 错误码
| 描述 | HTTP状态码 | 语义 |
| --- | --- | --- | 
| acctNo未找到 | 400 | 请输入正确的贷款账号,或检查贷款账号与合同号是否匹配 |

## 示例
### 请求示例
```javascript
{
    "acctNo":"82700156225596267",
    "contractNo":"LJT2017051011000001"
}
```
### 返回示例
```javascript
{
    "termNo":"1",
    "dtRepay":"2017-01-05",
    "repayAmt":"1000.32"
}
```
## FAQ
关于此文档暂时还没有FAQ