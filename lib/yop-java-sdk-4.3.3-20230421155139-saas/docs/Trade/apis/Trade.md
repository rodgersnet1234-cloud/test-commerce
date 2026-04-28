# TradeClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**order**](TradeClient.md#order) | **POST** /rest/v1.0/trade/order | 交易下单
[**orderClose**](TradeClient.md#orderClose) | **POST** /rest/v1.0/trade/order/close | 关闭订单
[**orderCombineQuery**](TradeClient.md#orderCombineQuery) | **GET** /rest/v1.0/trade/order/combine-query | 查询合并订单
[**orderQuery**](TradeClient.md#orderQuery) | **GET** /rest/v1.0/trade/order/query | 查询订单
[**receiptDownload**](TradeClient.md#receiptDownload) | **GET** /yos/v1.0/trade/receipt/download | 交易回单
[**refund**](TradeClient.md#refund) | **POST** /rest/v1.0/trade/refund | 申请退款
[**refundEnd**](TradeClient.md#refundEnd) | **POST** /rest/v1.0/trade/refund/end | 结束退款
[**refundFast**](TradeClient.md#refundFast) | **POST** /rest/v1.0/trade/refund/fast | 申请极速退款
[**refundQuery**](TradeClient.md#refundQuery) | **GET** /rest/v1.0/trade/refund/query | 查询退款
[**refundReceiptDownload**](TradeClient.md#refundReceiptDownload) | **GET** /yos/v1.0/trade/refund/receipt/download | 退款回单
[**refundSupply**](TradeClient.md#refundSupply) | **POST** /rest/v1.0/trade/refund/supply | 上送卡信息退款


<a name="order"></a>
# **order**
OrderResponse order(OrderRequest request)

交易下单

交易下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//OrderRequest中的参数说明参见Parameters章节
OrderRequest request = new OrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setOrderAmount("100.50");
request.setGoodsName("goodsName_example");
request.setFundProcessType("fundProcessType_example");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("memo_example");
request.setSubOrderDetail("subOrderDetail_example");
request.setExpiredTime("expiredTime_example");
request.setRedirectUrl("redirectUrl_example");
request.setCsUrl("csUrl_example");
request.setBusinessInfo("businessInfo_example");
request.setTerminalInfo("{\"terminalNo\":\"15704925\",\"terminalType\":\"POS”,”payWay”:”POS”}");
request.setYpPromotionInfo("自定义补贴商户[{\"type\":\"CUSTOM_ALLOWANCE\"}]");
request.setPayerInfo("{\"bankCardNo\":\"6225750005831234\",\"cardName\":\"爱丽丝\",\"idCardNo\":\"130225199006093323\",\"mobilePhoneNo\":\"13902092131\",\"userID\":\"20056788\"}");
request.setPayMerchantNo("payMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OrderResponse response = api.order(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#order, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **subOrderDetail** | **String**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **redirectUrl** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]
 **terminalInfo** | **String**|  | [optional]
 **ypPromotionInfo** | **String**|  | [optional]
 **payerInfo** | **String**|  | [optional]
 **payMerchantNo** | **String**|  | [optional]

### Return type
[**OrderYopCreateOrderV2ResDTOResult**](../model/OrderYopCreateOrderV2ResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="orderClose"></a>
# **orderClose**
OrderCloseResponse orderClose(OrderCloseRequest request)

关闭订单

关闭订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//OrderCloseRequest中的参数说明参见Parameters章节
OrderCloseRequest request = new OrderCloseRequest();
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OrderCloseResponse response = api.orderClose(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#orderClose, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**OrderCloseResponseOrderCloseDTOResult**](../model/OrderCloseResponseOrderCloseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="orderCombineQuery"></a>
# **orderCombineQuery**
OrderCombineQueryResponse orderCombineQuery(OrderCombineQueryRequest request)

查询合并订单

查询合并订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//OrderCombineQueryRequest中的参数说明参见Parameters章节
OrderCombineQueryRequest request = new OrderCombineQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setOrderId("orderId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OrderCombineQueryResponse response = api.orderCombineQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#orderCombineQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 交易发起方商编，此处为平台商商户编号 |
 **orderId** | **String**| 交易下单时传入的合单收款请求号 |

### Return type
[**OrderCombineQueryYopQueryCombineOrderResDTOResult**](../model/OrderCombineQueryYopQueryCombineOrderResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="orderQuery"></a>
# **orderQuery**
OrderQueryResponse orderQuery(OrderQueryRequest request)

查询订单

查询订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//OrderQueryRequest中的参数说明参见Parameters章节
OrderQueryRequest request = new OrderQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OrderQueryResponse response = api.orderQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#orderQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号。与交易下单传入的保持一致 |
 **merchantNo** | **String**| 收款商户编号 |
 **orderId** | **String**| 交易下单传入的商户收款请求号。&lt;br&gt;(合单收款场景请传入子单的商户收款请求号) |

### Return type
[**OrderQueryYopQueryOrderResDTOResult**](../model/OrderQueryYopQueryOrderResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="receiptDownload"></a>
# **receiptDownload**
ReceiptDownloadResponse receiptDownload(ReceiptDownloadRequest request)

交易回单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//ReceiptDownloadRequest中的参数说明参见Parameters章节
ReceiptDownloadRequest request = new ReceiptDownloadRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ReceiptDownloadResponse response = api.receiptDownload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#receiptDownload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| *标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**| 收款商户商编。单笔收款必传，合单收款场景中上传子单域信息subOrderDetail里的merchantNo |
 **orderId** | **String**|  |

### Return type
[**ReceiptDownloadReceiptResponseDTOResult**](../model/ReceiptDownloadReceiptResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refund"></a>
# **refund**
RefundResponse refund(RefundRequest request)

申请退款

&lt;p&gt;* 订单状态为“SUCCESS”时才能发起退款。&lt;/p&gt; &lt;p&gt;* 退款支持单笔交易分多次退款，多次退款需要提交原支付订单的商户订单号和不同的退款单号，总退款金额不能超过用户实际支付金额。&lt;/p&gt; &lt;p&gt;* 一笔退款失败后重新提交，请不要更换退款单号，请使用相同的商户退款请求号请求退款。&lt;/p&gt; * 申请退款接口的响应参数code仅代表业务的受理情况，具体退款是否成功，需要通过申请退款或查询退款接口返回的status获取退款结果。&lt;/br&gt;   &lt;span&gt;（1）当响应参数code&#x3D;OPR00000时,说明易宝已受理该笔退款,此时需要根据status来判断退款状态；&lt;/span&gt;   （2）当响应参数code≠OPR00000时,说明易宝没有受理该笔退款，可根据返回的message进行相应处理。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundRequest中的参数说明参见Parameters章节
RefundRequest request = new RefundRequest();
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");
request.setOrderId("order123456789");
request.setRefundRequestId("refundorder987654");
request.setUniqueOrderNo("1001201612070000000000000565");
request.setRefundAmount("88.88");
request.setDescription("用户申请退货并退款");
request.setMemo("退款");
request.setRefundAccountType("FUND_ACCOUNT");
request.setNotifyUrl("notifyUrl_example");
request.setYpPromotionRefundInfo("ypPromotionRefundInfo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundResponse response = api.refund(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refund, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **refundRequestId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **refundAmount** | **String**|  | [optional]
 **description** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **refundAccountType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **ypPromotionRefundInfo** | **String**|  | [optional]

### Return type
[**RefundResponseRefundDTOResult**](../model/RefundResponseRefundDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refundEnd"></a>
# **refundEnd**
RefundEndResponse refundEnd(RefundEndRequest request)

结束退款

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundEndRequest中的参数说明参见Parameters章节
RefundEndRequest request = new RefundEndRequest();
request.setOrderId("orderId123456");
request.setRefundRequestId("refund123456");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundEndResponse response = api.refundEnd(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refundEnd, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **refundRequestId** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**RefundEndYopEndRefundResponseDTOResult**](../model/RefundEndYopEndRefundResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refundFast"></a>
# **refundFast**
RefundFastResponse refundFast(RefundFastRequest request)

申请极速退款

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundFastRequest中的参数说明参见Parameters章节
RefundFastRequest request = new RefundFastRequest();
request.setOrderId("order123456789");
request.setRefundRequestId("refundorder987654321");
request.setRefundAmount("88.88");
request.setDescription("用户申请退货");
request.setRefundAccountType("FUND_ACCOUNT");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("memo_example");
request.setCardInfo("cardInfo_example");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundFastResponse response = api.refundFast(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refundFast, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **refundRequestId** | **String**|  | [optional]
 **refundAmount** | **String**|  | [optional]
 **description** | **String**|  | [optional]
 **refundAccountType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **cardInfo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**RefundFastYopFastRefundResponseDTOResult**](../model/RefundFastYopFastRefundResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refundQuery"></a>
# **refundQuery**
RefundQueryResponse refundQuery(RefundQueryRequest request)

查询退款

&lt;p&gt;提交退款申请后，通过调用该接口查询退款状态&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundQueryRequest中的参数说明参见Parameters章节
RefundQueryRequest request = new RefundQueryRequest();
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");
request.setOrderId("orderId_example");
request.setRefundRequestId("refundRequestId_example");
request.setUniqueRefundNo("uniqueRefundNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundQueryResponse response = api.refundQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refundQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号。与交易下单传入的保持一致 |
 **merchantNo** | **String**| 收款商户编号 |
 **orderId** | **String**| 收款交易对应的商户收款请求号 |
 **refundRequestId** | **String**| 商户退款请求号。可包含字母、数字、下划线；需要保证在商户端不重复。 |
 **uniqueRefundNo** | **String**| 商户退款请求对应在易宝的退款单号 | [optional]

### Return type
[**RefundQueryQueryRefundResponseDTOResult**](../model/RefundQueryQueryRefundResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refundReceiptDownload"></a>
# **refundReceiptDownload**
RefundReceiptDownloadResponse refundReceiptDownload(RefundReceiptDownloadRequest request)

退款回单

退款回单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundReceiptDownloadRequest中的参数说明参见Parameters章节
RefundReceiptDownloadRequest request = new RefundReceiptDownloadRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setRefundRequestId("refundRequestId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundReceiptDownloadResponse response = api.refundReceiptDownload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refundReceiptDownload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| *标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**| 收款商户商编。单笔收款必传，合单收款场景中上传子单域信息subOrderDetail里的merchantNo |
 **orderId** | **String**|  |
 **refundRequestId** | **String**|  |

### Return type
[**RefundReceiptDownloadReceiptResponseDTOResult**](../model/RefundReceiptDownloadReceiptResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="refundSupply"></a>
# **refundSupply**
RefundSupplyResponse refundSupply(RefundSupplyRequest request)

上送卡信息退款

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.trade.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TradeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TradeClient api = TradeClientBuilder.builder().build();

//RefundSupplyRequest中的参数说明参见Parameters章节
RefundSupplyRequest request = new RefundSupplyRequest();
request.setOrderId("order123456789");
request.setRefundRequestId("refundorder987654321");
request.setCardInfo("cardInfo_example");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RefundSupplyResponse response = api.refundSupply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TradeClient#refundSupply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **refundRequestId** | **String**|  | [optional]
 **cardInfo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**RefundSupplyYopSupplyCardInfoRefundResponseDTOResult**](../model/RefundSupplyYopSupplyCardInfoRefundResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

