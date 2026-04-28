
# RefundQueryQueryRefundResponseDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | 返回码 |  [optional]
**message** | **String** | 返回信息 |  [optional]
**parentMerchantNo** | **String** | 发起方商编 |  [optional]
**merchantNo** | **String** | 商户编号 |  [optional]
**orderId** | **String** | 商户收款请求号 |  [optional]
**refundRequestId** | **String** | 商户退款请求号 |  [optional]
**uniqueOrderNo** | **String** | 易宝收款订单号 |  [optional]
**uniqueRefundNo** | **String** | 易宝退款订单号 |  [optional]
**refundAmount** | [**BigDecimal**](BigDecimal.md) | 退款申请金额 |  [optional]
**returnMerchantFee** | [**BigDecimal**](BigDecimal.md) | 退回商户手续费 |  [optional]
**status** | **String** | 退款状态 |  [optional]
**description** | **String** | 退款原因 |  [optional]
**refundRequestDate** | **String** | 退款受理时间 |  [optional]
**refundSuccessDate** | **String** | 退款成功日期 |  [optional]
**failReason** | **String** | 退款失败原因 |  [optional]
**realRefundAmount** | [**BigDecimal**](BigDecimal.md) | 实际退款金额 |  [optional]
**cashRefundFee** | [**BigDecimal**](BigDecimal.md) | 用户实退金额 |  [optional]
**bankPromotionInfoDTOList** | [**List&lt;RefundQueryBankPromotionInfoDTOResult&gt;**](RefundQueryBankPromotionInfoDTOResult.md) | 渠道侧优惠退回列表 |  [optional]
**ypPromotionInfoDTOList** | [**List&lt;RefundQueryYpPromotionRefundInfoDTOResult&gt;**](RefundQueryYpPromotionRefundInfoDTOResult.md) | 易宝侧优惠退回列表 |  [optional]
**refundAccountDetail** | **String** | 退款资金来源信息 |  [optional]
**channelReceiverInfo** | **String** | 退款入账信息 |  [optional]



