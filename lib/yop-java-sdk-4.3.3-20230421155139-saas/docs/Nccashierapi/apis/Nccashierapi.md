# NccashierapiClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apiPay**](NccashierapiClient.md#apiPay) | **POST** /rest/v1.0/nccashierapi/api/pay | 聚合API收银台


<a name="apiPay"></a>
# **apiPay**
ApiPayResponse apiPay(ApiPayRequest request)

聚合API收银台

&lt;p&gt;API收银台统一支付接口，支持主扫支付(微信/支付宝/京东)、被扫支付(微信/支付宝/京东)、微信公众号、小程序支付、微信SDK支付&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.nccashierapi.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(NccashierapiClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
NccashierapiClient api = NccashierapiClientBuilder.builder().build();

//ApiPayRequest中的参数说明参见Parameters章节
ApiPayRequest request = new ApiPayRequest();
request.setPayTool("SCCANPAY");
request.setPayType("WECHAT");
request.setToken("token_example");
request.setAppId("appId_example");
request.setOpenId("openId_example");
request.setVersion("1.0");
request.setPayEmpowerNo("payEmpowerNo_example");
request.setMerchantTerminalId("merchantTerminalId_example");
request.setMerchantStoreNo("merchantStoreNo_example");
request.setUserIp("userIp_example");
request.setExtParamMap("{\"reportFee\":\"XIANXIA\"}");
request.setUserNo("userNo_example");
request.setUserType("userType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ApiPayResponse response = api.apiPay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling NccashierapiClient#apiPay, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payTool** | **String**|  | [optional]
 **payType** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **openId** | **String**|  | [optional]
 **version** | **String**|  | [optional]
 **payEmpowerNo** | **String**|  | [optional]
 **merchantTerminalId** | **String**|  | [optional]
 **merchantStoreNo** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **extParamMap** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]

### Return type
[**ApiPayUnifiedAPICashierResponseDTOResult**](../model/ApiPayUnifiedAPICashierResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

