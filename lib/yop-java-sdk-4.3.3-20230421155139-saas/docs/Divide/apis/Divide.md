# DivideClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apply**](DivideClient.md#apply) | **POST** /rest/v1.0/divide/apply | 申请分账
[**back**](DivideClient.md#back) | **POST** /rest/v1.0/divide/back | 申请分账资金归还
[**backQuery**](DivideClient.md#backQuery) | **GET** /rest/v1.0/divide/back/query | 查询分账资金归还结果
[**backReceiptDownload**](DivideClient.md#backReceiptDownload) | **GET** /yos/v1.0/divide/back/receipt/download | 分账资金归还回单
[**complete**](DivideClient.md#complete) | **POST** /rest/v1.0/divide/complete | 完结分账
[**query**](DivideClient.md#query) | **GET** /rest/v1.0/divide/query | 查询分账结果
[**receiptDownload**](DivideClient.md#receiptDownload) | **GET** /yos/v1.0/divide/receipt/download | 分账回单


<a name="apply"></a>
# **apply**
ApplyResponse apply(ApplyRequest request)

申请分账

订单支付成功后再分账时可以调用本接口实现

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//ApplyRequest中的参数说明参见Parameters章节
ApplyRequest request = new ApplyRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setDivideRequestId("divideRequestId_example");
request.setDivideDetail("[{\"amount\":\"100.00\",\"ledgerNo\":\"10000466938\",\"ledgerType\":\"MERCHANT2MERCHANT\",\"divideDetailDesc\":\"供应商结算\"},{\"amount\":\"100.00\",\"ledgerNo\":\"212345678912\",\"ledgerNoFrom\":\"10000466938\",\"ledgerType\":\"MERCHANT2MEMBER\"}]");
request.setAccountLinkInfo("{\"serviceProvider\":\"YEEPAY\",\"ipAddress\":\"192.168.1.1\",\"divideType\":\"1\",\"token\":\"token\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ApplyResponse response = api.apply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#apply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **divideRequestId** | **String**|  | [optional]
 **divideDetail** | **String**|  | [optional]
 **accountLinkInfo** | **String**|  | [optional]

### Return type
[**ApplyYopOrderDivideResDTOResult**](../model/ApplyYopOrderDivideResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="back"></a>
# **back**
BackResponse back(BackRequest request)

申请分账资金归还



### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//BackRequest中的参数说明参见Parameters章节
BackRequest request = new BackRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setDivideBackRequestId("divideBackRequestId_example");
request.setDivideRequestId("divideRequestId_example");
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setDivideBackDetail("[{\"amount\":\"3.45\",\"divideBackReason\":\"退回原因01\",\"divideDetailNo\":\"1003232421231232\"},{\"amount\":\"2.35\",\"divideBackReason\":\"退回原因02\",\"divideDetailNo\":\"200323242123343\"}]");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BackResponse response = api.back(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#back, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **divideBackRequestId** | **String**|  | [optional]
 **divideRequestId** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **divideBackDetail** | **String**|  | [optional]

### Return type
[**BackYopDivideBackResDTOResult**](../model/BackYopDivideBackResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="backQuery"></a>
# **backQuery**
BackQueryResponse backQuery(BackQueryRequest request)

查询分账资金归还结果

查询分账资金归还结果

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//BackQueryRequest中的参数说明参见Parameters章节
BackQueryRequest request = new BackQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setDivideBackRequestId("divideBackRequestId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BackQueryResponse response = api.backQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#backQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **orderId** | **String**|  |
 **uniqueOrderNo** | **String**|  |
 **divideBackRequestId** | **String**|  |

### Return type
[**BackQueryYopQueryDivideBackResDTOResult**](../model/BackQueryYopQueryDivideBackResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="backReceiptDownload"></a>
# **backReceiptDownload**
BackReceiptDownloadResponse backReceiptDownload(BackReceiptDownloadRequest request)

分账资金归还回单

分账资金归还回单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//BackReceiptDownloadRequest中的参数说明参见Parameters章节
BackReceiptDownloadRequest request = new BackReceiptDownloadRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setDivideBackRequestId("divideBackRequestId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setLedgerNo("ledgerNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BackReceiptDownloadResponse response = api.backReceiptDownload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#backReceiptDownload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| *标准商户收付款方案中此参数与收款商户编号一致；*平台商户收付款方案中此参数为平台商商户编号；*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**| 收款商户商编。单笔收款必传，合单收款场景中上传子单域信息subOrderDetail里的merchantNo |
 **divideBackRequestId** | **String**|  |
 **uniqueOrderNo** | **String**| 收款交易对应的易宝收款订单号 |
 **ledgerNo** | **String**| 分账接收方编号(接收分账资金的易宝商编) |

### Return type
[**BackReceiptDownloadReceiptResponseDTOResult**](../model/BackReceiptDownloadReceiptResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="complete"></a>
# **complete**
CompleteResponse complete(CompleteRequest request)

完结分账

完结分账

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//CompleteRequest中的参数说明参见Parameters章节
CompleteRequest request = new CompleteRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setDivideRequestId("divideRequestId_example");
request.setDivideDetailDesc("divideDetailDesc_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompleteResponse response = api.complete(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#complete, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **divideRequestId** | **String**|  | [optional]
 **divideDetailDesc** | **String**|  | [optional]

### Return type
[**CompleteYopOrderEndDivideResDTOResult**](../model/CompleteYopOrderEndDivideResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="query"></a>
# **query**
QueryResponse query(QueryRequest request)

查询分账结果

调用该接口查询分账结果

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//QueryRequest中的参数说明参见Parameters章节
QueryRequest request = new QueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setDivideRequestId("divideRequestId_example");
request.setOrderId("orderId_example");
request.setUniqueOrderNo("uniqueOrderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryResponse response = api.query(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#query, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**| 收款商户编号 |
 **divideRequestId** | **String**|  |
 **orderId** | **String**| 原支付订单的商户订单号 |
 **uniqueOrderNo** | **String**| 收款交易对应在易宝的单号 |

### Return type
[**QueryYopQueryOrderDivideResDTOResult**](../model/QueryYopQueryOrderDivideResDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="receiptDownload"></a>
# **receiptDownload**
ReceiptDownloadResponse receiptDownload(ReceiptDownloadRequest request)

分账回单

分账回单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.divide.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(DivideClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
DivideClient api = DivideClientBuilder.builder().build();

//ReceiptDownloadRequest中的参数说明参见Parameters章节
ReceiptDownloadRequest request = new ReceiptDownloadRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setDivideRequestId("divideRequestId_example");
request.setLedgerNo("ledgerNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ReceiptDownloadResponse response = api.receiptDownload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling DivideClient#receiptDownload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 交易发起方商编。与交易下单传入的保持一致 |
 **merchantNo** | **String**|  |
 **uniqueOrderNo** | **String**|  |
 **divideRequestId** | **String**|  |
 **ledgerNo** | **String**| 分账接收方编号(接收分账资金的易宝商编) |

### Return type
[**ReceiptDownloadReceiptResponseDTOResult**](../model/ReceiptDownloadReceiptResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

