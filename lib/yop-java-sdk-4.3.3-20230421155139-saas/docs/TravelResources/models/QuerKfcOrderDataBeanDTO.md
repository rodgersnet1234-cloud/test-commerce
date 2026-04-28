
# QuerKfcOrderDataBeanDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**totalPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;总价（元）&lt;/pre&gt; | 
**marketUnitPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;市场价（元）&lt;/pre&gt; | 
**refundPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;退款金额（元）&lt;/pre&gt; |  [optional]
**kfcPlaceOrder** | [**QueryKfcPlaceOrderBean**](QueryKfcPlaceOrderBean.md) |  |  [optional]
**unitPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;单价(元)&lt;/pre&gt; | 
**orderNo** | **String** | &lt;pre&gt;订单号&lt;/pre&gt; | 
**quantity** | **Integer** | &lt;pre&gt;数量&lt;/pre&gt; | 
**ticket** | **String** | &lt;pre&gt;取餐码&lt;/pre&gt; | 
**commissionPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;佣金（元），此字段在交易完成时才会有值&lt;/pre&gt; |  [optional]
**userId** | **Integer** | &lt;pre&gt;用户id&lt;/pre&gt; | 
**userRemark** | **String** | &lt;pre&gt;用户备注&lt;/pre&gt; |  [optional]
**userMobile** | **String** | &lt;pre&gt;用户手机号码&lt;/pre&gt; |  [optional]
**cancelTime** | **String** | &lt;pre&gt;取消时间&lt;/pre&gt; |  [optional]
**userName** | **String** | &lt;pre&gt;用户昵称&lt;/pre&gt; |  [optional]
**kfcOrderMobileSuffix** | **String** | &lt;pre&gt;下单手机后4位（非用户手机号）&lt;/pre&gt; |  [optional]
**kfcOrderMobileRemark** | **String** | &lt;pre&gt;下单手机备注&lt;/pre&gt; |  [optional]
**platformUniqueId** | **String** | &lt;pre&gt;平台用户唯一标识&lt;/pre&gt; |  [optional]
**takeout** | **Boolean** | &lt;pre&gt;是否外卖&lt;/pre&gt; |  [optional]
**takeoutPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;外送费(元)）&lt;/pre&gt; |  [optional]
**takeoutProvinceName** | **String** | &lt;pre&gt;外卖省份名称&lt;/pre&gt; |  [optional]
**takeoutProvinceCode** | **String** | &lt;pre&gt;外卖省份编号&lt;/pre&gt; |  [optional]
**takeoutCityName** | **String** | &lt;pre&gt;外卖城市名称&lt;/pre&gt; |  [optional]
**takeoutCityCode** | **String** | &lt;pre&gt;外卖城市编号&lt;/pre&gt; |  [optional]
**takeoutRegionName** | **String** | &lt;pre&gt;外卖区域名称&lt;/pre&gt; |  [optional]
**takeoutRegionCode** | **String** | &lt;pre&gt;外卖区域编号&lt;/pre&gt; |  [optional]
**takeoutMainAddress** | **String** | &lt;pre&gt;外卖主要地址&lt;/pre&gt; |  [optional]
**takeoutDetailAddress** | **String** | &lt;pre&gt;外卖详细地址&lt;/pre&gt; |  [optional]
**takeoutLon** | **String** | &lt;pre&gt;外卖地址经度&lt;/pre&gt; |  [optional]
**takeoutLat** | **String** | &lt;pre&gt;外卖地址纬度&lt;/pre&gt; |  [optional]
**takeoutDeliveryTime** | **String** | &lt;pre&gt;外卖预计送达时间&lt;/pre&gt; |  [optional]



