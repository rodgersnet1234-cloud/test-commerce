
# BillListDetailDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orderType** | [**OrderTypeEnum**](#OrderTypeEnum) | &lt;p&gt;订单类型&lt;/p&gt; 可选项如下: WITHDRAW:提现 RECHARGE:充值 PAYMENT:支付 DIVIDE:分账 DIVIDE_REFUND:分账退回 REFUND:退款 PAYMENT_MANAGE:管理费 BONUS:红包  | 
**amount** | **String** | &lt;p&gt;订单金额&lt;/p&gt; |  [optional]
**createTime** | **String** | &lt;p&gt;订单创建时间&lt;/p&gt; &lt;pre&gt;yyyy-MM-dd HH:mm:ss&lt;/pre&gt; |  [optional]
**uniqueOrderNo** | **String** |  |  [optional]
**productName** | **String** |  |  [optional]
**status** | [**StatusEnum**](#StatusEnum) | &lt;p&gt;订单状态&lt;/p&gt; 可选项如下: PROCESSING:处理中 SUCCESS:成功 FAIL:失败  | 


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



