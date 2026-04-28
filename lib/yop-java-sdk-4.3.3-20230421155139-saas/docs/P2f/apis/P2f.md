# P2fClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**companyFinanceAccount**](P2fClient.md#companyFinanceAccount) | **POST** /rest/v1.0/p2f/company-finance/account | 对公开户
[**companyFinanceAccountQuery**](P2fClient.md#companyFinanceAccountQuery) | **GET** /rest/v1.0/p2f/company-finance/account/query | 对公开户查询
[**companyFinanceAssetsQuery**](P2fClient.md#companyFinanceAssetsQuery) | **GET** /rest/v1.0/p2f/company-finance/assets/query | 对公资产查询
[**companyFinanceOrderQuery**](P2fClient.md#companyFinanceOrderQuery) | **GET** /rest/v1.0/p2f/company-finance/order/query | 对公申购赎回订单状态查询
[**companyFinancePurchaseOrder**](P2fClient.md#companyFinancePurchaseOrder) | **POST** /rest/v1.0/p2f/company-finance/purchase-order | 对公申购
[**companyFinanceRedeemOrder**](P2fClient.md#companyFinanceRedeemOrder) | **POST** /rest/v1.0/p2f/company-finance/redeem-order | 对公赎回
[**companyFinanceSmallPayment**](P2fClient.md#companyFinanceSmallPayment) | **POST** /rest/v1.0/p2f/company-finance/small-payment | 小额打款鉴权
[**companyFinanceTransactionQuery**](P2fClient.md#companyFinanceTransactionQuery) | **GET** /rest/v1.0/p2f/company-finance/transaction/query | 对公交易明细查询
[**fileUpload**](P2fClient.md#fileUpload) | **POST** /yos/v1.0/p2f/file-upload | 文件上传
[**zzdfOrder**](P2fClient.md#zzdfOrder) | **POST** /rest/v1.0/p2f/zzdf/order | 增值代付订单
[**zzdfQuery**](P2fClient.md#zzdfQuery) | **GET** /rest/v1.0/p2f/zzdf/query | 增值代付订单查询


<a name="companyFinanceAccount"></a>
# **companyFinanceAccount**
CompanyFinanceAccountResponse companyFinanceAccount(CompanyFinanceAccountRequest request)

对公开户

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceAccountRequest中的参数说明参见Parameters章节
CompanyFinanceAccountRequest request = new CompanyFinanceAccountRequest();
request.setCompName("compName_example");
request.setCompNo("compNo_example");
request.setCustomerCertExpiry("customerCertExpiry_example");
request.setRegSerialNoExpired("regSerialNoExpired_example");
request.setCompTelephone("compTelephone_example");
request.setOrgSMSMobile("orgSMSMobile_example");
request.setUniteCreditCode("uniteCreditCode_example");
request.setCompEmail("compEmail_example");
request.setCompAddr("compAddr_example");
request.setZipCode("zipCode_example");
request.setBizScope("bizScope_example");
request.setLegalName("legalName_example");
request.setLegalIdNo("legalIdNo_example");
request.setLegalStartDate("legalStartDate_example");
request.setLegalExpiredDate("legalExpiredDate_example");
request.setLegalMobile("legalMobile_example");
request.setBankCode("bankCode_example");
request.setBankName("bankName_example");
request.setBankCardNo("bankCardNo_example");
request.setBindType("bindType_example");
request.setBindAcctBranch("bindAcctBranch_example");
request.setThreeInOneFlag("threeInOneFlag_example");
request.setUniteCreditCodePath("uniteCreditCodePath_example");
request.setFrontPhotoPath("frontPhotoPath_example");
request.setBackPhotoPath("backPhotoPath_example");
request.setOpenAcctPermitCodePath("openAcctPermitCodePath_example");
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceAccountResponse response = api.companyFinanceAccount(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceAccount, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **compName** | **String**|  | [optional]
 **compNo** | **String**|  | [optional]
 **customerCertExpiry** | **String**|  | [optional]
 **regSerialNoExpired** | **String**|  | [optional]
 **compTelephone** | **String**|  | [optional]
 **orgSMSMobile** | **String**|  | [optional]
 **uniteCreditCode** | **String**|  | [optional]
 **compEmail** | **String**|  | [optional]
 **compAddr** | **String**|  | [optional]
 **zipCode** | **String**|  | [optional]
 **bizScope** | **String**|  | [optional]
 **legalName** | **String**|  | [optional]
 **legalIdNo** | **String**|  | [optional]
 **legalStartDate** | **String**|  | [optional]
 **legalExpiredDate** | **String**|  | [optional]
 **legalMobile** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **bankName** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **bindType** | **String**|  | [optional]
 **bindAcctBranch** | **String**|  | [optional]
 **threeInOneFlag** | **String**|  | [optional]
 **uniteCreditCodePath** | **String**|  | [optional]
 **frontPhotoPath** | **String**|  | [optional]
 **backPhotoPath** | **String**|  | [optional]
 **openAcctPermitCodePath** | **String**|  | [optional]
 **channelCode** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**CompanyFinanceAccountCompCustOpenAcctRspDTOResult**](../model/CompanyFinanceAccountCompCustOpenAcctRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceAccountQuery"></a>
# **companyFinanceAccountQuery**
CompanyFinanceAccountQueryResponse companyFinanceAccountQuery(CompanyFinanceAccountQueryRequest request)

对公开户查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceAccountQueryRequest中的参数说明参见Parameters章节
CompanyFinanceAccountQueryRequest request = new CompanyFinanceAccountQueryRequest();
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceAccountQueryResponse response = api.companyFinanceAccountQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceAccountQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelCode** | **String**|  |
 **requestNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**CompanyFinanceAccountQueryCompCustOpenAcctRspDTOResult**](../model/CompanyFinanceAccountQueryCompCustOpenAcctRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceAssetsQuery"></a>
# **companyFinanceAssetsQuery**
CompanyFinanceAssetsQueryResponse companyFinanceAssetsQuery(CompanyFinanceAssetsQueryRequest request)

对公资产查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceAssetsQueryRequest中的参数说明参见Parameters章节
CompanyFinanceAssetsQueryRequest request = new CompanyFinanceAssetsQueryRequest();
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceAssetsQueryResponse response = api.companyFinanceAssetsQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceAssetsQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channelCode** | **String**|  |
 **requestNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**CompanyFinanceAssetsQueryCompQueryAssetsResponseDTOResult**](../model/CompanyFinanceAssetsQueryCompQueryAssetsResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceOrderQuery"></a>
# **companyFinanceOrderQuery**
CompanyFinanceOrderQueryResponse companyFinanceOrderQuery(CompanyFinanceOrderQueryRequest request)

对公申购赎回订单状态查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceOrderQueryRequest中的参数说明参见Parameters章节
CompanyFinanceOrderQueryRequest request = new CompanyFinanceOrderQueryRequest();
request.setBizType("bizType_example");
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceOrderQueryResponse response = api.companyFinanceOrderQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceOrderQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bizType** | **String**| 可选项如下:&lt;br&gt;PURCHASE:申购&lt;br&gt;REDEEM:赎回 |
 **channelCode** | **String**|  |
 **requestNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**CompanyFinanceOrderQueryCompQueryOrderStatusResponseDTOResult**](../model/CompanyFinanceOrderQueryCompQueryOrderStatusResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinancePurchaseOrder"></a>
# **companyFinancePurchaseOrder**
CompanyFinancePurchaseOrderResponse companyFinancePurchaseOrder(CompanyFinancePurchaseOrderRequest request)

对公申购

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinancePurchaseOrderRequest中的参数说明参见Parameters章节
CompanyFinancePurchaseOrderRequest request = new CompanyFinancePurchaseOrderRequest();
request.setProdCode("prodCode_example");
request.setAmount(new BigDecimal("0"));
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setP2fOpenAcctNo("p2fOpenAcctNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinancePurchaseOrderResponse response = api.companyFinancePurchaseOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinancePurchaseOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prodCode** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **channelCode** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **p2fOpenAcctNo** | **String**|  | [optional]

### Return type
[**CompanyFinancePurchaseOrderCompTranPurchaseRspDTOResult**](../model/CompanyFinancePurchaseOrderCompTranPurchaseRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceRedeemOrder"></a>
# **companyFinanceRedeemOrder**
CompanyFinanceRedeemOrderResponse companyFinanceRedeemOrder(CompanyFinanceRedeemOrderRequest request)

对公赎回

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceRedeemOrderRequest中的参数说明参见Parameters章节
CompanyFinanceRedeemOrderRequest request = new CompanyFinanceRedeemOrderRequest();
request.setP2fOpenAcctNo("p2fOpenAcctNo_example");
request.setProdCode("prodCode_example");
request.setAmount(new BigDecimal("0"));
request.setRemark("remark_example");
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setP2fOrderId("p2fOrderId_example");
request.setRequestTime("2023-05-07 10:49:07");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceRedeemOrderResponse response = api.companyFinanceRedeemOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceRedeemOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **p2fOpenAcctNo** | **String**|  | [optional]
 **prodCode** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **remark** | **String**|  | [optional]
 **channelCode** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **p2fOrderId** | **String**|  | [optional]
 **requestTime** | **String**|  | [optional]

### Return type
[**CompanyFinanceRedeemOrderCompTranRedeemRspDTOResult**](../model/CompanyFinanceRedeemOrderCompTranRedeemRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceSmallPayment"></a>
# **companyFinanceSmallPayment**
CompanyFinanceSmallPaymentResponse companyFinanceSmallPayment(CompanyFinanceSmallPaymentRequest request)

小额打款鉴权

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceSmallPaymentRequest中的参数说明参见Parameters章节
CompanyFinanceSmallPaymentRequest request = new CompanyFinanceSmallPaymentRequest();
request.setConfirmCheckCode("confirmCheckCode_example");
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceSmallPaymentResponse response = api.companyFinanceSmallPayment(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceSmallPayment, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmCheckCode** | **String**|  | [optional]
 **channelCode** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**CompanyFinanceSmallPaymentCompCustOpenAcctConfirmRspDTOResult**](../model/CompanyFinanceSmallPaymentCompCustOpenAcctConfirmRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="companyFinanceTransactionQuery"></a>
# **companyFinanceTransactionQuery**
CompanyFinanceTransactionQueryResponse companyFinanceTransactionQuery(CompanyFinanceTransactionQueryRequest request)

对公交易明细查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//CompanyFinanceTransactionQueryRequest中的参数说明参见Parameters章节
CompanyFinanceTransactionQueryRequest request = new CompanyFinanceTransactionQueryRequest();
request.setStartDate("startDate_example");
request.setEndDate("endDate_example");
request.setChannelCode("channelCode_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CompanyFinanceTransactionQueryResponse response = api.companyFinanceTransactionQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#companyFinanceTransactionQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| 起始日期，格式yyyyMMdd |
 **endDate** | **String**| 结束日期，格式yyyyMMdd |
 **channelCode** | **String**|  |
 **requestNo** | **String**|  |
 **merchantNo** | **String**|  |

### Return type
[**CompanyFinanceTransactionQueryCompQueryTransactionListResponseDTOResult**](../model/CompanyFinanceTransactionQueryCompQueryTransactionListResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="fileUpload"></a>
# **fileUpload**
FileUploadResponse fileUpload(FileUploadRequest request)

文件上传

文件上传

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//FileUploadRequest中的参数说明参见Parameters章节
FileUploadRequest request = new FileUploadRequest();
request.setRequestNo("requestNo_example");
request.setIdentityType("identityType_example");
request.setIdentityId("identityId_example");
request.setIdType("ID");
request.setIdNO("idNO_example");
request.setFileType("fileType_example");
request.setImage(new File("/path/to/file"));

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    FileUploadResponse response = api.fileUpload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#fileUpload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **identityType** | **String**|  | [optional]
 **identityId** | **String**|  | [optional]
 **idType** | **String**|  | [optional]
 **idNO** | **String**|  | [optional]
 **fileType** | **String**|  | [optional]
 **image** | **File**|  | [optional]

### Return type
[**FileUploadCustFileUploadResponseDTOResult**](../model/FileUploadCustFileUploadResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="zzdfOrder"></a>
# **zzdfOrder**
ZzdfOrderResponse zzdfOrder(ZzdfOrderRequest request)

增值代付订单

充值代付接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//ZzdfOrderRequest中的参数说明参见Parameters章节
ZzdfOrderRequest request = new ZzdfOrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestNo("requestNo_example");
request.setOrderAmount(new BigDecimal("0"));
request.setReceiverAccountNo("receiverAccountNo_example");
request.setReceiverAccountName("receiverAccountName_example");
request.setReceiverBankCode("receiverBankCode_example");
request.setProvince("province_example");
request.setCity("city_example");
request.setBranchBankCode("branchBankCode_example");
request.setBankAccountType("bankAccountType_example");
request.setComments("comments_example");
request.setFeeChargeSide("feeChargeSide_example");
request.setTerminalType("terminalType_example");
request.setReceiveType("receiveType_example");
request.setNotifyUrl("notifyUrl_example");
request.setRemark("remark_example");
request.setRechargeAcctType("rechargeAcctType_example");
request.setRechargeRemark("rechargeRemark_example");
request.setRechargeFeeType("rechargeFeeType_example");
request.setRechargeBankCode("rechargeBankCode_example");
request.setRechargeBankCardNo("rechargeBankCardNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ZzdfOrderResponse response = api.zzdfOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#zzdfOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **receiverAccountNo** | **String**|  | [optional]
 **receiverAccountName** | **String**|  | [optional]
 **receiverBankCode** | **String**|  | [optional]
 **province** | **String**|  | [optional]
 **city** | **String**|  | [optional]
 **branchBankCode** | **String**|  | [optional]
 **bankAccountType** | **String**|  | [optional]
 **comments** | **String**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **terminalType** | **String**|  | [optional]
 **receiveType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **rechargeAcctType** | **String**|  | [optional]
 **rechargeRemark** | **String**|  | [optional]
 **rechargeFeeType** | **String**|  | [optional]
 **rechargeBankCode** | **String**|  | [optional]
 **rechargeBankCardNo** | **String**|  | [optional]

### Return type
[**ZzdfOrderRechargeAndPayRspDTOResult**](../model/ZzdfOrderRechargeAndPayRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="zzdfQuery"></a>
# **zzdfQuery**
ZzdfQueryResponse zzdfQuery(ZzdfQueryRequest request)

增值代付订单查询

增值代付订单查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.p2f.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(P2fClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
P2fClient api = P2fClientBuilder.builder().build();

//ZzdfQueryRequest中的参数说明参见Parameters章节
ZzdfQueryRequest request = new ZzdfQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestNo("requestNo_example");
request.setOrderNo("orderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ZzdfQueryResponse response = api.zzdfQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling P2fClient#zzdfQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **requestNo** | **String**|  | [optional]
 **orderNo** | **String**|  | [optional]

### Return type
[**ZzdfQueryQueryRechargeAndPayRspDTOResult**](../model/ZzdfQueryQueryRechargeAndPayRspDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

