
# SubscribeNotifyRequestDTO

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**merchantNo** | **String** | &lt;p&gt;商户编号（通知会员的归属商编）&lt;/p&gt; | 
**requestNo** | **String** | &lt;p&gt;商户请求号&lt;/p&gt; | 
**notifyUrl** | **String** | &lt;p&gt;通知商户地址&lt;/p&gt; |  [optional]
**memberList** | [**List&lt;MemberSubscribeNotifyInfo&gt;**](MemberSubscribeNotifyInfo.md) | &lt;p&gt;会员列表&lt;/p&gt; | 
**notifyType** | [**NotifyTypeEnum**](#NotifyTypeEnum) | &lt;p&gt;变更通知类型&lt;/p&gt; 可选项如下: ENABLE:会员续期有效 EXPIRE:会员订阅到期  | 
**operateTime** | **String** | &lt;p&gt;变更时间&lt;/p&gt; | 


<a name="NotifyTypeEnum"></a>
## Enum: NotifyTypeEnum
Name | Value
---- | -----
ENABLE | &quot;ENABLE&quot;
EXPIRE | &quot;EXPIRE&quot;



