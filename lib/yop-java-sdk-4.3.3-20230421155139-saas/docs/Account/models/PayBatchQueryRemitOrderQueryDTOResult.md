
# PayBatchQueryRemitOrderQueryDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requestNo** | **String** | 商户请求号 |  [optional]
**orderNo** | **String** | 易宝流水号 |  [optional]
**merchantNo** | **String** | 商编 |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | 订单金额 |  [optional]
**receiveAmount** | [**BigDecimal**](BigDecimal.md) | 收款金额 |  [optional]
**debitAmount** | [**BigDecimal**](BigDecimal.md) | 扣账金额 |  [optional]
**orderTime** | **String** | 创建时间 |  [optional]
**finishTime** | **String** | 完成时间 |  [optional]
**fee** | [**BigDecimal**](BigDecimal.md) | 手续费 |  [optional]
**feeUndertakerMerchantNo** | **String** | 手续费承担方编号 |  [optional]
**status** | **String** | 付款订单状态 |  [optional]
**failReason** | **String** | 失败或冲退原因 |  [optional]
**receiveType** | **String** | 付款到账类型 |  [optional]
**receiverAccountNo** | **String** | 收款方账号 |  [optional]
**receiverAccountName** | **String** | 收款方开户名 |  [optional]
**receiverBankCode** | **String** | 收款方银行编码 |  [optional]
**comments** | **String** | 银行附言 |  [optional]
**isReversed** | **Boolean** | 冲退标识 |  [optional]
**reverseTime** | **String** | 冲退时间 |  [optional]
**batchNo** | **String** | 批次号 |  [optional]
**cancelReason** | **String** | 撤销原因 |  [optional]



