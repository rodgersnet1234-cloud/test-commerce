# FrontcashierClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**agreementNosmsbind**](FrontcashierClient.md#agreementNosmsbind) | **POST** /rest/v1.0/frontcashier/agreement/nosmsbind | 存量签约
[**bankTransferPay**](FrontcashierClient.md#bankTransferPay) | **POST** /rest/v1.0/frontcashier/bank-transfer/pay | 银行转账支付
[**bankTransferQuery**](FrontcashierClient.md#bankTransferQuery) | **GET** /rest/v1.0/frontcashier/bank-transfer/query | 银行转账查询
[**bindcardConfirm**](FrontcashierClient.md#bindcardConfirm) | **POST** /rest/v1.0/frontcashier/bindcard/confirm | 绑卡-短验确认
[**bindcardConfirmV2**](FrontcashierClient.md#bindcardConfirmV2) | **POST** /rest/v2.0/frontcashier/bindcard/confirm | 中台绑卡-短验确认
[**bindcardGetcardbin**](FrontcashierClient.md#bindcardGetcardbin) | **POST** /rest/v1.0/frontcashier/bindcard/getcardbin | 银行卡卡bin识别
[**bindcardPayerrequest**](FrontcashierClient.md#bindcardPayerrequest) | **POST** /rest/v1.0/frontcashier/bindcard/payerrequest | 付款方签约
[**bindcardQueryorder**](FrontcashierClient.md#bindcardQueryorder) | **POST** /rest/v1.0/frontcashier/bindcard/queryorder | 查询签约/绑卡请求
[**bindcardQueryorderinfo**](FrontcashierClient.md#bindcardQueryorderinfo) | **GET** /rest/v1.0/frontcashier/bindcard/queryorderinfo | 签约/绑卡订单查询
[**bindcardRequest**](FrontcashierClient.md#bindcardRequest) | **POST** /rest/v1.0/frontcashier/bindcard/request | 绑卡-绑卡请求
[**bindcardRequestV2**](FrontcashierClient.md#bindcardRequestV2) | **POST** /rest/v2.0/frontcashier/bindcard/request | 中台绑卡-绑卡请求
[**bindpayConfirm**](FrontcashierClient.md#bindpayConfirm) | **POST** /rest/v1.0/frontcashier/bindpay/confirm | 绑卡支付-确认支付
[**bindpayRequest**](FrontcashierClient.md#bindpayRequest) | **POST** /rest/v1.0/frontcashier/bindpay/request | 绑卡支付-支付下单
[**bindpaySendsms**](FrontcashierClient.md#bindpaySendsms) | **POST** /rest/v1.0/frontcashier/bindpay/sendsms | 绑卡支付-请求发短验
[**fastbindcardRequest**](FrontcashierClient.md#fastbindcardRequest) | **POST** /rest/v1.0/frontcashier/fastbindcard/request | 查询本人银行卡并签约绑卡
[**getcardbin**](FrontcashierClient.md#getcardbin) | **POST** /rest/v1.0/frontcashier/getcardbin | 银行卡bin识别
[**upopActivescanPay**](FrontcashierClient.md#upopActivescanPay) | **POST** /rest/v1.0/frontcashier/upop/activescan/pay | 付款方主扫下单
[**upopActivescanQuerycoupon**](FrontcashierClient.md#upopActivescanQuerycoupon) | **GET** /rest/v1.0/frontcashier/upop/activescan/querycoupon | 【NOP】银联主扫查询优惠信息
[**upopActivescanQuerypayeeorder**](FrontcashierClient.md#upopActivescanQuerypayeeorder) | **POST** /rest/v1.0/frontcashier/upop/activescan/querypayeeorder | 收款方订单信息查询
[**upopActivescanQuerypayresult**](FrontcashierClient.md#upopActivescanQuerypayresult) | **POST** /rest/v1.0/frontcashier/upop/activescan/querypayresult | 付款订单状态查询
[**upopPassivescanValidate**](FrontcashierClient.md#upopPassivescanValidate) | **POST** /rest/v1.0/frontcashier/upop/passivescan/validate | 付款方验密回调
[**yjzfBindpayrequest**](FrontcashierClient.md#yjzfBindpayrequest) | **POST** /rest/v1.0/frontcashier/yjzf/bindpayrequest | 一键支付-二次支付下单
[**yjzfFirstpayrequest**](FrontcashierClient.md#yjzfFirstpayrequest) | **POST** /rest/v1.0/frontcashier/yjzf/firstpayrequest | 一键支付-首次支付下单
[**yjzfPaymentconfirm**](FrontcashierClient.md#yjzfPaymentconfirm) | **POST** /rest/v1.0/frontcashier/yjzf/paymentconfirm | 一键支付-确认支付
[**yjzfSendsms**](FrontcashierClient.md#yjzfSendsms) | **POST** /rest/v1.0/frontcashier/yjzf/sendsms | 一键支付-请求发验证码


<a name="agreementNosmsbind"></a>
# **agreementNosmsbind**
AgreementNosmsbindResponse agreementNosmsbind(AgreementNosmsbindRequest request)

存量签约

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//AgreementNosmsbindRequest中的参数说明参见Parameters章节
AgreementNosmsbindRequest request = new AgreementNosmsbindRequest();
request.setMerchantFlowId("merchantFlowId_example");
request.setUserNo("userNo_example");
request.setBankCardNo("bankCardNo_example");
request.setIdCardNo("idCardNo_example");
request.setIdCardType("idCardType_example");
request.setUserName("userName_example");
request.setPhone("159****8288");
request.setCvv("cvv_example");
request.setValid("valid_example");
request.setParentMerchantNo("parentMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AgreementNosmsbindResponse response = api.agreementNosmsbind(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#agreementNosmsbind, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantFlowId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **phone** | **String**|  | [optional]
 **cvv** | **String**|  | [optional]
 **valid** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**AgreementNosmsbindAgreementBindCardResponseDTOResult**](../model/AgreementNosmsbindAgreementBindCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankTransferPay"></a>
# **bankTransferPay**
BankTransferPayResponse bankTransferPay(BankTransferPayRequest request)

银行转账支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BankTransferPayRequest中的参数说明参见Parameters章节
BankTransferPayRequest request = new BankTransferPayRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:05");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("memo_example");
request.setGoodsName("goodsName_example");
request.setFundProcessType("fundProcessType_example");
request.setCsUrl("csUrl_example");
request.setCheckType("checkType_example");
request.setToken("token_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankTransferPayResponse response = api.bankTransferPay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bankTransferPay, ex:", e);
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
 **csUrl** | **String**|  | [optional]
 **checkType** | **String**|  | [optional]
 **token** | **String**|  | [optional]

### Return type
[**BankTransferPayAPIOfflineTransferResponseDTOResult**](../model/BankTransferPayAPIOfflineTransferResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankTransferQuery"></a>
# **bankTransferQuery**
BankTransferQueryResponse bankTransferQuery(BankTransferQueryRequest request)

银行转账查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BankTransferQueryRequest中的参数说明参见Parameters章节
BankTransferQueryRequest request = new BankTransferQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankTransferQueryResponse response = api.bankTransferQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bankTransferQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **orderId** | **String**| 商户系统内部生成的订单号，需要保持在同一个商户下唯一 |

### Return type
[**BankTransferQueryAPIOfflineTransferQueryResponseDTOResult**](../model/BankTransferQueryAPIOfflineTransferQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardConfirm"></a>
# **bindcardConfirm**
BindcardConfirmResponse bindcardConfirm(BindcardConfirmRequest request)

绑卡-短验确认

&lt;p&gt;该接口提供鉴权绑卡请求短信验证&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardConfirmRequest中的参数说明参见Parameters章节
BindcardConfirmRequest request = new BindcardConfirmRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setEmpower(true);
request.setSmsCode("smsCode_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardConfirmResponse response = api.bindcardConfirm(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardConfirm, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **empower** | **Boolean**|  | [optional]
 **smsCode** | **String**|  | [optional]

### Return type
[**BindcardConfirmOpenAuthBindCardConfirmResponseDTOResult**](../model/BindcardConfirmOpenAuthBindCardConfirmResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardConfirmV2"></a>
# **bindcardConfirmV2**
BindcardConfirmV2Response bindcardConfirmV2(BindcardConfirmV2Request request)

中台绑卡-短验确认

&lt;p&gt;该接口提供鉴权绑卡请求短信验证&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardConfirmV2Request中的参数说明参见Parameters章节
BindcardConfirmV2Request request = new BindcardConfirmV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setSmsCode("smsCode_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardConfirmV2Response response = api.bindcardConfirmV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardConfirmV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **smsCode** | **String**|  | [optional]

### Return type
[**BindcardConfirmV2OpenAuthBindCardConfirmResponseDTOResult**](../model/BindcardConfirmV2OpenAuthBindCardConfirmResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardGetcardbin"></a>
# **bindcardGetcardbin**
BindcardGetcardbinResponse bindcardGetcardbin(BindcardGetcardbinRequest request)

银行卡卡bin识别

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardGetcardbinRequest中的参数说明参见Parameters章节
BindcardGetcardbinRequest request = new BindcardGetcardbinRequest();
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");
request.setBankCardNo("688888888888");
request.setCardType("cardType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardGetcardbinResponse response = api.bindcardGetcardbin(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardGetcardbin, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]

### Return type
[**BindcardGetcardbinOpenQueryCardbinResponseDTOResult**](../model/BindcardGetcardbinOpenQueryCardbinResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardPayerrequest"></a>
# **bindcardPayerrequest**
BindcardPayerrequestResponse bindcardPayerrequest(BindcardPayerrequestRequest request)

付款方签约

付款方签约

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardPayerrequestRequest中的参数说明参见Parameters章节
BindcardPayerrequestRequest request = new BindcardPayerrequestRequest();
request.setBody(new BindcardPayerrequestOpenPayerAuthBindCardRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardPayerrequestResponse response = api.bindcardPayerrequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardPayerrequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**BindcardPayerrequestOpenPayerAuthBindCardRequestDTOParam**](../model/BindcardPayerrequestOpenPayerAuthBindCardRequestDTOParam.md)|  |

### Return type
[**BindcardPayerrequestOpenPayerAuthBindCardResponseDTOResult**](../model/BindcardPayerrequestOpenPayerAuthBindCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bindcardQueryorder"></a>
# **bindcardQueryorder**
BindcardQueryorderResponse bindcardQueryorder(BindcardQueryorderRequest request)

查询签约/绑卡请求

查询签约/绑卡请求

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardQueryorderRequest中的参数说明参见Parameters章节
BindcardQueryorderRequest request = new BindcardQueryorderRequest();
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setNopOrderId("nopOrderId_example");
request.setPhone("phone_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardQueryorderResponse response = api.bindcardQueryorder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardQueryorder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **nopOrderId** | **String**|  | [optional]
 **phone** | **String**|  | [optional]

### Return type
[**BindcardQueryorderOpenQueryOrderResponseDTOResult**](../model/BindcardQueryorderOpenQueryOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardQueryorderinfo"></a>
# **bindcardQueryorderinfo**
BindcardQueryorderinfoResponse bindcardQueryorderinfo(BindcardQueryorderinfoRequest request)

签约/绑卡订单查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardQueryorderinfoRequest中的参数说明参见Parameters章节
BindcardQueryorderinfoRequest request = new BindcardQueryorderinfoRequest();
request.setMerchantNo("10012426723");
request.setMerchantFlowId("order123456789");
request.setNopOrderId("NOP123456");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardQueryorderinfoResponse response = api.bindcardQueryorderinfo(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardQueryorderinfo, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **merchantFlowId** | **String**|  |
 **nopOrderId** | **String**|  | [optional]

### Return type
[**BindcardQueryorderinfoOpenQueryOrderInfoResponseDTOResult**](../model/BindcardQueryorderinfoOpenQueryOrderInfoResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardRequest"></a>
# **bindcardRequest**
BindcardRequestResponse bindcardRequest(BindcardRequestRequest request)

绑卡-绑卡请求

&lt;p&gt;该接口提供绑卡请求,该接口请求成功后需调求短验确认接口完成整个绑卡动作&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardRequestRequest中的参数说明参见Parameters章节
BindcardRequestRequest request = new BindcardRequestRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setBankCardNo("bankCardNo_example");
request.setUserName("userName_example");
request.setIdCardNo("idCardNo_example");
request.setPhone("phone_example");
request.setCvv2("cvv2_example");
request.setValidthru("validthru_example");
request.setRiskParamExt("riskParamExt_example");
request.setOrderValidate(56);
request.setAuthType("authType_example");
request.setEmpower(true);
request.setCardType("cardType_example");
request.setIsSMS(true);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardRequestResponse response = api.bindcardRequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardRequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **phone** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **validthru** | **String**|  | [optional]
 **riskParamExt** | **String**|  | [optional]
 **orderValidate** | **Integer**|  | [optional]
 **authType** | **String**|  | [optional]
 **empower** | **Boolean**|  | [optional]
 **cardType** | **String**|  | [optional]
 **isSMS** | **Boolean**|  | [optional]

### Return type
[**BindcardRequestOpenAuthBindCardResponseDTOResult**](../model/BindcardRequestOpenAuthBindCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindcardRequestV2"></a>
# **bindcardRequestV2**
BindcardRequestV2Response bindcardRequestV2(BindcardRequestV2Request request)

中台绑卡-绑卡请求

&lt;p&gt;该接口提供绑卡请求,该接口请求成功后需调求短验确认接口完成整个绑卡动作&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindcardRequestV2Request中的参数说明参见Parameters章节
BindcardRequestV2Request request = new BindcardRequestV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setBankCardNo("bankCardNo_example");
request.setUserName("userName_example");
request.setIdCardNo("idCardNo_example");
request.setPhone("phone_example");
request.setCvv2("cvv2_example");
request.setValidthru("validthru_example");
request.setOrderValidate(56);
request.setAuthType("authType_example");
request.setCardType("cardType_example");
request.setIsSMS("isSMS_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindcardRequestV2Response response = api.bindcardRequestV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindcardRequestV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **phone** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **validthru** | **String**|  | [optional]
 **orderValidate** | **Integer**|  | [optional]
 **authType** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **isSMS** | **String**|  | [optional]

### Return type
[**BindcardRequestV2OpenAuthBindCardResponseDTOResult**](../model/BindcardRequestV2OpenAuthBindCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindpayConfirm"></a>
# **bindpayConfirm**
BindpayConfirmResponse bindpayConfirm(BindpayConfirmRequest request)

绑卡支付-确认支付

&lt;p&gt;API收银台，绑卡支付，确认支付&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindpayConfirmRequest中的参数说明参见Parameters章节
BindpayConfirmRequest request = new BindpayConfirmRequest();
request.setToken("token_example");
request.setVersion("version_example");
request.setVerifyCode("verifyCode_example");
request.setCardno("cardno_example");
request.setOwner("owner_example");
request.setIdno("idno_example");
request.setPhoneNo("phoneNo_example");
request.setYpMobile("ypMobile_example");
request.setAvlidDate("avlidDate_example");
request.setCvv2("cvv2_example");
request.setIdCardType("idCardType_example");
request.setBankPWD("bankPWD_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindpayConfirmResponse response = api.bindpayConfirm(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindpayConfirm, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]
 **verifyCode** | **String**|  | [optional]
 **cardno** | **String**|  | [optional]
 **owner** | **String**|  | [optional]
 **idno** | **String**|  | [optional]
 **phoneNo** | **String**|  | [optional]
 **ypMobile** | **String**|  | [optional]
 **avlidDate** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **bankPWD** | **String**|  | [optional]

### Return type
[**BindpayConfirmApiBindPayConfirmResponseDTOResult**](../model/BindpayConfirmApiBindPayConfirmResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindpayRequest"></a>
# **bindpayRequest**
BindpayRequestResponse bindpayRequest(BindpayRequestRequest request)

绑卡支付-支付下单



### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindpayRequestRequest中的参数说明参见Parameters章节
BindpayRequestRequest request = new BindpayRequestRequest();
request.setToken("token_example");
request.setBindId("bindId_example");
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setUserIp("userIp_example");
request.setVersion("version_example");
request.setExtParamMap("extParamMap_example");
request.setPayMerchantNo("payMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindpayRequestResponse response = api.bindpayRequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindpayRequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **String**|  | [optional]
 **bindId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **version** | **String**|  | [optional]
 **extParamMap** | **String**|  | [optional]
 **payMerchantNo** | **String**|  | [optional]

### Return type
[**BindpayRequestApiBindPayPaymentResponseDTOResult**](../model/BindpayRequestApiBindPayPaymentResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bindpaySendsms"></a>
# **bindpaySendsms**
BindpaySendsmsResponse bindpaySendsms(BindpaySendsmsRequest request)

绑卡支付-请求发短验

&lt;p&gt;API收银台，绑卡支付，请求发送验证码&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//BindpaySendsmsRequest中的参数说明参见Parameters章节
BindpaySendsmsRequest request = new BindpaySendsmsRequest();
request.setToken("token_example");
request.setVersion("version_example");
request.setCardno("cardno_example");
request.setOwner("owner_example");
request.setIdno("idno_example");
request.setPhoneNo("phoneNo_example");
request.setYpMobile("ypMobile_example");
request.setAvlidDate("avlidDate_example");
request.setCvv2("cvv2_example");
request.setIdCardType("idCardType_example");
request.setBankPWD("bankPWD_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindpaySendsmsResponse response = api.bindpaySendsms(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#bindpaySendsms, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]
 **cardno** | **String**|  | [optional]
 **owner** | **String**|  | [optional]
 **idno** | **String**|  | [optional]
 **phoneNo** | **String**|  | [optional]
 **ypMobile** | **String**|  | [optional]
 **avlidDate** | **String**|  | [optional]
 **cvv2** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **bankPWD** | **String**|  | [optional]

### Return type
[**BindpaySendsmsApiBindPaySendSmsResponseDTOResult**](../model/BindpaySendsmsApiBindPaySendSmsResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="fastbindcardRequest"></a>
# **fastbindcardRequest**
FastbindcardRequestResponse fastbindcardRequest(FastbindcardRequestRequest request)

查询本人银行卡并签约绑卡

用于查询用户本人在指定银行开立的全部银行卡（可限定卡类型），并由商户选择一张银行卡在银行侧签约开通快捷支付，并完成易宝侧的绑卡。商户通过该接口获取用于查询银行卡并签约的银行页面地址等用于前端页面跳转相关的参数信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//FastbindcardRequestRequest中的参数说明参见Parameters章节
FastbindcardRequestRequest request = new FastbindcardRequestRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setUserName("userName_example");
request.setIdCardNo("idCardNo_example");
request.setIdCardType("idCardType_example");
request.setBankCode("bankCode_example");
request.setCardType("cardType_example");
request.setPageReturnUrl("pageReturnUrl_example");
request.setBindNotifyUrl("bindNotifyUrl_example");
request.setPhone("phone_example");
request.setRiskParamExt("riskParamExt_example");
request.setOrderValidate(56);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FastbindcardRequestResponse response = api.fastbindcardRequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#fastbindcardRequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **pageReturnUrl** | **String**|  | [optional]
 **bindNotifyUrl** | **String**|  | [optional]
 **phone** | **String**|  | [optional]
 **riskParamExt** | **String**|  | [optional]
 **orderValidate** | **Integer**|  | [optional]

### Return type
[**FastbindcardRequestOpenNetsUnionAuthBindCardResponseDTOResult**](../model/FastbindcardRequestOpenNetsUnionAuthBindCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="getcardbin"></a>
# **getcardbin**
GetcardbinResponse getcardbin(GetcardbinRequest request)

银行卡bin识别

银行卡bin识别

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//GetcardbinRequest中的参数说明参见Parameters章节
GetcardbinRequest request = new GetcardbinRequest();
request.setBankCardNo("bankCardNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    GetcardbinResponse response = api.getcardbin(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#getcardbin, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bankCardNo** | **String**|  | [optional]

### Return type
[**GetcardbinRecognizeCardBinResponseDTOResult**](../model/GetcardbinRecognizeCardBinResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="upopActivescanPay"></a>
# **upopActivescanPay**
UpopActivescanPayResponse upopActivescanPay(UpopActivescanPayRequest request)

付款方主扫下单

付款方主扫下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//UpopActivescanPayRequest中的参数说明参见Parameters章节
UpopActivescanPayRequest request = new UpopActivescanPayRequest();
request.setMerchantNo("merchantNo_example");
request.setMerchantFlowId("merchantFlowId_example");
request.setPaySerialNo("paySerialNo_example");
request.setCouponSerialNo("couponSerialNo_example");
request.setTradeAmount(new BigDecimal("0"));
request.setBindId(789L);
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setCallBackUrl("callBackUrl_example");
request.setPayComments("payComments_example");
request.setDeviceID("deviceID_example");
request.setDeviceType("deviceType_example");
request.setAccountIDHash("accountIDHash_example");
request.setSourceIP("sourceIP_example");
request.setUsrRgstrDt("2023-05-07");
request.setAccountEmailLife("accountEmailLife_example");
request.setDeviceLocation("deviceLocation_example");
request.setFullDeviceNumber("fullDeviceNumber_example");
request.setCaptureMethod("captureMethod_example");
request.setDeviceSimNumber("deviceSimNumber_example");
request.setDeviceName("deviceName_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpopActivescanPayResponse response = api.upopActivescanPay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#upopActivescanPay, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **merchantFlowId** | **String**|  | [optional]
 **paySerialNo** | **String**|  | [optional]
 **couponSerialNo** | **String**|  | [optional]
 **tradeAmount** | **BigDecimal**|  | [optional]
 **bindId** | **Long**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **callBackUrl** | **String**|  | [optional]
 **payComments** | **String**|  | [optional]
 **deviceID** | **String**|  | [optional]
 **deviceType** | **String**|  | [optional]
 **accountIDHash** | **String**|  | [optional]
 **sourceIP** | **String**|  | [optional]
 **usrRgstrDt** | **String**|  | [optional]
 **accountEmailLife** | **String**|  | [optional]
 **deviceLocation** | **String**|  | [optional]
 **fullDeviceNumber** | **String**|  | [optional]
 **captureMethod** | **String**|  | [optional]
 **deviceSimNumber** | **String**|  | [optional]
 **deviceName** | **String**|  | [optional]

### Return type
[**UpopActivescanPayOpenActiveScanPayResponseDTOResult**](../model/UpopActivescanPayOpenActiveScanPayResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="upopActivescanQuerycoupon"></a>
# **upopActivescanQuerycoupon**
UpopActivescanQuerycouponResponse upopActivescanQuerycoupon(UpopActivescanQuerycouponRequest request)

【NOP】银联主扫查询优惠信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//UpopActivescanQuerycouponRequest中的参数说明参见Parameters章节
UpopActivescanQuerycouponRequest request = new UpopActivescanQuerycouponRequest();
request.setMerchantFlowId("221007104428249784269");
request.setPaySerialNo("paySerialNo_example");
request.setTradeAmount(new BigDecimal("0"));
request.setBindId(123456L);
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setRiskInfoDeviceID("riskInfoDeviceID_example");
request.setRiskInfoDeviceType("riskInfoDeviceType_example");
request.setRiskInfoAccountIDHash("riskInfoAccountIDHash_example");
request.setRiskInfoSourceIP("riskInfoSourceIP_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpopActivescanQuerycouponResponse response = api.upopActivescanQuerycoupon(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#upopActivescanQuerycoupon, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantFlowId** | **String**|  |
 **paySerialNo** | **String**|  |
 **tradeAmount** | **BigDecimal**| 99.99 |
 **bindId** | **Long**|  |
 **userNo** | **String**|  |
 **userType** | **String**| 用户标识类型&lt;br&gt;可选项如下:&lt;br&gt;USER_ID:用户ID&lt;br&gt;IMEI:imei&lt;br&gt;MAC:网卡地址&lt;br&gt;EMAIL:用户注册地址&lt;br&gt;PHONE:用户注册手机号&lt;br&gt;ID_CARD:用户身份证号&lt;br&gt;AGREEMENT_NO:用户纸质订单协议号&lt;br&gt;WECHAT:微信号 |
 **riskInfoDeviceID** | **String**|  |
 **riskInfoDeviceType** | **String**| 设备类型&lt;br&gt;可选项如下:&lt;br&gt;PHONE:手机&lt;br&gt;TABLET:平板&lt;br&gt;PC:电脑&lt;br&gt;WATCH:只能手表 |
 **riskInfoAccountIDHash** | **String**| 应用提供方下的用户登录账号的hash值 |
 **riskInfoSourceIP** | **String**|  |

### Return type
[**UpopActivescanQuerycouponOpenQueryCouponInfoResponseDTOResult**](../model/UpopActivescanQuerycouponOpenQueryCouponInfoResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="upopActivescanQuerypayeeorder"></a>
# **upopActivescanQuerypayeeorder**
UpopActivescanQuerypayeeorderResponse upopActivescanQuerypayeeorder(UpopActivescanQuerypayeeorderRequest request)

收款方订单信息查询

收款方订单信息查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//UpopActivescanQuerypayeeorderRequest中的参数说明参见Parameters章节
UpopActivescanQuerypayeeorderRequest request = new UpopActivescanQuerypayeeorderRequest();
request.setMerchantFlowId("merchantFlowId_example");
request.setQrCode("qrCode_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpopActivescanQuerypayeeorderResponse response = api.upopActivescanQuerypayeeorder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#upopActivescanQuerypayeeorder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantFlowId** | **String**|  | [optional]
 **qrCode** | **String**|  | [optional]

### Return type
[**UpopActivescanQuerypayeeorderOpenQueryPayeeOrderInfoResponseDTOResult**](../model/UpopActivescanQuerypayeeorderOpenQueryPayeeOrderInfoResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="upopActivescanQuerypayresult"></a>
# **upopActivescanQuerypayresult**
UpopActivescanQuerypayresultResponse upopActivescanQuerypayresult(UpopActivescanQuerypayresultRequest request)

付款订单状态查询

付款订单状态查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//UpopActivescanQuerypayresultRequest中的参数说明参见Parameters章节
UpopActivescanQuerypayresultRequest request = new UpopActivescanQuerypayresultRequest();
request.setBody(new UpopActivescanQuerypayresultOpenQueryActiveScanPayResultRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpopActivescanQuerypayresultResponse response = api.upopActivescanQuerypayresult(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#upopActivescanQuerypayresult, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**UpopActivescanQuerypayresultOpenQueryActiveScanPayResultRequestDTOParam**](../model/UpopActivescanQuerypayresultOpenQueryActiveScanPayResultRequestDTOParam.md)|  |

### Return type
[**UpopActivescanQuerypayresultOpenQueryActiveScanPayResultResponseDTOResult**](../model/UpopActivescanQuerypayresultOpenQueryActiveScanPayResultResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="upopPassivescanValidate"></a>
# **upopPassivescanValidate**
UpopPassivescanValidateResponse upopPassivescanValidate(UpopPassivescanValidateRequest request)

付款方验密回调

付款方验密回调

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//UpopPassivescanValidateRequest中的参数说明参见Parameters章节
UpopPassivescanValidateRequest request = new UpopPassivescanValidateRequest();
request.setMerchantFlowId("merchantFlowId_example");
request.setPayOrderNo("payOrderNo_example");
request.setCouponInfo("couponInfo_example");
request.setRealTradeAmount(new BigDecimal("0"));

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpopPassivescanValidateResponse response = api.upopPassivescanValidate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#upopPassivescanValidate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantFlowId** | **String**|  | [optional]
 **payOrderNo** | **String**|  | [optional]
 **couponInfo** | **String**|  | [optional]
 **realTradeAmount** | **BigDecimal**|  | [optional]

### Return type
[**UpopPassivescanValidateOpenPassiveValidateResponseDTOResult**](../model/UpopPassivescanValidateOpenPassiveValidateResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="yjzfBindpayrequest"></a>
# **yjzfBindpayrequest**
YjzfBindpayrequestResponse yjzfBindpayrequest(YjzfBindpayrequestRequest request)

一键支付-二次支付下单

API收银台-一键支付-二次支付下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//YjzfBindpayrequestRequest中的参数说明参见Parameters章节
YjzfBindpayrequestRequest request = new YjzfBindpayrequestRequest();
request.setBindId("bindId_example");
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setUserIp("userIp_example");
request.setPaymentExt("paymentExt_example");
request.setToken("token_example");
request.setVersion("version_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YjzfBindpayrequestResponse response = api.yjzfBindpayrequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#yjzfBindpayrequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bindId** | **String**|  | [optional]
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **paymentExt** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]

### Return type
[**YjzfBindpayrequestAPIYJZFBindPaymentResponseDTOResult**](../model/YjzfBindpayrequestAPIYJZFBindPaymentResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="yjzfFirstpayrequest"></a>
# **yjzfFirstpayrequest**
YjzfFirstpayrequestResponse yjzfFirstpayrequest(YjzfFirstpayrequestRequest request)

一键支付-首次支付下单

API收银台-一键支付-首次支付下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//YjzfFirstpayrequestRequest中的参数说明参见Parameters章节
YjzfFirstpayrequestRequest request = new YjzfFirstpayrequestRequest();
request.setUserNo("userNo_example");
request.setUserType("userType_example");
request.setUserIp("userIp_example");
request.setCardNo("cardNo_example");
request.setOwner("owner_example");
request.setIdNo("idNo_example");
request.setPhoneNo("phoneNo_example");
request.setCvv("cvv_example");
request.setAvlidDate("avlidDate_example");
request.setPaymentExt("paymentExt_example");
request.setToken("token_example");
request.setVersion("version_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YjzfFirstpayrequestResponse response = api.yjzfFirstpayrequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#yjzfFirstpayrequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userNo** | **String**|  | [optional]
 **userType** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **cardNo** | **String**|  | [optional]
 **owner** | **String**|  | [optional]
 **idNo** | **String**|  | [optional]
 **phoneNo** | **String**|  | [optional]
 **cvv** | **String**|  | [optional]
 **avlidDate** | **String**|  | [optional]
 **paymentExt** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]

### Return type
[**YjzfFirstpayrequestAPIYJZFFirstPaymentResponseDTOResult**](../model/YjzfFirstpayrequestAPIYJZFFirstPaymentResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="yjzfPaymentconfirm"></a>
# **yjzfPaymentconfirm**
YjzfPaymentconfirmResponse yjzfPaymentconfirm(YjzfPaymentconfirmRequest request)

一键支付-确认支付

API收银台-一键支付-确认支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//YjzfPaymentconfirmRequest中的参数说明参见Parameters章节
YjzfPaymentconfirmRequest request = new YjzfPaymentconfirmRequest();
request.setRecordId("recordId_example");
request.setVerifyCode("verifyCode_example");
request.setOwner("owner_example");
request.setIdNo("idNo_example");
request.setPhoneNo("phoneNo_example");
request.setCvv("cvv_example");
request.setAvlidDate("avlidDate_example");
request.setBankPWD("bankPWD_example");
request.setPaymentExt("paymentExt_example");
request.setToken("token_example");
request.setVersion("version_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YjzfPaymentconfirmResponse response = api.yjzfPaymentconfirm(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#yjzfPaymentconfirm, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recordId** | **String**|  | [optional]
 **verifyCode** | **String**|  | [optional]
 **owner** | **String**|  | [optional]
 **idNo** | **String**|  | [optional]
 **phoneNo** | **String**|  | [optional]
 **cvv** | **String**|  | [optional]
 **avlidDate** | **String**|  | [optional]
 **bankPWD** | **String**|  | [optional]
 **paymentExt** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]

### Return type
[**YjzfPaymentconfirmAPIYJZFConfirmPayResponseDTOResult**](../model/YjzfPaymentconfirmAPIYJZFConfirmPayResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="yjzfSendsms"></a>
# **yjzfSendsms**
YjzfSendsmsResponse yjzfSendsms(YjzfSendsmsRequest request)

一键支付-请求发验证码

API收银台-一键支付-请求发验证码

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.frontcashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(FrontcashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
FrontcashierClient api = FrontcashierClientBuilder.builder().build();

//YjzfSendsmsRequest中的参数说明参见Parameters章节
YjzfSendsmsRequest request = new YjzfSendsmsRequest();
request.setRecordId("recordId_example");
request.setOwner("owner_example");
request.setIdNo("idNo_example");
request.setPhoneNo("phoneNo_example");
request.setCvv("cvv_example");
request.setAvlidDate("avlidDate_example");
request.setBankPWD("bankPWD_example");
request.setPaymentExt("paymentExt_example");
request.setToken("token_example");
request.setVersion("version_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YjzfSendsmsResponse response = api.yjzfSendsms(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling FrontcashierClient#yjzfSendsms, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recordId** | **String**|  | [optional]
 **owner** | **String**|  | [optional]
 **idNo** | **String**|  | [optional]
 **phoneNo** | **String**|  | [optional]
 **cvv** | **String**|  | [optional]
 **avlidDate** | **String**|  | [optional]
 **bankPWD** | **String**|  | [optional]
 **paymentExt** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **version** | **String**|  | [optional]

### Return type
[**YjzfSendsmsAPIBasicResponseDTOResult**](../model/YjzfSendsmsAPIBasicResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

