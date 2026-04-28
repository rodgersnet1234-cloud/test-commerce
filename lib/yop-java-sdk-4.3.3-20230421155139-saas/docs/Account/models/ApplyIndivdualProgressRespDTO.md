
# ApplyIndivdualProgressRespDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**returnCode** | **String** | &lt;p&gt;返回码，响应成功时返回UA00000&lt;/p&gt; | 
**returnMsg** | **String** | &lt;p&gt;返回信息&lt;/p&gt; |  [optional]
**id** | **Long** | &lt;p&gt;收款方id&lt;/p&gt; |  [optional]
**finishTime** | [**DateTime**](DateTime.md) | &lt;p&gt;完成时间&lt;/p&gt; |  [optional]
**applicationStatus** | [**ApplicationStatusEnum**](#ApplicationStatusEnum) | &lt;p&gt;申请状态&lt;/p&gt; 可选项如下: SUCCESS:成功 REJECT:失败 RECEIVE:处理中  |  [optional]
**failReason** | **String** | &lt;p&gt;失败原因&lt;/p&gt; |  [optional]
**requestNo** | **String** | &lt;p&gt;商户请求号&lt;/p&gt; |  [optional]
**applyTime** | [**DateTime**](DateTime.md) | &lt;p&gt;申请时间&lt;/p&gt; |  [optional]
**merchantNo** | **String** | &lt;p&gt;商户编号&lt;/p&gt; |  [optional]


<a name="ApplicationStatusEnum"></a>
## Enum: ApplicationStatusEnum
Name | Value
---- | -----
SUCCESS | &quot;SUCCESS&quot;
REJECT | &quot;REJECT&quot;
RECEIVE | &quot;RECEIVE&quot;



