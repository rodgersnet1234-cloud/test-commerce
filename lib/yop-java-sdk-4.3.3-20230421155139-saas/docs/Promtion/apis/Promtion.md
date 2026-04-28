# PromtionClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pointCreate**](PromtionClient.md#pointCreate) | **POST** /rest/v1.0/promtion/point/create | 营销积分账户开立
[**pointOperate**](PromtionClient.md#pointOperate) | **POST** /rest/v1.0/promtion/point/operate | 营销账户积分变更
[**pointQuery**](PromtionClient.md#pointQuery) | **GET** /rest/v1.0/promtion/point/query | 营销账户积分查询
[**subsidyApply**](PromtionClient.md#subsidyApply) | **POST** /rest/v1.0/promtion/subsidy/apply | 申请营销补贴
[**subsidyBack**](PromtionClient.md#subsidyBack) | **POST** /rest/v1.0/promtion/subsidy/back | 申请营销补贴退回
[**subsidyBackQuery**](PromtionClient.md#subsidyBackQuery) | **GET** /rest/v1.0/promtion/subsidy/back/query | 查询营销补贴退回
[**subsidyQuery**](PromtionClient.md#subsidyQuery) | **GET** /rest/v1.0/promtion/subsidy/query | 查询营销补贴


<a name="pointCreate"></a>
# **pointCreate**
PointCreateResponse pointCreate(PointCreateRequest request)

营销积分账户开立

营销积分账户开立

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//PointCreateRequest中的参数说明参见Parameters章节
PointCreateRequest request = new PointCreateRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PointCreateResponse response = api.pointCreate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#pointCreate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]

### Return type
[**PointCreateAccountCreateResponseDTOResult**](../model/PointCreateAccountCreateResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="pointOperate"></a>
# **pointOperate**
PointOperateResponse pointOperate(PointOperateRequest request)

营销账户积分变更

营销账户积分变更

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//PointOperateRequest中的参数说明参见Parameters章节
PointOperateRequest request = new PointOperateRequest();
request.setRequestId("requestId_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setPoint(new BigDecimal("0"));
request.setPayDirection("payDirection_example");
request.setRemark("remark_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PointOperateResponse response = api.pointOperate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#pointOperate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestId** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **point** | **BigDecimal**|  | [optional]
 **payDirection** | **String**|  | [optional]
 **remark** | **String**|  | [optional]

### Return type
[**PointOperatePointAccountOperateResponseDTOResult**](../model/PointOperatePointAccountOperateResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="pointQuery"></a>
# **pointQuery**
PointQueryResponse pointQuery(PointQueryRequest request)

营销账户积分查询

营销账户积分查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//PointQueryRequest中的参数说明参见Parameters章节
PointQueryRequest request = new PointQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PointQueryResponse response = api.pointQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#pointQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 业务发起商编 |
 **merchantNo** | **String**| 商户编号 |
 **merchantUserNo** | **String**| 商户用户ID |

### Return type
[**PointQueryPointAccountQueryResponseDTOResult**](../model/PointQueryPointAccountQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="subsidyApply"></a>
# **subsidyApply**
SubsidyApplyResponse subsidyApply(SubsidyApplyRequest request)

申请营销补贴

商户申请营销补贴

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//SubsidyApplyRequest中的参数说明参见Parameters章节
SubsidyApplyRequest request = new SubsidyApplyRequest();
request.setOrderId("orderId_example");
request.setUniqueOrderNo("1001201612070000000000000565");
request.setSubsidyRequestId("subsidyRequestId_example");
request.setSubsidyAmount("12.34");
request.setAssumeMerchantNo("assumeMerchantNo_example");
request.setMemo("memo_example");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SubsidyApplyResponse response = api.subsidyApply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#subsidyApply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **subsidyRequestId** | **String**|  | [optional]
 **subsidyAmount** | **String**|  | [optional]
 **assumeMerchantNo** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**SubsidyApplyYopSubsidyResDTOResult**](../model/SubsidyApplyYopSubsidyResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="subsidyBack"></a>
# **subsidyBack**
SubsidyBackResponse subsidyBack(SubsidyBackRequest request)

申请营销补贴退回

商户申请营销补贴退回

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//SubsidyBackRequest中的参数说明参见Parameters章节
SubsidyBackRequest request = new SubsidyBackRequest();
request.setOrderId("orderId_example");
request.setSubsidyRequestId("subsidyRequestId_example");
request.setSubsidyBackRequestId("subsidyBackRequestId_example");
request.setSubsidyBackAmount("12.34");
request.setReturnAccountType("returnAccountType_example");
request.setMemo("memo_example");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SubsidyBackResponse response = api.subsidyBack(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#subsidyBack, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**|  | [optional]
 **subsidyRequestId** | **String**|  | [optional]
 **subsidyBackRequestId** | **String**|  | [optional]
 **subsidyBackAmount** | **String**|  | [optional]
 **returnAccountType** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**SubsidyBackYopSubsidyBackResDTOResult**](../model/SubsidyBackYopSubsidyBackResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="subsidyBackQuery"></a>
# **subsidyBackQuery**
SubsidyBackQueryResponse subsidyBackQuery(SubsidyBackQueryRequest request)

查询营销补贴退回

商户申请营销补贴退回查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//SubsidyBackQueryRequest中的参数说明参见Parameters章节
SubsidyBackQueryRequest request = new SubsidyBackQueryRequest();
request.setSubsidyRequestId("subsidyRequestId_example");
request.setSubsidyBackRequestId("subsidyBackRequestId_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SubsidyBackQueryResponse response = api.subsidyBackQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#subsidyBackQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subsidyRequestId** | **String**| 商户补贴请求号 |
 **subsidyBackRequestId** | **String**| 商户补贴退回请求号 |
 **parentMerchantNo** | **String**| 发起方商户编号(与交易下单传入保持一致) |
 **merchantNo** | **String**| 收款商户编号 |

### Return type
[**SubsidyBackQueryYopQuerySubsidyBackResDTOResult**](../model/SubsidyBackQueryYopQuerySubsidyBackResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="subsidyQuery"></a>
# **subsidyQuery**
SubsidyQueryResponse subsidyQuery(SubsidyQueryRequest request)

查询营销补贴

商户申请营销补贴查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.promtion.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PromtionClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PromtionClient api = PromtionClientBuilder.builder().build();

//SubsidyQueryRequest中的参数说明参见Parameters章节
SubsidyQueryRequest request = new SubsidyQueryRequest();
request.setOrderId("orderId_example");
request.setSubsidyRequestId("subsidyRequestId_example");
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10012426723");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SubsidyQueryResponse response = api.subsidyQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PromtionClient#subsidyQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **String**| 商户收款请求号 |
 **subsidyRequestId** | **String**| 商户营销补贴请求号 |
 **parentMerchantNo** | **String**| 发起方商户编号(与交易下单传入保持一致) |
 **merchantNo** | **String**| 收款商户编号 |

### Return type
[**SubsidyQueryYopQuerySubsidyResDTOResult**](../model/SubsidyQueryYopQuerySubsidyResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

