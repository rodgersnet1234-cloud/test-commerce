# InsuranceClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**realnameAuth**](InsuranceClient.md#realnameAuth) | **POST** /rest/v1.0/insurance/realname/auth | 实名缴费认证
[**realnameNotify**](InsuranceClient.md#realnameNotify) | **POST** /rest/v1.0/insurance/realname/notify | 交易通知


<a name="realnameAuth"></a>
# **realnameAuth**
RealnameAuthResponse realnameAuth(RealnameAuthRequest request)

实名缴费认证

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.insurance.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InsuranceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InsuranceClient api = InsuranceClientBuilder.builder().build();

//RealnameAuthRequest中的参数说明参见Parameters章节
RealnameAuthRequest request = new RealnameAuthRequest();
request.setBody(new RealnameAuthCommonInsurRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RealnameAuthResponse response = api.realnameAuth(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InsuranceClient#realnameAuth, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**RealnameAuthCommonInsurRequestDTOParam**](../model/RealnameAuthCommonInsurRequestDTOParam.md)|  |

### Return type
[**RealnameAuthCommonInsurResponseDTOResult**](../model/RealnameAuthCommonInsurResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="realnameNotify"></a>
# **realnameNotify**
RealnameNotifyResponse realnameNotify(RealnameNotifyRequest request)

交易通知

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.insurance.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InsuranceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InsuranceClient api = InsuranceClientBuilder.builder().build();

//RealnameNotifyRequest中的参数说明参见Parameters章节
RealnameNotifyRequest request = new RealnameNotifyRequest();
request.setRequestNo("requestNo_example");
request.setQueryNo("queryNo_example");
request.setCustomrNo("customrNo_example");
request.setCode("code_example");
request.setAmount("amount_example");
request.setCardNo("cardNo_example");
request.setTradeNo("tradeNo_example");
request.setDate("date_example");
request.setSystemNo("systemNo_example");
request.setTerminalNo("terminalNo_example");
request.setPaNo("paNo_example");
request.setValidateSequenceNo("validateSequenceNo_example");
request.setRequestType("requestType_example");
request.setWarrantBank("warrantBank_example");
request.setAesKey("aesKey_example");
request.setUser("user_example");
request.setPassword("password_example");
request.setProdId("prodId_example");
request.setReqType("reqType_example");
request.setSysId("sysId_example");
request.setRequestUrl("requestUrl_example");
request.setMacKey("macKey_example");
request.setEnvironment("environment_example");
request.setTpdu("tpdu_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RealnameNotifyResponse response = api.realnameNotify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InsuranceClient#realnameNotify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **queryNo** | **String**|  | [optional]
 **customrNo** | **String**|  | [optional]
 **code** | **String**|  | [optional]
 **amount** | **String**|  | [optional]
 **cardNo** | **String**|  | [optional]
 **tradeNo** | **String**|  | [optional]
 **date** | **String**|  | [optional]
 **systemNo** | **String**|  | [optional]
 **terminalNo** | **String**|  | [optional]
 **paNo** | **String**|  | [optional]
 **validateSequenceNo** | **String**|  | [optional]
 **requestType** | **String**|  | [optional]
 **warrantBank** | **String**|  | [optional]
 **aesKey** | **String**|  | [optional]
 **user** | **String**|  | [optional]
 **password** | **String**|  | [optional]
 **prodId** | **String**|  | [optional]
 **reqType** | **String**|  | [optional]
 **sysId** | **String**|  | [optional]
 **requestUrl** | **String**|  | [optional]
 **macKey** | **String**|  | [optional]
 **environment** | **String**|  | [optional]
 **tpdu** | **String**|  | [optional]

### Return type
[**RealnameNotifyCommonNoticeResponseDTOResult**](../model/RealnameNotifyCommonNoticeResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

