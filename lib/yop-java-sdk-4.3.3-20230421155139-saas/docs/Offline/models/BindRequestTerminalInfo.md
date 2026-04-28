
# BindRequestTerminalInfo

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | **String** | &lt;pre&gt;交互模式:&lt;br /&gt;枚举值：&lt;br /&gt;NONORDER：内部下单（默认）&lt;br /&gt;SCAN：扫码&lt;br /&gt;PUSH：推单&lt;/pre&gt; |  [optional]
**isVoice** | **Integer** | &lt;pre&gt;交易完成后是否语音播报 &lt;br /&gt;0:否&lt;br /&gt;1:是（默认）&lt;/pre&gt; |  [optional]
**memo** | [**BindTerminalMemo**](BindTerminalMemo.md) |  |  [optional]
**payWay** | [**PayWayInfo**](PayWayInfo.md) |  |  [optional]
**shopNo** | **String** | &lt;pre&gt;网点编号&lt;/pre&gt; |  [optional]
**serialNo** | **String** | &lt;p&gt;终端序列号&lt;/p&gt; | 



