
# UpopActivescanQuerypayresultOpenQueryActiveScanPayResultResponseDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | 错误码 |  [optional]
**message** | **String** | 错误码描述 |  [optional]
**origCode** | **String** | 失败错误码 |  [optional]
**origMessage** | **String** | 失败错误描述 |  [optional]
**payOrderNo** | **String** | 付款订单号 |  [optional]
**realTradeAmount** | [**BigDecimal**](BigDecimal.md) | 实际付款金额 |  [optional]
**totalRefundAmount** | [**BigDecimal**](BigDecimal.md) | 总退款金额 |  [optional]
**payeeMerchantId** | **String** | 收款商户号 |  [optional]
**payeeMerchantName** | **String** | 收款商户名称 |  [optional]
**payeeMCC** | **String** | 收款方MCC |  [optional]
**status** | **String** | 订单状态 |  [optional]
**couponInfo** | **String** | 营销信息 |  [optional]
**origTxnAmt** | [**BigDecimal**](BigDecimal.md) | 初始交易金额（原订单金额） |  [optional]
**totalRefundOrigTxnAmt** | [**BigDecimal**](BigDecimal.md) | 申请退款总金额 |  [optional]
**refundTradeDetailList** | [**List&lt;UpopActivescanQuerypayresultRefundTradeDetailResponseDTOResult&gt;**](UpopActivescanQuerypayresultRefundTradeDetailResponseDTOResult.md) | 退款明细列表 |  [optional]



