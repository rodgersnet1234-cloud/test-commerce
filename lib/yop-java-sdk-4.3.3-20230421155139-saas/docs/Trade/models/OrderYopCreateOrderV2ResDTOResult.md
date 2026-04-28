
# OrderYopCreateOrderV2ResDTOResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | 返回码 |  [optional]
**message** | **String** | 返回信息 |  [optional]
**parentMerchantNo** | **String** | 发起方商编 |  [optional]
**merchantNo** | **String** | 商户编号 |  [optional]
**orderId** | **String** | 商户收款请求号 |  [optional]
**uniqueOrderNo** | **String** | 易宝收款订单号 |  [optional]
**token** | **String** | 支付授权token |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | 订单金额 |  [optional]
**subOrderInfoList** | [**List&lt;OrderYopSubOrderDetailDTOResult&gt;**](OrderYopSubOrderDetailDTOResult.md) | 子单域信息 |  [optional]



