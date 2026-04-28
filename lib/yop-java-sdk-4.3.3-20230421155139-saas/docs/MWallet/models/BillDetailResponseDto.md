
# BillDetailResponseDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** |  |  [optional]
**message** | **String** |  |  [optional]
**createTime** | **String** | &lt;p&gt;订单创建时间&lt;/p&gt; &lt;div data-page-id&#x3D;\&quot;PAIVdmdabo9DDcxbHUWcsiHvn7b\&quot; data-docx-has-block-data&#x3D;\&quot;false\&quot;&gt; &lt;div class&#x3D;\&quot; old-record-id-Gkucd8266oYWk2xKIwfcrH8GnOg\&quot;&gt;（yyyy-MM-dd HH:mm:ss）&lt;/div&gt; &lt;/div&gt; |  [optional]
**requestNo** | **String** | &lt;p&gt;商户请求号&lt;/p&gt; |  [optional]
**uniqueOrderNo** | **String** | &lt;p&gt;易宝唯一订单号&lt;/p&gt; |  [optional]
**orderType** | [**OrderTypeEnum**](#OrderTypeEnum) | &lt;p&gt;订单类型&lt;/p&gt; 可选项如下: WITHDRAW:提现 RECHARGE:充值 PAYMENT:支付 DIVIDE:分账 DIVIDE_REFUND:分账退回 REFUND:退款 PAYMENT_MANAGE:管理费 BONUS:红包  | 
**status** | [**StatusEnum**](#StatusEnum) | &lt;p&gt;订单状态&lt;/p&gt; 可选项如下: PROCESSING:处理中 SUCCESS:成功 FAIL:失败  | 
**payWay** | **String** | &lt;p&gt;交易渠道&lt;/p&gt; |  [optional]
**amount** | **String** | &lt;p&gt;订单金额&lt;/p&gt; &lt;p&gt;（精确到2位小数）&lt;/p&gt; |  [optional]
**fee** | **String** | &lt;p&gt;手续费金额&lt;/p&gt; |  [optional]
**completedTime** | **String** | &lt;p&gt;订单完成时间&lt;/p&gt; |  [optional]
**productName** | **String** | &lt;p&gt;产品名称&lt;/p&gt; |  [optional]
**remark** | **String** | &lt;p&gt;备注信息&lt;/p&gt; |  [optional]


<a name="OrderTypeEnum"></a>
## Enum: OrderTypeEnum
Name | Value
---- | -----
WITHDRAW | &quot;WITHDRAW&quot;
RECHARGE | &quot;RECHARGE&quot;
PAYMENT | &quot;PAYMENT&quot;
DIVIDE | &quot;DIVIDE&quot;
DIVIDE_REFUND | &quot;DIVIDE_REFUND&quot;
REFUND | &quot;REFUND&quot;
PAYMENT_MANAGE | &quot;PAYMENT_MANAGE&quot;
BONUS | &quot;BONUS&quot;


<a name="StatusEnum"></a>
## Enum: StatusEnum
Name | Value
---- | -----
PROCESSING | &quot;PROCESSING&quot;
SUCCESS | &quot;SUCCESS&quot;
FAIL | &quot;FAIL&quot;



