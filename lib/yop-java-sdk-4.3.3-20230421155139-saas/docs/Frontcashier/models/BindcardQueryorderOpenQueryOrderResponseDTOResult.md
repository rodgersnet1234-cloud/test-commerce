
# BindcardQueryorderOpenQueryOrderResponseDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | 返回码 |  [optional]
**message** | **String** | 返回描述 |  [optional]
**merchantNo** | **String** | 收单商户编号 |  [optional]
**merchantFlowId** | **String** | 商户签约/绑卡请求号 |  [optional]
**nopOrderId** | **String** | 易宝订单号 |  [optional]
**orderStatus** | **String** | 订单状态 |  [optional]
**signStatus** | **String** | 银行签约状态 |  [optional]
**userNo** | **String** | 用户标识 |  [optional]
**userType** | **String** | 用户标识类型 |  [optional]
**entrustProtocolId** | **String** | 商业委托协议ID，仅商业委托返回 |  [optional]
**collectAmount** | [**BigDecimal**](BigDecimal.md) | 代收金额，仅商业委托返回 |  [optional]
**collectBeginDate** | **String** | 代收开始时间，仅商业委托返回 |  [optional]
**collectEndDate** | **String** | 代收结束时间，仅商业委托返回 |  [optional]
**cycleFrequency** | **Integer** | 代收频次，仅商业委托返回 |  [optional]
**cycleStep** | **Integer** | 代收步长，仅商业委托返回 |  [optional]
**cycleStepUnit** | **String** | 代收周期单位，仅商业委托返回 |  [optional]
**submitMethod** | **String** | 跳页签约提交方式，仅跳页签约返回 |  [optional]
**submitUrl** | **String** | 跳页签约url，仅跳页签约返回 |  [optional]
**encoding** | **String** | 跳页页面编码，仅跳页签约返回 |  [optional]
**bankCardNo** | **String** | 银行卡号 |  [optional]
**userName** | **String** | 姓名 |  [optional]
**idCardNo** | **String** | 证件号 |  [optional]
**idCardType** | **String** | 证件类型 |  [optional]
**phone** | **String** | 银行预留手机号 |  [optional]
**bankCode** | **String** | 银行编码 |  [optional]
**signSuccessNotifyUrl** | **String** | 跳页签约回调地址，仅跳页签约返回 |  [optional]
**bindId** | **String** | 签约/绑卡ID |  [optional]



