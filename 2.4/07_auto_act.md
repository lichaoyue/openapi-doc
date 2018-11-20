#授信自动审批接口
## 描述
将授信数据通过接口实现自动审批功能,省去人工审批（暂时只支持个贷）<br/>
例如：授信申请创建之后，并填写完所有的必填信息。然后调用自动审批API将会把授信申请自动提交推送到外部机构中（担保方或资金方）中

## 示例代码
具体方法详见<a href="https://codeload.github.com/lianjintai/openapi-demo-java/zip/master" target="_blank">接口demo下载</a>授信自动审批demo,包路径[com.ljt.openapi.demo.demos.LoanAppAutoActDemo]。


## API代码
loan_app:app:auto_act

## 请求参数
| 名称 | 类型 | 是否必须 | 描述 | 示例值 |
| --- | --- | --- | --- | --- |
| appID | String | 是 | 申请ID | c4d6f8cfabc547539c2ae4fb49130aff |




## 响应参数
| 名称 | 类型 | 描述 |示例值 |
| --- | --- | --- | --- |
| appID | String | 申请ID | c4d6f8cfabc547539c2ae4fb49130aff |
 

## 错误码

## 请求参数示例
### 请求示例
```javascript
{
    "appID": "c4d6f8cfabc547539c2ae4fb49130aff" 
}
```
## 返回示例
```javascript
{
   "appID": "c4d6f8cfabc547539c2ae4fb49130aff"
}
```
## FAQ
1、怎么样才能触发自动审批
>1、产品需要配置开启自动审批<br/>
>2、授信申请需要填写完业务要求的所有的信息（[个贷产品配置](01_cs_fac_config.md)返回配置中所有必填信息，包括“客户信息”、“关联人”、“申请材料”、“业务”）

2、调用自动审批之后，但授信申请没有提交到下一个审批人
>1、检查授信申请详情页面tab页面“错误信息”中的错误提示<br/>
>2、此授信申请的申请人，已有申请在审批处理中。（可手动提交审批确认具体原因）

3、调用自动审批之后，但授信申请没有推送到“担保方”或者“资金方”
>1、授信申请的业务是否已配置推送关系（可推送的担保方或资金方）<br/>
>2、授信申请的申请人是否已有推送到“担保方”或“资金方”的授信申请