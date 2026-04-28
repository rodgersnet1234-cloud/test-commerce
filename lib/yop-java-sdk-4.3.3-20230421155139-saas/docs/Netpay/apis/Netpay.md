# NetpayClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**order**](NetpayClient.md#order) | **POST** /rest/v1.0/netpay/order | 网银支付


<a name="order"></a>
# **order**
OrderResponse order(OrderRequest request)

网银支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.netpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(NetpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
NetpayClient api = NetpayClientBuilder.builder().build();

//OrderRequest中的参数说明参见Parameters章节
OrderRequest request = new OrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:06");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("memo_example");
request.setGoodsName("goodsName_example");
request.setFundProcessType("fundProcessType_example");
request.setCardType("cardType_example");
request.setBankAccountType("bankAccountType_example");
request.setBankCode("bankCode_example");
request.setTerminalType("terminalType_example");
request.setPayerIp("payerIp_example");
request.setCsNotifyUrl("csNotifyUrl_example");
request.setBusinessInfo("businessInfo_example");
request.setRedirectUrl("redirectUrl_example");
request.setOrderType("orderType_example");
request.setPayerAccountName("payerAccountName_example");
request.setPayerAccountNo("payerAccountNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OrderResponse response = api.order(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling NetpayClient#order, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **bankAccountType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **terminalType** | **String**|  | [optional]
 **payerIp** | **String**|  | [optional]
 **csNotifyUrl** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]
 **redirectUrl** | **String**|  | [optional]
 **orderType** | **String**|  | [optional]
 **payerAccountName** | **String**|  | [optional]
 **payerAccountNo** | **String**|  | [optional]

### Return type
[**OrderOrderResponseDTOResult**](../model/OrderOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

