# FacepayClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**facepayProxyBindConfirmSms**](FacepayClient.md#facepayProxyBindConfirmSms) | **POST** /rest/v1.0/facepay/facepay-proxy/bind-confirm-sms | 绑卡确认短信
[**facepayProxyBindFirstCard**](FacepayClient.md#facepayProxyBindFirstCard) | **POST** /rest/v1.0/facepay/facepay-proxy/bind-first-card | 首次绑卡
[**facepayProxyBindSendSms**](FacepayClient.md#facepayProxyBindSendSms) | **POST** /rest/v1.0/facepay/facepay-proxy/bind-send-sms | 绑卡发送短验
[**facepayProxyCertificateNoAuth**](FacepayClient.md#facepayProxyCertificateNoAuth) | **POST** /rest/v1.0/facepay/facepay-proxy/certificate-no-auth | 身份认证验证
[**facepayProxyCheckLogonSmscode**](FacepayClient.md#facepayProxyCheckLogonSmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/check-logon-smscode | 检查登录短信验证
[**facepayProxyConfirmFirstCardSmscode**](FacepayClient.md#facepayProxyConfirmFirstCardSmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/confirm-first-card-smscode | 第一张卡确认短验
[**facepayProxyConfirmVerifySmscode**](FacepayClient.md#facepayProxyConfirmVerifySmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/confirm-verify-smscode | 确认验证短验
[**facepayProxyCreateBindCard**](FacepayClient.md#facepayProxyCreateBindCard) | **POST** /rest/v1.0/facepay/facepay-proxy/create-bind-card | 创建绑卡记录
[**facepayProxyCreateOrder**](FacepayClient.md#facepayProxyCreateOrder) | **POST** /rest/v1.0/facepay/facepay-proxy/create-order | 创建订单
[**facepayProxyFaceLogon**](FacepayClient.md#facepayProxyFaceLogon) | **POST** /rest/v1.0/facepay/facepay-proxy/face-logon | 人脸登录
[**facepayProxyOpenFaceAccount**](FacepayClient.md#facepayProxyOpenFaceAccount) | **POST** /rest/v1.0/facepay/facepay-proxy/open-face-account | 开通人脸账号
[**facepayProxyPaySendSms**](FacepayClient.md#facepayProxyPaySendSms) | **POST** /rest/v1.0/facepay/facepay-proxy/pay-send-sms | 支付发送短验
[**facepayProxyQueryBindCardInfo**](FacepayClient.md#facepayProxyQueryBindCardInfo) | **POST** /rest/v1.0/facepay/facepay-proxy/query-bind-card-info | 检查卡bin
[**facepayProxyQueryOrderAfter**](FacepayClient.md#facepayProxyQueryOrderAfter) | **POST** /rest/v1.0/facepay/facepay-proxy/query-order-after | 后查订单
[**facepayProxyQueryOrderBefore**](FacepayClient.md#facepayProxyQueryOrderBefore) | **POST** /rest/v1.0/facepay/facepay-proxy/query-order-before | 查询订单
[**facepayProxySendFirstCardSmscode**](FacepayClient.md#facepayProxySendFirstCardSmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/send-first-card-smscode | 第一张绑卡发送短验
[**facepayProxySendLogonSmscode**](FacepayClient.md#facepayProxySendLogonSmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/send-logon-smscode | 发送登录短信验证
[**facepayProxySendVerifySmscode**](FacepayClient.md#facepayProxySendVerifySmscode) | **POST** /rest/v1.0/facepay/facepay-proxy/send-verify-smscode | 发送验证短验
[**facepayProxyVerifyUserInfo**](FacepayClient.md#facepayProxyVerifyUserInfo) | **POST** /rest/v1.0/facepay/facepay-proxy/verify-user-info | 验证用户基本信息
[**oAuth2TokenGenerateToken**](FacepayClient.md#oAuth2TokenGenerateToken) | **POST** /rest/v1.0/facepay/o-auth2-token/generate-token | 生成token
[**sosDeleteBindNo**](FacepayClient.md#sosDeleteBindNo) | **POST** /rest/v1.0/facepay/sos/delete-bind-no | 删除绑卡编号


<a name="facepayProxyBindConfirmSms"></a>
# **facepayProxyBindConfirmSms**
FacepayProxyBindConfirmSmsResponse facepayProxyBindConfirmSms(FacepayProxyBindConfirmSmsRequest request)

绑卡确认短信

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyBindConfirmSmsRequest中的参数说明参见Parameters章节
FacepayProxyBindConfirmSmsRequest request = new FacepayProxyBindConfirmSmsRequest();
request.setBindBizNo("bindBizNo_example");
request.setSmsCode("smsCode_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyBindConfirmSmsResponse response = api.facepayProxyBindConfirmSms(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyBindConfirmSms, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bindBizNo** | **String**|  | [optional]
 **smsCode** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyBindConfirmSmsBindCardResponseResult**](../model/FacepayProxyBindConfirmSmsBindCardResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyBindFirstCard"></a>
# **facepayProxyBindFirstCard**
FacepayProxyBindFirstCardResponse facepayProxyBindFirstCard(FacepayProxyBindFirstCardRequest request)

首次绑卡

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyBindFirstCardRequest中的参数说明参见Parameters章节
FacepayProxyBindFirstCardRequest request = new FacepayProxyBindFirstCardRequest();
request.setBankCardNo("bankCardNo_example");
request.setPhoneNumber("phoneNumber_example");
request.setCvv2("cvv2_example");
request.setExpireDate("expireDate_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyBindFirstCardResponse response = api.facepayProxyBindFirstCard(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyBindFirstCard, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bankCardNo** | **String**|  | [optional]
 **phoneNumber** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **expireDate** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyBindFirstCardBindCardResponseResult**](../model/FacepayProxyBindFirstCardBindCardResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyBindSendSms"></a>
# **facepayProxyBindSendSms**
FacepayProxyBindSendSmsResponse facepayProxyBindSendSms(FacepayProxyBindSendSmsRequest request)

绑卡发送短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyBindSendSmsRequest中的参数说明参见Parameters章节
FacepayProxyBindSendSmsRequest request = new FacepayProxyBindSendSmsRequest();
request.setBindBizNo("bindBizNo_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyBindSendSmsResponse response = api.facepayProxyBindSendSms(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyBindSendSms, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bindBizNo** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyBindSendSmsBindCardResponseResult**](../model/FacepayProxyBindSendSmsBindCardResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyCertificateNoAuth"></a>
# **facepayProxyCertificateNoAuth**
FacepayProxyCertificateNoAuthResponse facepayProxyCertificateNoAuth(FacepayProxyCertificateNoAuthRequest request)

身份认证验证

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyCertificateNoAuthRequest中的参数说明参见Parameters章节
FacepayProxyCertificateNoAuthRequest request = new FacepayProxyCertificateNoAuthRequest();
request.setOrderToken("orderToken_example");
request.setFaceRequestNo("faceRequestNo_example");
request.setCertificateNoLastN("certificateNoLastN_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyCertificateNoAuthResponse response = api.facepayProxyCertificateNoAuth(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyCertificateNoAuth, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderToken** | **String**|  | [optional]
 **faceRequestNo** | **String**|  | [optional]
 **certificateNoLastN** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyCertificateNoAuthFaceLogonResponseResult**](../model/FacepayProxyCertificateNoAuthFaceLogonResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyCheckLogonSmscode"></a>
# **facepayProxyCheckLogonSmscode**
FacepayProxyCheckLogonSmscodeResponse facepayProxyCheckLogonSmscode(FacepayProxyCheckLogonSmscodeRequest request)

检查登录短信验证

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyCheckLogonSmscodeRequest中的参数说明参见Parameters章节
FacepayProxyCheckLogonSmscodeRequest request = new FacepayProxyCheckLogonSmscodeRequest();
request.setOrderToken("orderToken_example");
request.setFaceRequestNo("faceRequestNo_example");
request.setSmsCode("smsCode_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyCheckLogonSmscodeResponse response = api.facepayProxyCheckLogonSmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyCheckLogonSmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderToken** | **String**|  | [optional]
 **faceRequestNo** | **String**|  | [optional]
 **smsCode** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyCheckLogonSmscodeBaseUserResponseResult**](../model/FacepayProxyCheckLogonSmscodeBaseUserResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyConfirmFirstCardSmscode"></a>
# **facepayProxyConfirmFirstCardSmscode**
FacepayProxyConfirmFirstCardSmscodeResponse facepayProxyConfirmFirstCardSmscode(FacepayProxyConfirmFirstCardSmscodeRequest request)

第一张卡确认短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyConfirmFirstCardSmscodeRequest中的参数说明参见Parameters章节
FacepayProxyConfirmFirstCardSmscodeRequest request = new FacepayProxyConfirmFirstCardSmscodeRequest();
request.setBindBizNo("bindBizNo_example");
request.setSmsCode("smsCode_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyConfirmFirstCardSmscodeResponse response = api.facepayProxyConfirmFirstCardSmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyConfirmFirstCardSmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bindBizNo** | **String**|  | [optional]
 **smsCode** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyConfirmFirstCardSmscodeBaseResponseResult**](../model/FacepayProxyConfirmFirstCardSmscodeBaseResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyConfirmVerifySmscode"></a>
# **facepayProxyConfirmVerifySmscode**
FacepayProxyConfirmVerifySmscodeResponse facepayProxyConfirmVerifySmscode(FacepayProxyConfirmVerifySmscodeRequest request)

确认验证短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyConfirmVerifySmscodeRequest中的参数说明参见Parameters章节
FacepayProxyConfirmVerifySmscodeRequest request = new FacepayProxyConfirmVerifySmscodeRequest();
request.setSmsCode("smsCode_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyConfirmVerifySmscodeResponse response = api.facepayProxyConfirmVerifySmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyConfirmVerifySmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smsCode** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyConfirmVerifySmscodeUserInfoResponseResult**](../model/FacepayProxyConfirmVerifySmscodeUserInfoResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyCreateBindCard"></a>
# **facepayProxyCreateBindCard**
FacepayProxyCreateBindCardResponse facepayProxyCreateBindCard(FacepayProxyCreateBindCardRequest request)

创建绑卡记录

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyCreateBindCardRequest中的参数说明参见Parameters章节
FacepayProxyCreateBindCardRequest request = new FacepayProxyCreateBindCardRequest();
request.setBankCardNo("bankCardNo_example");
request.setPhoneNumber("phoneNumber_example");
request.setCvv2("cvv2_example");
request.setExpireDate("expireDate_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyCreateBindCardResponse response = api.facepayProxyCreateBindCard(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyCreateBindCard, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bankCardNo** | **String**|  | [optional]
 **phoneNumber** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **expireDate** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyCreateBindCardBindCardResponseResult**](../model/FacepayProxyCreateBindCardBindCardResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyCreateOrder"></a>
# **facepayProxyCreateOrder**
FacepayProxyCreateOrderResponse facepayProxyCreateOrder(FacepayProxyCreateOrderRequest request)

创建订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyCreateOrderRequest中的参数说明参见Parameters章节
FacepayProxyCreateOrderRequest request = new FacepayProxyCreateOrderRequest();
request.setOrderToken("orderToken_example");
request.setOrderAmount("orderAmount_example");
request.setUniquePayNo("uniquePayNo_example");
request.setBindBizNo("bindBizNo_example");
request.setExpireDate("expireDate_example");
request.setCvv2("cvv2_example");
request.setSmsCode("smsCode_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyCreateOrderResponse response = api.facepayProxyCreateOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyCreateOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderToken** | **String**|  | [optional]
 **orderAmount** | **String**|  | [optional]
 **uniquePayNo** | **String**|  | [optional]
 **bindBizNo** | **String**|  | [optional]
 **expireDate** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **smsCode** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyCreateOrderPayOrderResponseResult**](../model/FacepayProxyCreateOrderPayOrderResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyFaceLogon"></a>
# **facepayProxyFaceLogon**
FacepayProxyFaceLogonResponse facepayProxyFaceLogon(FacepayProxyFaceLogonRequest request)

人脸登录

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyFaceLogonRequest中的参数说明参见Parameters章节
FacepayProxyFaceLogonRequest request = new FacepayProxyFaceLogonRequest();
request.setOrderToken("orderToken_example");
request.setFaceImage("faceImage_example");
request.setCollectType("collectType_example");
request.setCollectDevice("collectDevice_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyFaceLogonResponse response = api.facepayProxyFaceLogon(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyFaceLogon, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderToken** | **String**|  | [optional]
 **faceImage** | **String**|  | [optional]
 **collectType** | **String**|  | [optional]
 **collectDevice** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyFaceLogonFaceLogonResponseResult**](../model/FacepayProxyFaceLogonFaceLogonResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyOpenFaceAccount"></a>
# **facepayProxyOpenFaceAccount**
FacepayProxyOpenFaceAccountResponse facepayProxyOpenFaceAccount(FacepayProxyOpenFaceAccountRequest request)

开通人脸账号

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyOpenFaceAccountRequest中的参数说明参见Parameters章节
FacepayProxyOpenFaceAccountRequest request = new FacepayProxyOpenFaceAccountRequest();
request.setFaceImageFirst("faceImageFirst_example");
request.setFaceImageSecond("faceImageSecond_example");
request.setFaceImageThird("faceImageThird_example");
request.setCollectType("collectType_example");
request.setCollectDevice("collectDevice_example");
request.setOrderToken("orderToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyOpenFaceAccountResponse response = api.facepayProxyOpenFaceAccount(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyOpenFaceAccount, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **faceImageFirst** | **String**|  | [optional]
 **faceImageSecond** | **String**|  | [optional]
 **faceImageThird** | **String**|  | [optional]
 **collectType** | **String**|  | [optional]
 **collectDevice** | **String**|  | [optional]
 **orderToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyOpenFaceAccountBaseUserResponseResult**](../model/FacepayProxyOpenFaceAccountBaseUserResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyPaySendSms"></a>
# **facepayProxyPaySendSms**
FacepayProxyPaySendSmsResponse facepayProxyPaySendSms(FacepayProxyPaySendSmsRequest request)

支付发送短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyPaySendSmsRequest中的参数说明参见Parameters章节
FacepayProxyPaySendSmsRequest request = new FacepayProxyPaySendSmsRequest();
request.setUniquePayNo("uniquePayNo_example");
request.setBindBizNo("bindBizNo_example");
request.setCvv2("cvv2_example");
request.setExpireDate("expireDate_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyPaySendSmsResponse response = api.facepayProxyPaySendSms(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyPaySendSms, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uniquePayNo** | **String**|  | [optional]
 **bindBizNo** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **expireDate** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyPaySendSmsBaseUserResponseResult**](../model/FacepayProxyPaySendSmsBaseUserResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyQueryBindCardInfo"></a>
# **facepayProxyQueryBindCardInfo**
FacepayProxyQueryBindCardInfoResponse facepayProxyQueryBindCardInfo(FacepayProxyQueryBindCardInfoRequest request)

检查卡bin

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyQueryBindCardInfoRequest中的参数说明参见Parameters章节
FacepayProxyQueryBindCardInfoRequest request = new FacepayProxyQueryBindCardInfoRequest();
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyQueryBindCardInfoResponse response = api.facepayProxyQueryBindCardInfo(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyQueryBindCardInfo, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyQueryBindCardInfoBindCardInfoResponseResult**](../model/FacepayProxyQueryBindCardInfoBindCardInfoResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyQueryOrderAfter"></a>
# **facepayProxyQueryOrderAfter**
FacepayProxyQueryOrderAfterResponse facepayProxyQueryOrderAfter(FacepayProxyQueryOrderAfterRequest request)

后查订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyQueryOrderAfterRequest中的参数说明参见Parameters章节
FacepayProxyQueryOrderAfterRequest request = new FacepayProxyQueryOrderAfterRequest();
request.setOrderToken("orderToken_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyQueryOrderAfterResponse response = api.facepayProxyQueryOrderAfter(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyQueryOrderAfter, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderToken** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyQueryOrderAfterOrderAfterResponseResult**](../model/FacepayProxyQueryOrderAfterOrderAfterResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyQueryOrderBefore"></a>
# **facepayProxyQueryOrderBefore**
FacepayProxyQueryOrderBeforeResponse facepayProxyQueryOrderBefore(FacepayProxyQueryOrderBeforeRequest request)

查询订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyQueryOrderBeforeRequest中的参数说明参见Parameters章节
FacepayProxyQueryOrderBeforeRequest request = new FacepayProxyQueryOrderBeforeRequest();
request.setBody(new FacepayProxyQueryOrderBeforeOrderBeforeRequestParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyQueryOrderBeforeResponse response = api.facepayProxyQueryOrderBefore(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyQueryOrderBefore, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**FacepayProxyQueryOrderBeforeOrderBeforeRequestParam**](../model/FacepayProxyQueryOrderBeforeOrderBeforeRequestParam.md)|  |

### Return type
[**FacepayProxyQueryOrderBeforeOrderBeforeResponseResult**](../model/FacepayProxyQueryOrderBeforeOrderBeforeResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="facepayProxySendFirstCardSmscode"></a>
# **facepayProxySendFirstCardSmscode**
FacepayProxySendFirstCardSmscodeResponse facepayProxySendFirstCardSmscode(FacepayProxySendFirstCardSmscodeRequest request)

第一张绑卡发送短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxySendFirstCardSmscodeRequest中的参数说明参见Parameters章节
FacepayProxySendFirstCardSmscodeRequest request = new FacepayProxySendFirstCardSmscodeRequest();
request.setBindBizNo("bindBizNo_example");
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxySendFirstCardSmscodeResponse response = api.facepayProxySendFirstCardSmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxySendFirstCardSmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bindBizNo** | **String**|  | [optional]
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxySendFirstCardSmscodeBaseResponseResult**](../model/FacepayProxySendFirstCardSmscodeBaseResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxySendLogonSmscode"></a>
# **facepayProxySendLogonSmscode**
FacepayProxySendLogonSmscodeResponse facepayProxySendLogonSmscode(FacepayProxySendLogonSmscodeRequest request)

发送登录短信验证

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxySendLogonSmscodeRequest中的参数说明参见Parameters章节
FacepayProxySendLogonSmscodeRequest request = new FacepayProxySendLogonSmscodeRequest();
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxySendLogonSmscodeResponse response = api.facepayProxySendLogonSmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxySendLogonSmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxySendLogonSmscodeBaseResponseResult**](../model/FacepayProxySendLogonSmscodeBaseResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxySendVerifySmscode"></a>
# **facepayProxySendVerifySmscode**
FacepayProxySendVerifySmscodeResponse facepayProxySendVerifySmscode(FacepayProxySendVerifySmscodeRequest request)

发送验证短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxySendVerifySmscodeRequest中的参数说明参见Parameters章节
FacepayProxySendVerifySmscodeRequest request = new FacepayProxySendVerifySmscodeRequest();
request.setBizNo("bizNo_example");
request.setBizToken("bizToken_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxySendVerifySmscodeResponse response = api.facepayProxySendVerifySmscode(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxySendVerifySmscode, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bizNo** | **String**|  | [optional]
 **bizToken** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxySendVerifySmscodeBaseResponseResult**](../model/FacepayProxySendVerifySmscodeBaseResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="facepayProxyVerifyUserInfo"></a>
# **facepayProxyVerifyUserInfo**
FacepayProxyVerifyUserInfoResponse facepayProxyVerifyUserInfo(FacepayProxyVerifyUserInfoRequest request)

验证用户基本信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//FacepayProxyVerifyUserInfoRequest中的参数说明参见Parameters章节
FacepayProxyVerifyUserInfoRequest request = new FacepayProxyVerifyUserInfoRequest();
request.setName("name_example");
request.setCertificateNo("certificateNo_example");
request.setBizSystem("bizSystem_example");
request.setMtToken("mtToken_example");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FacepayProxyVerifyUserInfoResponse response = api.facepayProxyVerifyUserInfo(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#facepayProxyVerifyUserInfo, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**|  | [optional]
 **certificateNo** | **String**|  | [optional]
 **bizSystem** | **String**|  | [optional]
 **mtToken** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]

### Return type
[**FacepayProxyVerifyUserInfoUserInfoResponseResult**](../model/FacepayProxyVerifyUserInfoUserInfoResponseResult.md)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="oAuth2TokenGenerateToken"></a>
# **oAuth2TokenGenerateToken**
OAuth2TokenGenerateTokenResponse oAuth2TokenGenerateToken(OAuth2TokenGenerateTokenRequest request)

生成token

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//OAuth2TokenGenerateTokenRequest中的参数说明参见Parameters章节
OAuth2TokenGenerateTokenRequest request = new OAuth2TokenGenerateTokenRequest();
request.setUserId("userId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OAuth2TokenGenerateTokenResponse response = api.oAuth2TokenGenerateToken(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#oAuth2TokenGenerateToken, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userId** | **String**|  | [optional]

### Return type
[**OAuth2TokenGenerateTokenOAuth2TokenResponseResult**](../model/OAuth2TokenGenerateTokenOAuth2TokenResponseResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="sosDeleteBindNo"></a>
# **sosDeleteBindNo**
SosDeleteBindNoResponse sosDeleteBindNo(SosDeleteBindNoRequest request)

删除绑卡编号

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.facepay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FacepayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FacepayClient api = FacepayClientBuilder.builder().build();

//SosDeleteBindNoRequest中的参数说明参见Parameters章节
SosDeleteBindNoRequest request = new SosDeleteBindNoRequest();
request.setString0("string0_example");
request.setString1("string1_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SosDeleteBindNoResponse response = api.sosDeleteBindNo(request);
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FacepayClient#sosDeleteBindNo, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **string0** | **String**|  | [optional]
 **string1** | **String**|  | [optional]

### Return type
null (empty response body)

### Authorization
YOP-OAUTH2


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

