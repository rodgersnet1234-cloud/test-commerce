
# PayQueryRemitOrderQueryRespDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**returnCode** | **String** | 返回码 |  [optional]
**returnMsg** | **String** | 返回信息 |  [optional]
**requestNo** | **String** | 商户请求号 |  [optional]
**orderNo** | **String** | 易宝付款订单号 |  [optional]
**merchantNo** | **String** | 商户编号 |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | 付款金额 |  [optional]
**receiveAmount** | [**BigDecimal**](BigDecimal.md) | 到账金额 |  [optional]
**debitAmount** | [**BigDecimal**](BigDecimal.md) | 扣账金额 |  [optional]
**orderTime** | **String** | 付款下单时间 |  [optional]
**finishTime** | **String** | 付款完成时间 |  [optional]
**fee** | [**BigDecimal**](BigDecimal.md) | 手续费 |  [optional]
**feeUndertakerMerchantNo** | **String** | 手续费承担方商编 |  [optional]
**status** | **String** | 订单状态 |  [optional]
**failReason** | **String** | 失败原因 |  [optional]
**receiveType** | **String** | 到账类型 |  [optional]
**receiverAccountNo** | **String** | 收款方银行账号 |  [optional]
**receiverAccountName** | **String** | 收款方开户名 |  [optional]
**receiverBankCode** | **String** | 收款方开户行编码 |  [optional]
**comments** | **String** | 银行附言 |  [optional]
**isReversed** | **Boolean** | 冲退标识 |  [optional]
**reverseTime** | **String** | 冲退时间 |  [optional]



