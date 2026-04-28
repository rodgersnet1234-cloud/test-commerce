
# QueryCinemaOrderDataBeanDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**totalPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;票总价&lt;/pre&gt; | 
**seatsDesc** | **String** | &lt;pre&gt;seatsDesc&lt;/pre&gt; | 
**cinemaAddr** | **String** | &lt;pre&gt;影院的详细地址&lt;/pre&gt; | 
**canUserCancel** | **Boolean** | &lt;pre&gt;用户能否取消订单&lt;/pre&gt; | 
**language** | **String** | &lt;pre&gt;影片语言&lt;/pre&gt; | 
**versionTypes** | **String** | &lt;pre&gt;影片类型&lt;/pre&gt; | 
**cityId** | **Integer** | &lt;pre&gt;城市id&lt;/pre&gt; | 
**pic** | **String** | &lt;pre&gt;电影海报URL地址&lt;/pre&gt; | 
**marketUnitPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;市场价格&lt;/pre&gt; |  [optional]
**duration** | **Integer** | &lt;pre&gt;播放时长&lt;/pre&gt; | 
**showId** | **Integer** | &lt;pre&gt;场次id&lt;/pre&gt; | 
**coupons** | [**List&lt;QueryCinemaOrderCouponBeanDTO&gt;**](QueryCinemaOrderCouponBeanDTO.md) | &lt;pre&gt;券码数组&lt;/pre&gt; |  [optional]
**cinemaId** | **Integer** | &lt;pre&gt;影院id&lt;/pre&gt; | 
**cinemaName** | **String** | &lt;pre&gt;影院名称&lt;/pre&gt; | 
**showEndTime** | **String** | &lt;pre&gt;场次结束时间&lt;/pre&gt; | 
**unitPrice** | [**BigDecimal**](BigDecimal.md) | &lt;pre&gt;票单价&lt;/pre&gt; | 
**subPlatformId** | **Integer** | &lt;pre&gt;子平台id&lt;/pre&gt; |  [optional]
**orderNo** | **String** | &lt;pre&gt;订单号&lt;/pre&gt; | 
**distanceToShow** | **String** | &lt;pre&gt;距离开场时间&lt;/pre&gt; |  [optional]
**seatsCount** | **Integer** | &lt;pre&gt;座位数量&lt;/pre&gt; | 
**showTime** | **String** | &lt;pre&gt;场次开始时间&lt;/pre&gt; | 
**platformId** | **Integer** | &lt;pre&gt;平台id&lt;/pre&gt; | 
**userName** | **String** | &lt;pre&gt;userName&lt;/pre&gt; | 
**acceptAdjust** | **Boolean** | &lt;pre&gt;是否接受调坐&lt;/pre&gt; |  [optional]
**userId** | **Integer** | &lt;pre&gt;用户id&lt;/pre&gt; | 
**userRemark** | **String** | &lt;pre&gt;用户备注&lt;/pre&gt; |  [optional]
**drawMode** | **Integer** | &lt;pre&gt;0:竞价出票(折扣出票) 5:快速出票(非折扣出票)&lt;/pre&gt; |  [optional]
**regionId** | **Integer** | &lt;pre&gt;区域id&lt;/pre&gt; | 
**hallId** | **Integer** | &lt;pre&gt;影厅id&lt;/pre&gt; | 
**filmId** | **Integer** | &lt;pre&gt;电影id&lt;/pre&gt; | 
**filmName** | **String** | &lt;pre&gt;影片名称&lt;/pre&gt; | 
**cinemaCity** | **String** | &lt;pre&gt;电影的城市&lt;/pre&gt; | 
**hallName** | **String** | &lt;pre&gt;影厅名称&lt;/pre&gt; | 
**platformUniqueId** | **String** | &lt;pre&gt;平台唯一用户标识&lt;/pre&gt; |  [optional]
**commissionPrice** | [**BigDecimal**](BigDecimal.md) | &lt;p&gt;佣金&lt;/p&gt; |  [optional]



