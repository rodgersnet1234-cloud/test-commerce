# AuthClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**faceAuth**](AuthClient.md#faceAuth) | **POST** /rest/v1.0/auth/face-auth | 人脸核验
[**faceAuthKyc**](AuthClient.md#faceAuthKyc) | **POST** /rest/v1.0/auth/face-auth-kyc | 身份核验
[**faceAuthKycQuery**](AuthClient.md#faceAuthKycQuery) | **GET** /rest/v1.0/auth/face-auth-kyc-query | 身份核验结果查询
[**faceAuthResultQuery**](AuthClient.md#faceAuthResultQuery) | **GET** /rest/v1.0/auth/face-auth-result-query | 人脸核验结果查询
[**multipleAuth**](AuthClient.md#multipleAuth) | **POST** /rest/v1.0/auth/multiple-auth | 新信息认证


<a name="faceAuth"></a>
# **faceAuth**
FaceAuthResponse faceAuth(FaceAuthRequest request)

人脸核验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.auth.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AuthClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AuthClient api = AuthClientBuilder.builder().build();

//FaceAuthRequest中的参数说明参见Parameters章节
FaceAuthRequest request = new FaceAuthRequest();
request.setRequestNo("REQ6437657876");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10012345679");
request.setName("张三");
request.setCardNo("cardNo_example");
request.setCardType("cardType_example");
request.setReturnUrl("returnUrl_example");
request.setNotifyUrl("notifyUrl_example");
request.setExtraData("extraData_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FaceAuthResponse response = api.faceAuth(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AuthClient#faceAuth, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **cardNo** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **extraData** | **String**|  | [optional]

### Return type
[**FaceAuthFaceAuthResponseDTOResult**](../model/FaceAuthFaceAuthResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="faceAuthKyc"></a>
# **faceAuthKyc**
FaceAuthKycResponse faceAuthKyc(FaceAuthKycRequest request)

身份核验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.auth.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AuthClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AuthClient api = AuthClientBuilder.builder().build();

//FaceAuthKycRequest中的参数说明参见Parameters章节
FaceAuthKycRequest request = new FaceAuthKycRequest();
request.setRequestNo("REQ6437657876");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10012345679");
request.setName("张三");
request.setCardNo("cardNo_example");
request.setCardType("cardType_example");
request.setReturnUrl("returnUrl_example");
request.setNotifyUrl("notifyUrl_example");
request.setExtraData("extraData_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FaceAuthKycResponse response = api.faceAuthKyc(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AuthClient#faceAuthKyc, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **cardNo** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **extraData** | **String**|  | [optional]

### Return type
[**FaceAuthKycFaceAuthResponseDTOResult**](../model/FaceAuthKycFaceAuthResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="faceAuthKycQuery"></a>
# **faceAuthKycQuery**
FaceAuthKycQueryResponse faceAuthKycQuery(FaceAuthKycQueryRequest request)

身份核验结果查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.auth.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AuthClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AuthClient api = AuthClientBuilder.builder().build();

//FaceAuthKycQueryRequest中的参数说明参见Parameters章节
FaceAuthKycQueryRequest request = new FaceAuthKycQueryRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FaceAuthKycQueryResponse response = api.faceAuthKycQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AuthClient#faceAuthKycQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**FaceAuthKycQueryFaceAuthResultQueryResponseDTOResult**](../model/FaceAuthKycQueryFaceAuthResultQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="faceAuthResultQuery"></a>
# **faceAuthResultQuery**
FaceAuthResultQueryResponse faceAuthResultQuery(FaceAuthResultQueryRequest request)

人脸核验结果查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.auth.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AuthClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AuthClient api = AuthClientBuilder.builder().build();

//FaceAuthResultQueryRequest中的参数说明参见Parameters章节
FaceAuthResultQueryRequest request = new FaceAuthResultQueryRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FaceAuthResultQueryResponse response = api.faceAuthResultQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AuthClient#faceAuthResultQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**FaceAuthResultQueryFaceAuthResultQueryResponseDTOResult**](../model/FaceAuthResultQueryFaceAuthResultQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="multipleAuth"></a>
# **multipleAuth**
MultipleAuthResponse multipleAuth(MultipleAuthRequest request)

新信息认证



### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.auth.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AuthClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AuthClient api = AuthClientBuilder.builder().build();

//MultipleAuthRequest中的参数说明参见Parameters章节
MultipleAuthRequest request = new MultipleAuthRequest();
request.setMerchantNo("100000000000");
request.setAuthType("authType_example");
request.setRequestNo("requestNo_example");
request.setIdCardNo("230231199510101010");
request.setUsername("易小宝");
request.setBankCardNo("6217876555556554324");
request.setRemark("remark_example");
request.setMobile("mobile_example");
request.setIdCardType("idCardType_example");
request.setClientSource("clientSource_example");
request.setExtMap("{\"verifyBsnSceneDesc\":\"描述\",\"sourceIP\":\"AD80:0000:0000:0000:ABAA:0000:00C 2:0002\",\"appType\":\"01\",\"appName\":\"某某银行直销银行\",\"verifyBsnScene\":\"99\",\"ipType\":\"06\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MultipleAuthResponse response = api.multipleAuth(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AuthClient#multipleAuth, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **authType** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **username** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **clientSource** | **String**|  | [optional]
 **extMap** | **String**|  | [optional]

### Return type
[**MultipleAuthAuthResponseDTOResult**](../model/MultipleAuthAuthResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

