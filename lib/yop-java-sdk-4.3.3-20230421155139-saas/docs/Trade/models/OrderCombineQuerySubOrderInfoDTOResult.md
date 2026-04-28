
# OrderCombineQuerySubOrderInfoDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**merchantNo** | **String** | 商户编号 |  [optional]
**orderId** | **String** | 商户收款请求号 |  [optional]
**uniqueOrderNo** | **String** | 易宝收款订单号 |  [optional]
**bankOrderId** | **String** | 银行订单号 |  [optional]
**channelOrderId** | **String** | 渠道订单号 |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | 订单金额 |  [optional]
**payAmount** | [**BigDecimal**](BigDecimal.md) | 支付金额 |  [optional]
**unSplitAmount** | [**BigDecimal**](BigDecimal.md) | 剩余可分账金额 |  [optional]
**goodsName** | **String** | 商品描述 |  [optional]
**merchantFee** | [**BigDecimal**](BigDecimal.md) | 商户手续费 |  [optional]
**customerFee** | [**BigDecimal**](BigDecimal.md) | 用户手续费 |  [optional]
**memo** | **String** | 对账备注 |  [optional]
**status** | **String** | 订单状态 |  [optional]
**payWay** | **String** | 支付方式 |  [optional]
**paySuccessDate** | **String** | 支付成功时间 |  [optional]
**fundProcessType** | **String** | 分账标识 |  [optional]
**channel** | **String** | 渠道类型 |  [optional]
**ypPromotionInfo** | [**List&lt;OrderCombineQueryYpPromotionInfoDTOResult&gt;**](OrderCombineQueryYpPromotionInfoDTOResult.md) | 未命名 |  [optional]



