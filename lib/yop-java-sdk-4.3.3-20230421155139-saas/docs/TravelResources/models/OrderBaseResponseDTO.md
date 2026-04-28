
# OrderBaseResponseDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | &lt;p&gt;代表本次请求成功，订单状态需要关注orderStatus&lt;/p&gt; |  [optional]
**orderStatus** | **String** | &lt;pre&gt;订单状态:&lt;/pre&gt; | 
**supplierChannel** | **String** | &lt;pre&gt;供应商渠道&lt;/pre&gt; | 
**message** | **String** |  |  [optional]
**paymentUniqueOrderNo** | **String** | &lt;pre&gt;支付请求流水号&lt;/pre&gt; |  [optional]
**orderAmount** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;订单金额&lt;/pre&gt; | 
**complateTime** | **String** | &lt;pre&gt;完成时间。订单出货成功时返回&lt;/pre&gt; |  [optional]
**cancelTime** | **String** | &lt;p&gt;订单取消时返回，取消时间&lt;/p&gt; |  [optional]
**orderSuccessTime** | **String** | &lt;pre&gt;下单成功时间。下单成功时返回&lt;/pre&gt; |  [optional]
**systemOrderNo** | **String** | &lt;pre&gt;系统返回唯一订单号&lt;/pre&gt; | 
**paySuccessTime** | **String** | &lt;pre&gt;支付成功时间。支付成功时返回&lt;/pre&gt; | 
**parentMerchantNo** | **String** | &lt;p&gt;请求商编&lt;/p&gt; | 
**merchantNo** | **String** | &lt;p&gt;业务商编&lt;/p&gt; | 
**merchantRequestNo** | **String** | &lt;p&gt;商户订单号&lt;/p&gt; | 
**parentMerchantRequestNo** | **String** | &lt;pre&gt;请求方订单号&lt;/pre&gt; |  [optional]
**supplierOrderNo** | **String** | &lt;pre&gt;资源方订单号&lt;/pre&gt; |  [optional]



