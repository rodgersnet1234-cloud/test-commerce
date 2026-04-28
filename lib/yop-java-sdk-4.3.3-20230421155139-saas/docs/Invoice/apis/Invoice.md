# InvoiceClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apply**](InvoiceClient.md#apply) | **POST** /rest/v1.0/invoice/apply | 申请开票
[**feeQuery**](InvoiceClient.md#feeQuery) | **GET** /rest/v1.0/invoice/fee/query | 查询手续费
[**infoModify**](InvoiceClient.md#infoModify) | **POST** /rest/v1.0/invoice/info/modify | 添加/修改发票信息
[**infoQuery**](InvoiceClient.md#infoQuery) | **GET** /rest/v1.0/invoice/info/query | 查询发票信息
[**recordQuery**](InvoiceClient.md#recordQuery) | **GET** /rest/v1.0/invoice/record/query | 查询开票记录


<a name="apply"></a>
# **apply**
ApplyResponse apply(ApplyRequest request)

申请开票

商户通过此接口可以申请开票

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.invoice.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InvoiceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InvoiceClient api = InvoiceClientBuilder.builder().build();

//ApplyRequest中的参数说明参见Parameters章节
ApplyRequest request = new ApplyRequest();
request.setMerchantNo("10040040287");
request.setCustomerRequestNo("01e1c1a0509e435091e98fc99f11cb4b");
request.setParentMerchantNo("10040040286");
request.setChargingDateStart("2023-05-07 10:49:08");
request.setChargingDateEnd("2023-05-07 10:49:08");
request.setNotifyUrl("http://172.19.100.117:8001/yop-boss/accept");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ApplyResponse response = api.apply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InvoiceClient#apply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **customerRequestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **chargingDateStart** | **String**|  | [optional]
 **chargingDateEnd** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**ApplyApplyInvoiceYOPResponseDtoResult**](../model/ApplyApplyInvoiceYOPResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="feeQuery"></a>
# **feeQuery**
FeeQueryResponse feeQuery(FeeQueryRequest request)

查询手续费

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.invoice.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InvoiceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InvoiceClient api = InvoiceClientBuilder.builder().build();

//FeeQueryRequest中的参数说明参见Parameters章节
FeeQueryRequest request = new FeeQueryRequest();
request.setMerchantNo("10080009462");
request.setParentMerchantNo("10080009456");
request.setChargingDateStart("2023-05-07 10:49:08");
request.setChargingDateEnd("2023-05-07 10:49:08");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FeeQueryResponse response = api.feeQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InvoiceClient#feeQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 开票商编 |
 **parentMerchantNo** | **String**| 上级商编 |
 **chargingDateStart** | **String**| 收费开始日期 |
 **chargingDateEnd** | **String**| 收费结束日期 |

### Return type
[**FeeQueryGetFeeResponseDtoResult**](../model/FeeQueryGetFeeResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="infoModify"></a>
# **infoModify**
InfoModifyResponse infoModify(InfoModifyRequest request)

添加/修改发票信息

商户通过此接口，可以添加或修改发票信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.invoice.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InvoiceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InvoiceClient api = InvoiceClientBuilder.builder().build();

//InfoModifyRequest中的参数说明参见Parameters章节
InfoModifyRequest request = new InfoModifyRequest();
request.setMerchantNo("10040040287");
request.setCustomerRequestNo("8d697f55a80141e291d9cac2d444fb22");
request.setParentMerchantNo("10040040286");
request.setMode("mode_example");
request.setInvoiceType("invoiceType_example");
request.setInvoiceForm("invoiceForm_example");
request.setLinkman("张三");
request.setLinkmanPhone("13300976554");
request.setPostalAddress("北京市通州区滨惠北一街3号院1号楼1层1-8-22");
request.setPostalCode("100020");
request.setTaxpayerId("91110000752646912Q");
request.setInvoicePhone("010-57073962");
request.setInvoiceAddress("北京市通州区滨惠北一街3号院1号楼1层1-8-22");
request.setBankName("招商银行北京建国门支行");
request.setAccountNo("110902081410707");
request.setEmail("san.zhang@yeepay.com");
request.setRemark("备注1");
request.setStandardType("GGXH-001");
request.setUnit("件");
request.setQuantity(1);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    InfoModifyResponse response = api.infoModify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InvoiceClient#infoModify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **customerRequestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **mode** | **String**|  | [optional]
 **invoiceType** | **String**|  | [optional]
 **invoiceForm** | **String**|  | [optional]
 **linkman** | **String**|  | [optional]
 **linkmanPhone** | **String**|  | [optional]
 **postalAddress** | **String**|  | [optional]
 **postalCode** | **String**|  | [optional]
 **taxpayerId** | **String**|  | [optional]
 **invoicePhone** | **String**|  | [optional]
 **invoiceAddress** | **String**|  | [optional]
 **bankName** | **String**|  | [optional]
 **accountNo** | **String**|  | [optional]
 **email** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **standardType** | **String**|  | [optional]
 **unit** | **String**|  | [optional]
 **quantity** | **Integer**|  | [optional]

### Return type
[**InfoModifyAddOrModifyInvoiceInfoResponseDtoResult**](../model/InfoModifyAddOrModifyInvoiceInfoResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="infoQuery"></a>
# **infoQuery**
InfoQueryResponse infoQuery(InfoQueryRequest request)

查询发票信息

商户通过接口可以查询发票信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.invoice.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InvoiceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InvoiceClient api = InvoiceClientBuilder.builder().build();

//InfoQueryRequest中的参数说明参见Parameters章节
InfoQueryRequest request = new InfoQueryRequest();
request.setParentMerchantNo("10040040286");
request.setMerchantNo("10040040287");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    InfoQueryResponse response = api.infoQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InvoiceClient#infoQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 上级商编 |
 **merchantNo** | **String**| 开票商编 |

### Return type
[**InfoQueryQueryInvoiceInfoYOPResponseDtoResult**](../model/InfoQueryQueryInvoiceInfoYOPResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="recordQuery"></a>
# **recordQuery**
RecordQueryResponse recordQuery(RecordQueryRequest request)

查询开票记录

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.invoice.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(InvoiceClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
InvoiceClient api = InvoiceClientBuilder.builder().build();

//RecordQueryRequest中的参数说明参见Parameters章节
RecordQueryRequest request = new RecordQueryRequest();
request.setParentMerchantNo("10080009456");
request.setCustomerRequestNo("337fbe4b345241fbb2854ed7c1bef5a2");
request.setMerchantNo("10080009462");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RecordQueryResponse response = api.recordQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling InvoiceClient#recordQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 上级商编 |
 **customerRequestNo** | **String**| 请求号，与开票商编二者至少填写一个 | [optional]
 **merchantNo** | **String**| 开票商编，与请求号二者至少填写一个 | [optional]

### Return type
[**RecordQueryQueryApplyInvoiceResponseDTOResult**](../model/RecordQueryQueryApplyInvoiceResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

