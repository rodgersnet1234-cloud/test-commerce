# AggpayClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**complaintWechatDetails**](AggpayClient.md#complaintWechatDetails) | **GET** /rest/v1.0/aggpay/complaint/wechat/details | 查询投诉订单详情
[**complaintWechatFeedback**](AggpayClient.md#complaintWechatFeedback) | **POST** /rest/v1.0/aggpay/complaint/wechat/feedback | 回复用户处理内容
[**complaintWechatList**](AggpayClient.md#complaintWechatList) | **GET** /rest/v1.0/aggpay/complaint/wechat/list | 查询投诉订单列表
[**complaintWechatNegotiationHistory**](AggpayClient.md#complaintWechatNegotiationHistory) | **GET** /rest/v1.0/aggpay/complaint/wechat/negotiation-history | 查询投诉协商历史
[**pay**](AggpayClient.md#pay) | **POST** /rest/v1.0/aggpay/pay | 付款码支付
[**payLink**](AggpayClient.md#payLink) | **POST** /rest/v1.0/aggpay/pay-link | 生成聚合订单码
[**prePay**](AggpayClient.md#prePay) | **POST** /rest/v1.0/aggpay/pre-pay | 聚合支付统一下单
[**queryUserid**](AggpayClient.md#queryUserid) | **POST** /rest/v1.0/aggpay/query-userid | 付款码查询用户ID
[**tutelagePrePay**](AggpayClient.md#tutelagePrePay) | **POST** /rest/v1.0/aggpay/tutelage/pre-pay | 聚合支付托管下单
[**violationWechatChannel**](AggpayClient.md#violationWechatChannel) | **GET** /rest/v1.0/aggpay/violation/wechat/channel | 微信违规查询接口(服务商/平台商版)
[**wechatConfigAdd**](AggpayClient.md#wechatConfigAdd) | **POST** /rest/v1.0/aggpay/wechat-config/add | 公众号配置接口
[**wechatConfigAddV2**](AggpayClient.md#wechatConfigAddV2) | **POST** /rest/v2.0/aggpay/wechat-config/add | 公众号配置接口
[**wechatConfigQuery**](AggpayClient.md#wechatConfigQuery) | **GET** /rest/v1.0/aggpay/wechat-config/query | 公众号配置查询
[**wechatConfigQueryV2**](AggpayClient.md#wechatConfigQueryV2) | **GET** /rest/v2.0/aggpay/wechat-config/query | 公众号配置查询


<a name="complaintWechatDetails"></a>
# **complaintWechatDetails**
ComplaintWechatDetailsResponse complaintWechatDetails(ComplaintWechatDetailsRequest request)

查询投诉订单详情

商户可通过调用此接口，查询指定投诉单的用户投诉详情，包含投诉内容、投诉关联订单、投诉人联系方式等信息，方便商户处理投诉。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//ComplaintWechatDetailsRequest中的参数说明参见Parameters章节
ComplaintWechatDetailsRequest request = new ComplaintWechatDetailsRequest();
request.setComplaintNo("complaintNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ComplaintWechatDetailsResponse response = api.complaintWechatDetails(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#complaintWechatDetails, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **complaintNo** | **String**| 投诉单号 |

### Return type
[**ComplaintWechatDetailsWechatComplaintInfoFlatResponseDTOResult**](../model/ComplaintWechatDetailsWechatComplaintInfoFlatResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="complaintWechatFeedback"></a>
# **complaintWechatFeedback**
ComplaintWechatFeedbackResponse complaintWechatFeedback(ComplaintWechatFeedbackRequest request)

回复用户处理内容

商户可通过调用此接口，提交回复内容或反馈投诉单已处理完成。其中上传图片凭证需首先调用【子商户入网资质文件上传】接口，得到图片URL，再将URL填入请求。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//ComplaintWechatFeedbackRequest中的参数说明参见Parameters章节
ComplaintWechatFeedbackRequest request = new ComplaintWechatFeedbackRequest();
request.setComplaintNo("200201820200101080076610000");
request.setFeedbackContent("已与用户沟通解决");
request.setImageList("[\"https://qpic.cn/xx1\",\"https://qpic.cn/xxx2\"]");
request.setFeedbackType("GENERAL");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ComplaintWechatFeedbackResponse response = api.complaintWechatFeedback(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#complaintWechatFeedback, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **complaintNo** | **String**|  | [optional]
 **feedbackContent** | **String**|  | [optional]
 **imageList** | **String**|  | [optional]
 **feedbackType** | **String**|  | [optional]

### Return type
[**ComplaintWechatFeedbackBaseResponseDTOResult**](../model/ComplaintWechatFeedbackBaseResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="complaintWechatList"></a>
# **complaintWechatList**
ComplaintWechatListResponse complaintWechatList(ComplaintWechatListRequest request)

查询投诉订单列表

对于SAAS服务商、平台商、标准商户可通过调用此接口，查询指定时间段的所有用户投诉信息；也可通过调用此接口，查询指定子商户编号对应子商户的投诉信息，若不指定则查询所有子商户投诉信息。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//ComplaintWechatListRequest中的参数说明参见Parameters章节
ComplaintWechatListRequest request = new ComplaintWechatListRequest();
request.setStartTime("2022-05-01");
request.setEndTime("2022-06-01");
request.setMerchantOrderNo("20220906154617947762222");
request.setWechatOrderNo("4200000404201909069117582536");
request.setMerchantNo("10083213321");
request.setPage(56);
request.setLimit(56);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ComplaintWechatListResponse response = api.complaintWechatList(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#complaintWechatList, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startTime** | **String**| 投诉发生的开始日期，格式为yyyy-MM-dd。&lt;br&gt;注意，查询日期跨度不超过30天 |
 **endTime** | **String**| 投诉发生的结束日期，格式为yyyy-MM-dd。&lt;br&gt;注意，查询日期跨度不超过30天 |
 **merchantOrderNo** | **String**| 投诉单关联的易宝商户订单号 | [optional]
 **wechatOrderNo** | **String**| 投诉单关联的微信订单号 | [optional]
 **merchantNo** | **String**| 投诉单对应的易宝商户编号 | [optional]
 **page** | **Integer**| 默认1，最小为1 | [optional]
 **limit** | **Integer**| 默认20，设置该次请求返回的最大投诉条数，范围【1,100】 | [optional]

### Return type
[**ComplaintWechatListWechatComplaintListFlatResponseDTOResult**](../model/ComplaintWechatListWechatComplaintListFlatResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="complaintWechatNegotiationHistory"></a>
# **complaintWechatNegotiationHistory**
ComplaintWechatNegotiationHistoryResponse complaintWechatNegotiationHistory(ComplaintWechatNegotiationHistoryRequest request)

查询投诉协商历史

商户可通过调用此接口，查询指定投诉的用户/商户协商历史，输出查询结果，方便商户根据处理历史来制定后续处理方案。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//ComplaintWechatNegotiationHistoryRequest中的参数说明参见Parameters章节
ComplaintWechatNegotiationHistoryRequest request = new ComplaintWechatNegotiationHistoryRequest();
request.setComplaintNo("200201820200101080076610000");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ComplaintWechatNegotiationHistoryResponse response = api.complaintWechatNegotiationHistory(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#complaintWechatNegotiationHistory, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **complaintNo** | **String**| 投诉单对应的投诉单号 |

### Return type
[**ComplaintWechatNegotiationHistoryWechatComplaintNegotiationHistoryFlatResponseDTOResult**](../model/ComplaintWechatNegotiationHistoryWechatComplaintNegotiationHistoryFlatResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="pay"></a>
# **pay**
PayResponse pay(PayRequest request)

付款码支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//PayRequest中的参数说明参见Parameters章节
PayRequest request = new PayRequest();
request.setParentMerchantNo("10040012345");
request.setMerchantNo("10040054321");
request.setOrderId("orderId12345");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:07");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setMemo("memo_example");
request.setGoodsName("旺仔牛奶");
request.setFundProcessType("REAL_TIME");
request.setPayWay("MERCHANT_SCAN");
request.setChannel("WECHAT");
request.setScene("OFFLINE");
request.setAuthCode("authCode123");
request.setAppId("appId12345");
request.setUserIp("123.123.123.123");
request.setTerminalId("00000000");
request.setTerminalSceneInfo("{\"storeId\":\"门店id\",\"storeName\":\"门店名称\",\"operatorId\":\"商户操作员编号\",\"alipayStoreId\":\"支付宝的店铺编号\",\"areaCode\":\"门店行政区划码\",\"address\":\"门店详细地址\"}");
request.setChannelSpecifiedInfo("{\"hbFqNum\":\"3\",\"hbFqSellerPercent\":\"0\",\"sysServiceProviderId\":\"\",\"isEnterprisePay\":\"N\"}");
request.setChannelPromotionInfo("channelPromotionInfo_example");
request.setIdentityInfo("{\"identityVerifyType\":\"Y\",\"payerIdType\":\"IDENTITY_CARD\",\"payerNumber\":\"234512198006252456\",\"payerName\":\"名字\"}");
request.setLimitCredit("N");
request.setToken("83BCDF29CFACB4411533080B67864EF8C907CCDC5E10A707C285FEA10CDB8221");
request.setUniqueOrderNo("1012202101070000001989946571");
request.setCsUrl("csUrl_example");
request.setEncryptedPINData("encryptedPINData_example");
request.setPayerAccountNo("payerAccountNo_example");
request.setAccountLinkInfo("{accountProvider\":\"BOL\",\"token\":\"xxx\"}");
request.setBankCode("BOC");
request.setBusinessInfo("businessInfo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayResponse response = api.pay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#pay, ex:", e);
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
 **payWay** | **String**|  | [optional]
 **channel** | **String**|  | [optional]
 **scene** | **String**|  | [optional]
 **authCode** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **terminalId** | **String**|  | [optional]
 **terminalSceneInfo** | **String**|  | [optional]
 **channelSpecifiedInfo** | **String**|  | [optional]
 **channelPromotionInfo** | **String**|  | [optional]
 **identityInfo** | **String**|  | [optional]
 **limitCredit** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **encryptedPINData** | **String**|  | [optional]
 **payerAccountNo** | **String**|  | [optional]
 **accountLinkInfo** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]

### Return type
[**PayPassiveOrderResponseDTOResult**](../model/PayPassiveOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="payLink"></a>
# **payLink**
PayLinkResponse payLink(PayLinkRequest request)

生成聚合订单码

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//PayLinkRequest中的参数说明参见Parameters章节
PayLinkRequest request = new PayLinkRequest();
request.setParentMerchantNo("10040012345");
request.setMerchantNo("10040054321");
request.setOrderId("OrderId12345");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:07");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setMemo("memo_example");
request.setGoodsName("旺仔牛奶");
request.setFundProcessType("REAL_TIME");
request.setScene("OFFLINE");
request.setAppId("appId12345");
request.setChannelSpecifiedInfo("{\"hbFqNum\":\"3\",\"hbFqSellerPercent\":\"0\",\"sysServiceProviderId\":\"\",\"isEnterprisePay\":\"N\"}");
request.setChannelPromotionInfo("channelPromotionInfo_example");
request.setIdentityInfo("{\"identityVerifyType\":\"Y\",\"payerIdType\":\"IDENTITY_CARD\",\"payerNumber\":\"234512198006252456\",\"payerName\":\"名字\"}");
request.setLimitCredit("N");
request.setCsUrl("csUrl_example");
request.setYpPromotionInfo("自定义支付立减：[{\"amount\":\"0.01\",\"type\":\"CUSTOM_REDUCTION\"}],自定义补贴商户[{\"type\":\"CUSTOM_ALLOWANCE\"}]");
request.setBusinessInfo("businessInfo_example");
request.setToken("83BCDF29CFACB4411533080B67864EF8C907CCDC5E10A707C285FEA10CDB8221");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayLinkResponse response = api.payLink(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#payLink, ex:", e);
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
 **scene** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **channelSpecifiedInfo** | **String**|  | [optional]
 **channelPromotionInfo** | **String**|  | [optional]
 **identityInfo** | **String**|  | [optional]
 **limitCredit** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **ypPromotionInfo** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]
 **token** | **String**|  | [optional]

### Return type
[**PayLinkOrderCodeResponseDTOResult**](../model/PayLinkOrderCodeResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="prePay"></a>
# **prePay**
PrePayResponse prePay(PrePayRequest request)

聚合支付统一下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//PrePayRequest中的参数说明参见Parameters章节
PrePayRequest request = new PrePayRequest();
request.setParentMerchantNo("10040012345");
request.setMerchantNo("10040054321");
request.setOrderId("orderId12345");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:07");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setRedirectUrl("https://notify.merchant.com/xxx");
request.setMemo("memo_example");
request.setGoodsName("旺仔牛奶");
request.setFundProcessType("REAL_TIME");
request.setPayWay("USER_SCAN");
request.setChannel("ALIPAY");
request.setScene("OFFLINE");
request.setAppId("appId12345");
request.setUserId("userId12345");
request.setUserIp("123.123.123.123");
request.setChannelSpecifiedInfo("{\"hbFqNum\":\"3\",\"hbFqSellerPercent\":\"0\",\"sysServiceProviderId\":\"\"}");
request.setChannelPromotionInfo("channelPromotionInfo_example");
request.setIdentityInfo("{\"identityVerifyType\":\"Y\",\"payerIdType\":\"IDENTITY_CARD\",\"payerNumber\":\"234512198006252456\",\"payerName\":\"名字\"}");
request.setLimitCredit("N");
request.setToken("83BCDF29CFACB4411533080B67864EF8C907CCDC5E10A707C285FEA10CDB8221");
request.setUniqueOrderNo("1012202101070000001989946571");
request.setCsUrl("csUrl_example");
request.setAccountLinkInfo("{accountProvider\":\"BOL\",\"token\":\"xxx\"}");
request.setYpPromotionInfo("自定义支付立减：[{\"amount\":\"0.01\",\"type\":\"CUSTOM_REDUCTION\"}],自定义补贴商户[{\"type\":\"CUSTOM_ALLOWANCE\"}]");
request.setBankCode("BOC");
request.setBusinessInfo("businessInfo_example");
request.setUserAuthCode("userAuthCode_example");
request.setChannelActivityInfo("channelActivityInfo_example");
request.setTerminalId("terminalId_example");
request.setTerminalSceneInfo("terminalSceneInfo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PrePayResponse response = api.prePay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#prePay, ex:", e);
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
 **redirectUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **payWay** | **String**|  | [optional]
 **channel** | **String**|  | [optional]
 **scene** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **userId** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **channelSpecifiedInfo** | **String**|  | [optional]
 **channelPromotionInfo** | **String**|  | [optional]
 **identityInfo** | **String**|  | [optional]
 **limitCredit** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **accountLinkInfo** | **String**|  | [optional]
 **ypPromotionInfo** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]
 **userAuthCode** | **String**|  | [optional]
 **channelActivityInfo** | **String**|  | [optional]
 **terminalId** | **String**|  | [optional]
 **terminalSceneInfo** | **String**|  | [optional]

### Return type
[**PrePayOrderResponseDTOResult**](../model/PrePayOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="queryUserid"></a>
# **queryUserid**
QueryUseridResponse queryUserid(QueryUseridRequest request)

付款码查询用户ID

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//QueryUseridRequest中的参数说明参见Parameters章节
QueryUseridRequest request = new QueryUseridRequest();
request.setParentMerchantNo("10040012345");
request.setMerchantNo("10040054321");
request.setAppId("appid12345");
request.setAuthCode("authCode123");
request.setChannel("WECHAT");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryUseridResponse response = api.queryUserid(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#queryUserid, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **authCode** | **String**|  | [optional]
 **channel** | **String**|  | [optional]

### Return type
[**QueryUseridPassiveGetUserIdResponseDTOResult**](../model/QueryUseridPassiveGetUserIdResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="tutelagePrePay"></a>
# **tutelagePrePay**
TutelagePrePayResponse tutelagePrePay(TutelagePrePayRequest request)

聚合支付托管下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//TutelagePrePayRequest中的参数说明参见Parameters章节
TutelagePrePayRequest request = new TutelagePrePayRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:07");
request.setMemo("memo_example");
request.setGoodsName("旺仔牛奶");
request.setFundProcessType("REAL_TIME");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setPayWay("SDK_PAY");
request.setChannel("WECHAT");
request.setScene("OFFLINE");
request.setAppId("appId12345");
request.setUserIp("123.123.123.123");
request.setLimitCredit("N");
request.setToken("83BCDF29CFACB4411533080B67864EF8C907CCDC5E10A707C285FEA10CDB8221");
request.setCsUrl("csUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TutelagePrePayResponse response = api.tutelagePrePay(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#tutelagePrePay, ex:", e);
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
 **memo** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **payWay** | **String**|  | [optional]
 **channel** | **String**|  | [optional]
 **scene** | **String**|  | [optional]
 **appId** | **String**|  | [optional]
 **userIp** | **String**|  | [optional]
 **limitCredit** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]

### Return type
[**TutelagePrePayWrapPrePayOrderResponseDTOResult**](../model/TutelagePrePayWrapPrePayOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="violationWechatChannel"></a>
# **violationWechatChannel**
ViolationWechatChannelResponse violationWechatChannel(ViolationWechatChannelRequest request)

微信违规查询接口(服务商/平台商版)

查询商户在微信的违规信息(根据渠道号查询)

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//ViolationWechatChannelRequest中的参数说明参见Parameters章节
ViolationWechatChannelRequest request = new ViolationWechatChannelRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setBeginTime("2023-05-07 10:49:07");
request.setEndTime("2023-05-07 10:49:07");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ViolationWechatChannelResponse response = api.violationWechatChannel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#violationWechatChannel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 服务商/平台商商编 |
 **beginTime** | **String**| 查询的开始时间&lt;br&gt;格式\&quot;yyyy-MM-dd HH:mm:ss\&quot; |
 **endTime** | **String**| 查询的结束时间&lt;br&gt;格式\&quot;yyyy-MM-dd HH:mm:ss\&quot;&lt;br&gt;（开始时间和结束时间间隔不得超过一小时） |

### Return type
[**ViolationWechatChannelWechatRiskQueryResponseDTOResult**](../model/ViolationWechatChannelWechatRiskQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="wechatConfigAdd"></a>
# **wechatConfigAdd**
WechatConfigAddResponse wechatConfigAdd(WechatConfigAddRequest request)

公众号配置接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//WechatConfigAddRequest中的参数说明参见Parameters章节
WechatConfigAddRequest request = new WechatConfigAddRequest();
request.setBody(new WechatConfigAddWechatConfigRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WechatConfigAddResponse response = api.wechatConfigAdd(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#wechatConfigAdd, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**WechatConfigAddWechatConfigRequestDTOParam**](../model/WechatConfigAddWechatConfigRequestDTOParam.md)|  |

### Return type
[**WechatConfigAddWechatConfigResponseDTOResult**](../model/WechatConfigAddWechatConfigResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="wechatConfigAddV2"></a>
# **wechatConfigAddV2**
WechatConfigAddV2Response wechatConfigAddV2(WechatConfigAddV2Request request)

公众号配置接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//WechatConfigAddV2Request中的参数说明参见Parameters章节
WechatConfigAddV2Request request = new WechatConfigAddV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setTradeAuthDirList("[\"http://www.yeepay.com/\",\"http://www.yeepay.com/\"]");
request.setAppIdList("[{\"appId\":\"appId\",\"appSecret\":\"appSecret\",\"appIdType\":\"OFFICIAL_ACCOUNT\",\"subscribeAppId\":\"subscribeAppId\"},{\"appId\":\"appId\",\"appSecret\":\"appSecret\",\"appIdType\":\"MINI_PROGRAM\",\"subscribeAppId\":\"subscribeAppId\"}]");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WechatConfigAddV2Response response = api.wechatConfigAddV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#wechatConfigAddV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **tradeAuthDirList** | **String**|  | [optional]
 **appIdList** | **String**|  | [optional]

### Return type
[**WechatConfigAddV2WechatConfigFlatResponseDTOResult**](../model/WechatConfigAddV2WechatConfigFlatResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="wechatConfigQuery"></a>
# **wechatConfigQuery**
WechatConfigQueryResponse wechatConfigQuery(WechatConfigQueryRequest request)

公众号配置查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//WechatConfigQueryRequest中的参数说明参见Parameters章节
WechatConfigQueryRequest request = new WechatConfigQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setAppIdType("appIdType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WechatConfigQueryResponse response = api.wechatConfigQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#wechatConfigQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **appIdType** | **String**| OFFICIAL_ACCOUNT:公众号&lt;br&gt;MINI_PROGRAM:小程序 | [optional]

### Return type
[**WechatConfigQueryWechatConfigResponseDTOResult**](../model/WechatConfigQueryWechatConfigResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="wechatConfigQueryV2"></a>
# **wechatConfigQueryV2**
WechatConfigQueryV2Response wechatConfigQueryV2(WechatConfigQueryV2Request request)

公众号配置查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.aggpay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AggpayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AggpayClient api = AggpayClientBuilder.builder().build();

//WechatConfigQueryV2Request中的参数说明参见Parameters章节
WechatConfigQueryV2Request request = new WechatConfigQueryV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setAppIdType("appIdType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WechatConfigQueryV2Response response = api.wechatConfigQueryV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AggpayClient#wechatConfigQueryV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **appIdType** | **String**| appId类型&lt;br&gt;OFFICIAL_ACCOUNT:公众号&lt;br&gt;MINI_PROGRAM:小程序 | [optional]

### Return type
[**WechatConfigQueryV2WechatConfigFlatResponseDTOResult**](../model/WechatConfigQueryV2WechatConfigFlatResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

