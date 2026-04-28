
# KfcOrderRequestDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parentMerchantNo** | **String** | &lt;p&gt;请求商编&lt;/p&gt; | 
**merchantNo** | **String** | &lt;p&gt;业务商编&lt;/p&gt; | 
**merchantRequestNo** | **String** | &lt;p&gt;商户订单号（与千猪的订单号要相同）&lt;/p&gt; | 
**parentMerchantRequestNo** | **String** | &lt;pre&gt;请求方订单号&lt;/pre&gt; |  [optional]
**supplierChannel** | **String** | &lt;p&gt;采购渠道&lt;/p&gt; | 
**platformIdAccountInfo** | **String** | &lt;pre&gt;供应方平台给采购方分配的秘钥&lt;/pre&gt; &lt;pre&gt;platformId与secret要拼接起来使用aes加密后传递&lt;/pre&gt; &lt;pre&gt;aes key在对接时找易宝技术支持&lt;/pre&gt; &lt;pre&gt;加密方式：&lt;/pre&gt; &lt;pre&gt;platformId&#x3D;123&amp;amp;secret&#x3D;abc 将拼接的字符串直接使用aes加密&lt;/pre&gt; | 
**complateNotifyUrl** | **String** | &lt;pre&gt;订单完成通知地址：订单发货成功、订单取消、订单已完成&lt;/pre&gt; |  [optional]



