
# OrderQueryYopQueryOrderResDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | 返回码 |  [optional]
**message** | **String** | 返回信息 |  [optional]
**parentMerchantNo** | **String** | 发起方商编 |  [optional]
**merchantNo** | **String** | 商户编号 |  [optional]
**orderId** | **String** | 商户收款请求号 |  [optional]
**uniqueOrderNo** | **String** | 易宝收款订单号 |  [optional]
**status** | **String** | 订单状态 |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | 订单金额 |  [optional]
**payAmount** | [**BigDecimal**](BigDecimal.md) | 支付金额 |  [optional]
**merchantFee** | [**BigDecimal**](BigDecimal.md) | 商户手续费 |  [optional]
**customerFee** | [**BigDecimal**](BigDecimal.md) | 用户手续费 |  [optional]
**paySuccessDate** | **String** | 支付成功时间 |  [optional]
**memo** | **String** | 对账备注 |  [optional]
**payWay** | **String** | 支付方式 |  [optional]
**token** | **String** | token |  [optional]
**fundProcessType** | **String** | 分账都订单标识 |  [optional]
**bankOrderId** | **String** | 银行订单号 |  [optional]
**channelOrderId** | **String** | 渠道订单号 |  [optional]
**channel** | **String** | 渠道类型 |  [optional]
**realPayAmount** | [**BigDecimal**](BigDecimal.md) | 用户实际支付金额 |  [optional]
**unSplitAmount** | [**BigDecimal**](BigDecimal.md) | 剩余可分账金额 |  [optional]
**totalRefundAmount** | [**BigDecimal**](BigDecimal.md) | 未命名 |  [optional]
**payerInfo** | [**OrderQueryPayerInfoResult**](OrderQueryPayerInfoResult.md) | 付款信息 |  [optional]
**channelPromotionInfo** | [**List&lt;OrderQueryChannelPromotionInfoDTOResult&gt;**](OrderQueryChannelPromotionInfoDTOResult.md) | 渠道侧优惠列表 |  [optional]
**ypPromotionInfo** | [**List&lt;OrderQueryYpPromotionInfoDTOResult&gt;**](OrderQueryYpPromotionInfoDTOResult.md) | 易宝优惠列表 |  [optional]
**terminalInfo** | **String** | 终端信息 |  [optional]
**installmentInfo** | [**OrderQueryInstallmentInfoResult**](OrderQueryInstallmentInfoResult.md) | 信用卡分期信息 |  [optional]
**failReason** | **String** | 支付失败的失败原因 |  [optional]
**failCode** | **String** | 支付失败的code码 |  [optional]



