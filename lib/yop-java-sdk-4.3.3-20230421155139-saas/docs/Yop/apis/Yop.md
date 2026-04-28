# YopClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oauth2ReportKey**](YopClient.md#oauth2ReportKey) | **POST** /rest/v1.0/yop/oauth2/report-key | YOP报备临时公钥


<a name="oauth2ReportKey"></a>
# **oauth2ReportKey**
Oauth2ReportKeyResponse oauth2ReportKey(Oauth2ReportKeyRequest request)

YOP报备临时公钥

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.yop.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(YopClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
YopClient api = YopClientBuilder.builder().build();

//Oauth2ReportKeyRequest中的参数说明参见Parameters章节
Oauth2ReportKeyRequest request = new Oauth2ReportKeyRequest();
request.setKeyType("keyType_example");
request.setKey("key_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    Oauth2ReportKeyResponse response = api.oauth2ReportKey(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling YopClient#oauth2ReportKey, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **keyType** | **String**|  | [optional]
 **key** | **String**|  | [optional]

### Return type
[**Oauth2ReportKeyHandshakeResponseResult**](../model/Oauth2ReportKeyHandshakeResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

