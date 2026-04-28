# MerClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authStateQueryV2**](MerClient.md#authStateQueryV2) | **GET** /rest/v2.0/mer/auth/state/query | 商户授权状态查询接口
[**merchantDisposeQuery**](MerClient.md#merchantDisposeQuery) | **GET** /rest/v1.0/mer/merchant/dispose/query | 沉默商户解冻申请进度查询
[**merchantDisposeUnfreeze**](MerClient.md#merchantDisposeUnfreeze) | **POST** /rest/v1.0/mer/merchant/dispose/unfreeze | 沉默商户解冻申请
[**merchantInfoModify**](MerClient.md#merchantInfoModify) | **POST** /rest/v1.0/mer/merchant/info/modify | 商户信息变更
[**merchantSupplementQualificationQuery**](MerClient.md#merchantSupplementQualificationQuery) | **GET** /rest/v1.0/mer/merchant/supplement/qualification/query | 后补资质查询
[**merchantSupplementQualificationSubmit**](MerClient.md#merchantSupplementQualificationSubmit) | **POST** /rest/v1.0/mer/merchant/supplement/qualification/submit | 后补资质提交
[**merchantWechatauthCancel**](MerClient.md#merchantWechatauthCancel) | **POST** /rest/v1.0/mer/merchant/wechatauth/cancel | 撤销微信实名认证申请单
[**merchantWechatauthQuery**](MerClient.md#merchantWechatauthQuery) | **GET** /rest/v1.0/mer/merchant/wechatauth/query | 查询微信实名认证状态
[**notifyRepeatV2**](MerClient.md#notifyRepeatV2) | **POST** /rest/v2.0/mer/notify/repeat | 重复获取(短验/邮件/电子签章)
[**productFeeModifyV2**](MerClient.md#productFeeModifyV2) | **POST** /rest/v2.0/mer/product/fee/modify | 商户产品变更
[**productFeeQueryV2**](MerClient.md#productFeeQueryV2) | **GET** /rest/v2.0/mer/product/fee/query | 商户产品费率查询
[**productIncrementSettleOpenV2**](MerClient.md#productIncrementSettleOpenV2) | **POST** /rest/v2.0/mer/product/increment-settle/open | 增值结算产品开通
[**productModifyQueryV2**](MerClient.md#productModifyQueryV2) | **GET** /rest/v2.0/mer/product/modify/query | 商户产品变更进度查询接口
[**registerQueryV2**](MerClient.md#registerQueryV2) | **GET** /rest/v2.0/mer/register/query | 商户入网进度查询接口
[**registerSaasIndexV2**](MerClient.md#registerSaasIndexV2) | **POST** /rest/v2.0/mer/register/saas/index | 特约商户H5页面入网（小微）
[**registerSaasMerchantV2**](MerClient.md#registerSaasMerchantV2) | **POST** /rest/v2.0/mer/register/saas/merchant | 特约商户入网(企业/个体)
[**registerSaasMicroV2**](MerClient.md#registerSaasMicroV2) | **POST** /rest/v2.0/mer/register/saas/micro | 特约商户入网(小微)
[**registerSaasWebIndexV2**](MerClient.md#registerSaasWebIndexV2) | **POST** /rest/v2.0/mer/register/saas/web/index | 特约商户WEB页面入网（企业/个体）


<a name="authStateQueryV2"></a>
# **authStateQueryV2**
AuthStateQueryV2Response authStateQueryV2(AuthStateQueryV2Request request)

商户授权状态查询接口

商户授权状态查询接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//AuthStateQueryV2Request中的参数说明参见Parameters章节
AuthStateQueryV2Request request = new AuthStateQueryV2Request();
request.setMerchantNo("merchantNo_example");
request.setReportMerchantNo("reportMerchantNo_example");
request.setFeeType("feeType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AuthStateQueryV2Response response = api.authStateQueryV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#authStateQueryV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 易宝商户编号 |
 **reportMerchantNo** | **String**| 报备商户编号 | [optional]
 **feeType** | **String**| 可选项如下：&lt;br&gt;GONGYI:微信公益&lt;br&gt;GONGJIAO:微信公缴&lt;br&gt;XIANXIA:微信线下&lt;br&gt;BAOXIAN:微信保险&lt;br&gt;XIANSHANG:微信线上&lt;br&gt;OLDLVZHOU:微信老绿洲&lt;br&gt;LVZHOU:微信绿洲&lt;br&gt;XIAOYUAN:微信校园&lt;br&gt;ALIPUTONG:支付宝普通 | [optional]

### Return type
[**AuthStateQueryV2IdentityAuthStateResDtoResult**](../model/AuthStateQueryV2IdentityAuthStateResDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantDisposeQuery"></a>
# **merchantDisposeQuery**
MerchantDisposeQueryResponse merchantDisposeQuery(MerchantDisposeQueryRequest request)

沉默商户解冻申请进度查询

查询沉默商户解冻申请单进度

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantDisposeQueryRequest中的参数说明参见Parameters章节
MerchantDisposeQueryRequest request = new MerchantDisposeQueryRequest();
request.setRequestNo("requestNo_example");
request.setApplicationNo("applicationNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantDisposeQueryResponse response = api.merchantDisposeQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantDisposeQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**| 请求号与工单号二选一必填 | [optional]
 **applicationNo** | **String**| 请求号与工单号二选一必填 | [optional]

### Return type
[**MerchantDisposeQueryMerchantQueryDisposeNotifyRespDtoResult**](../model/MerchantDisposeQueryMerchantQueryDisposeNotifyRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantDisposeUnfreeze"></a>
# **merchantDisposeUnfreeze**
MerchantDisposeUnfreezeResponse merchantDisposeUnfreeze(MerchantDisposeUnfreezeRequest request)

沉默商户解冻申请

支持自助发起沉默商户解冻

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantDisposeUnfreezeRequest中的参数说明参见Parameters章节
MerchantDisposeUnfreezeRequest request = new MerchantDisposeUnfreezeRequest();
request.setRequestNo("requestNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantDisposeUnfreezeResponse response = api.merchantDisposeUnfreeze(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantDisposeUnfreeze, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**MerchantDisposeUnfreezeMerchantDisposeRespDtoResult**](../model/MerchantDisposeUnfreezeMerchantDisposeRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantInfoModify"></a>
# **merchantInfoModify**
MerchantInfoModifyResponse merchantInfoModify(MerchantInfoModifyRequest request)

商户信息变更

商户信息变更

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantInfoModifyRequest中的参数说明参见Parameters章节
MerchantInfoModifyRequest request = new MerchantInfoModifyRequest();
request.setRequestNo("a04cf8bded8b4413a43ab455b21eedcd");
request.setMerchantNo("merchantNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setMerchantSubjectInfo("{ \"licenceUrl\":\"商户证件照片地址\", \"signName\":\"商户签约名\", \"licenceNo\":\"商户证件号码\", \"shortName\":\"商户简称\" }");
request.setMerchantCorporationInfo("{ \"legalName\":\"法人名称\", \"legalLicenceType\":\"ID_CARD\", \"legalLicenceNo\":\"法人证件编号\", \"legalLicenceFrontUrl\":\"法人证件人像面照片地址\", \"legalLicenceBackUrl\":\"法人证件非人像面照片地址\" }");
request.setMerchantContactInfo("{ \"contactName\":\"联系人姓名\", \"contactMobile\":\"联系人手机号\", \"contactEmail\":\"联系人邮箱\", \"contactLicenceNo\":\"联系人证件号码\" ,\"servicePhone\":\"客服电话\"}");
request.setIndustryCategoryInfo("{ \"primaryIndustryCategory\":\"一级行业分类编码\", \"secondaryIndustryCategory\":\"二级行业分类编码\" }");
request.setBusinessAddressInfo("{ \"province\":\"经营省\", \"city\":\"经营市\", \"district\":\"经营区\", \"address\":\"经营地址\" }");
request.setAccountInfo("{\"bankAccountName\":\"开户名称\",\"bankAccountType\":\"银行账户类型\",\"bankAccountNo\":\"银行账户号码\",\"bankCardTag\":\"[\\\"SETTLEMENT\\\",\\\"WITHDRAW\\\"]\",\"authorizationUrl\":\"https://staticres.yeepay.com/xxx.文件后缀\",\"bankCode\":\"开户总行编码\"}");
request.setBankToken("{ \"deviceIp\":\"交易ip\", \"token\":\"交易口令\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantInfoModifyResponse response = api.merchantInfoModify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantInfoModify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **merchantSubjectInfo** | **String**|  | [optional]
 **merchantCorporationInfo** | **String**|  | [optional]
 **merchantContactInfo** | **String**|  | [optional]
 **industryCategoryInfo** | **String**|  | [optional]
 **businessAddressInfo** | **String**|  | [optional]
 **accountInfo** | **String**|  | [optional]
 **bankToken** | **String**|  | [optional]

### Return type
[**MerchantInfoModifyMerchantInfoModifyRespDTOResult**](../model/MerchantInfoModifyMerchantInfoModifyRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantSupplementQualificationQuery"></a>
# **merchantSupplementQualificationQuery**
MerchantSupplementQualificationQueryResponse merchantSupplementQualificationQuery(MerchantSupplementQualificationQueryRequest request)

后补资质查询

后补资质查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantSupplementQualificationQueryRequest中的参数说明参见Parameters章节
MerchantSupplementQualificationQueryRequest request = new MerchantSupplementQualificationQueryRequest();
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantSupplementQualificationQueryResponse response = api.merchantSupplementQualificationQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantSupplementQualificationQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]

### Return type
[**MerchantSupplementQualificationQueryQueryMopQuaInfoRespDTOResult**](../model/MerchantSupplementQualificationQueryQueryMopQuaInfoRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantSupplementQualificationSubmit"></a>
# **merchantSupplementQualificationSubmit**
MerchantSupplementQualificationSubmitResponse merchantSupplementQualificationSubmit(MerchantSupplementQualificationSubmitRequest request)

后补资质提交

后补资质提交

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantSupplementQualificationSubmitRequest中的参数说明参见Parameters章节
MerchantSupplementQualificationSubmitRequest request = new MerchantSupplementQualificationSubmitRequest();
request.setMerchantNo("1234567890");
request.setQualifications("[   {     \"value\": \"https://staticres.yeepay.com/xxx.文件后缀\",     \"key\": \"LEGAL_LICENCE_FRONT_URL\"   },   {     \"value\": \"https://staticres.yeepay.com/xxx.文件后缀\",     \"key\": \"LEGAL_LICENCE_BACK_URL\"   } ]");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantSupplementQualificationSubmitResponse response = api.merchantSupplementQualificationSubmit(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantSupplementQualificationSubmit, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **qualifications** | **String**|  | [optional]

### Return type
[**MerchantSupplementQualificationSubmitSubmitMopQuaInfoRespDTOResult**](../model/MerchantSupplementQualificationSubmitSubmitMopQuaInfoRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantWechatauthCancel"></a>
# **merchantWechatauthCancel**
MerchantWechatauthCancelResponse merchantWechatauthCancel(MerchantWechatauthCancelRequest request)

撤销微信实名认证申请单

撤销微信实名认证申请单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantWechatauthCancelRequest中的参数说明参见Parameters章节
MerchantWechatauthCancelRequest request = new MerchantWechatauthCancelRequest();
request.setApplymentId("applymentId_example");
request.setRequestNo("requestNo_example");
request.setSubMerchantNo("subMerchantNo_example");
request.setReportFee("reportFee_example");
request.setChannelId("channelId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantWechatauthCancelResponse response = api.merchantWechatauthCancel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantWechatauthCancel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **applymentId** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **subMerchantNo** | **String**|  | [optional]
 **reportFee** | **String**|  | [optional]
 **channelId** | **String**|  | [optional]

### Return type
[**MerchantWechatauthCancelApplymentCancelRespDtoResult**](../model/MerchantWechatauthCancelApplymentCancelRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="merchantWechatauthQuery"></a>
# **merchantWechatauthQuery**
MerchantWechatauthQueryResponse merchantWechatauthQuery(MerchantWechatauthQueryRequest request)

查询微信实名认证状态

查询微信实名认证状态

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//MerchantWechatauthQueryRequest中的参数说明参见Parameters章节
MerchantWechatauthQueryRequest request = new MerchantWechatauthQueryRequest();
request.setApplymentId("applymentId_example");
request.setSubMerchantNo("subMerchantNo_example");
request.setReportFee("reportFee_example");
request.setRequestNo("requestNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantWechatauthQueryResponse response = api.merchantWechatauthQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#merchantWechatauthQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **applymentId** | **String**|  |
 **subMerchantNo** | **String**|  |
 **reportFee** | **String**| GONGYI 微信公益&lt;br&gt;GONGJIAO 微信公缴&lt;br&gt;XIANXIA 微信线下&lt;br&gt;BAOXIAN 微信保险&lt;br&gt;XIANSHANG 微信线上&lt;br&gt;OLDLVZHOU 微信老绿洲&lt;br&gt;LVZHOU 微信绿洲&lt;br&gt;XIAOYUAN 微信校园 |
 **requestNo** | **String**|  | [optional]

### Return type
[**MerchantWechatauthQueryQueryCertificateResultRespDtoResult**](../model/MerchantWechatauthQueryQueryCertificateResultRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="notifyRepeatV2"></a>
# **notifyRepeatV2**
NotifyRepeatV2Response notifyRepeatV2(NotifyRepeatV2Request request)

重复获取(短验/邮件/电子签章)

重复获取(短验/邮件/电子签章)

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//NotifyRepeatV2Request中的参数说明参见Parameters章节
NotifyRepeatV2Request request = new NotifyRepeatV2Request();
request.setRequestNo("requestNo_example");
request.setApplicationNo("applicationNo_example");
request.setType("type_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    NotifyRepeatV2Response response = api.notifyRepeatV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#notifyRepeatV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **applicationNo** | **String**|  | [optional]
 **type** | **String**|  | [optional]

### Return type
[**NotifyRepeatV2MerchantNetInRepeatNotifyRespDtoResult**](../model/NotifyRepeatV2MerchantNetInRepeatNotifyRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="productFeeModifyV2"></a>
# **productFeeModifyV2**
ProductFeeModifyV2Response productFeeModifyV2(ProductFeeModifyV2Request request)

商户产品变更

商户产品变更

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//ProductFeeModifyV2Request中的参数说明参见Parameters章节
ProductFeeModifyV2Request request = new ProductFeeModifyV2Request();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setProductInfo("[{\"productCode\":\"MERCHANT_SCAN_ALIPAY_OFFLINE\",\"rateType\":\"SINGLE_PERCENT\",\"percentRate\":\"0.1\",\"undertaker\":\"PLATFORM_MERCHANT\",\"paymentMethod\":\"REAL_TIME\"}]");
request.setProductQualificationInfo("{\"mcc\":\"7829\",\"paymentScene\":\"RLZYFW\",\"systemScreenshotUrl\":\"https://staticres.yeepay.com/xxx.文件后缀\",\"specialPermitProcessUrl\":\"https://staticres.yeepay.com/xxx.文件后缀\",\"agreementPhotoUrl\":\"https://staticres.yeepay.com/xxx.文件后缀\"}");
request.setSettlementAccountInfo("{ \"settlementDirection\":\"结算方向\", \"bankCode\":\"开户总行编码\", \"bankAccountType\":\"银行账户类型\", \"bankCardNo\":\"银行账户号码\" }");
request.setFunctionService("[\"SHARE\"]");
request.setFunctionServiceQualificationInfo("{\"shareScene\":\"FZ_FJ001\",\"shareCertificate\":\"https://staticres.yeepay.com/xxx.文件后缀\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ProductFeeModifyV2Response response = api.productFeeModifyV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#productFeeModifyV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **productInfo** | **String**|  | [optional]
 **productQualificationInfo** | **String**|  | [optional]
 **settlementAccountInfo** | **String**|  | [optional]
 **functionService** | **String**|  | [optional]
 **functionServiceQualificationInfo** | **String**|  | [optional]

### Return type
[**ProductFeeModifyV2ModifyProductFeeRespDtoResult**](../model/ProductFeeModifyV2ModifyProductFeeRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="productFeeQueryV2"></a>
# **productFeeQueryV2**
ProductFeeQueryV2Response productFeeQueryV2(ProductFeeQueryV2Request request)

商户产品费率查询

商户产品费率查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//ProductFeeQueryV2Request中的参数说明参见Parameters章节
ProductFeeQueryV2Request request = new ProductFeeQueryV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setProductCode("MERCHANT_SCAN_ALIPAY_OFFLINE");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ProductFeeQueryV2Response response = api.productFeeQueryV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#productFeeQueryV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 如果为平台商拓展商户（入驻商户），此为平台商商户编号；&lt;br&gt;如为saas服务商拓展商户（平台商/标准商户），此为saas服务商商户编号。 |
 **merchantNo** | **String**| 需要查询产品的商户编号 |
 **productCode** | **String**|  | [optional]

### Return type
[**ProductFeeQueryV2QueryProductFeeRespDtoResult**](../model/ProductFeeQueryV2QueryProductFeeRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="productIncrementSettleOpenV2"></a>
# **productIncrementSettleOpenV2**
ProductIncrementSettleOpenV2Response productIncrementSettleOpenV2(ProductIncrementSettleOpenV2Request request)

增值结算产品开通

增值结算产品开通

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//ProductIncrementSettleOpenV2Request中的参数说明参见Parameters章节
ProductIncrementSettleOpenV2Request request = new ProductIncrementSettleOpenV2Request();
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setProductInfo("[{\"productCode\":\"S0\",\"rateType\":\"FIXED_MIX_PERCENT\",\"percentRate\":\"0.1\",\"fixedRate\":\"111\"}]");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ProductIncrementSettleOpenV2Response response = api.productIncrementSettleOpenV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#productIncrementSettleOpenV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **productInfo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**ProductIncrementSettleOpenV2AddIncrementSettleProductRespDtoResult**](../model/ProductIncrementSettleOpenV2AddIncrementSettleProductRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="productModifyQueryV2"></a>
# **productModifyQueryV2**
ProductModifyQueryV2Response productModifyQueryV2(ProductModifyQueryV2Request request)

商户产品变更进度查询接口

商户产品变更进度查询接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//ProductModifyQueryV2Request中的参数说明参见Parameters章节
ProductModifyQueryV2Request request = new ProductModifyQueryV2Request();
request.setRequestNo("0adc579914d541f8baa3be75387846f1");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ProductModifyQueryV2Response response = api.productModifyQueryV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#productModifyQueryV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |

### Return type
[**ProductModifyQueryV2ProductModifyProgressQueryRespDtoResult**](../model/ProductModifyQueryV2ProductModifyProgressQueryRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="registerQueryV2"></a>
# **registerQueryV2**
RegisterQueryV2Response registerQueryV2(RegisterQueryV2Request request)

商户入网进度查询接口

商户入网进度查询接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//RegisterQueryV2Request中的参数说明参见Parameters章节
RegisterQueryV2Request request = new RegisterQueryV2Request();
request.setRequestNo("0adc579914d541f8baa3be75387846f1");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RegisterQueryV2Response response = api.registerQueryV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#registerQueryV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |

### Return type
[**RegisterQueryV2NetInProgressQueryRespDtoResult**](../model/RegisterQueryV2NetInProgressQueryRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="registerSaasIndexV2"></a>
# **registerSaasIndexV2**
RegisterSaasIndexV2Response registerSaasIndexV2(RegisterSaasIndexV2Request request)

特约商户H5页面入网（小微）

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//RegisterSaasIndexV2Request中的参数说明参见Parameters章节
RegisterSaasIndexV2Request request = new RegisterSaasIndexV2Request();
request.setRequestNo("示例值：REQ6437657876");
request.setParentMerchantNo("示例值：10080000001");
request.setNotifyUrl("示例值：http://www.shili111.com");
request.setReturnUrl("示例值：http://www.shili.com");
request.setMobile("159****8288");
request.setName("示例值：张三");
request.setIdCardNo("示例值：430422199001236704");
request.setWalletUserNo("示例值：User89849");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RegisterSaasIndexV2Response response = api.registerSaasIndexV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#registerSaasIndexV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **walletUserNo** | **String**|  | [optional]

### Return type
[**RegisterSaasIndexV2UserPreRegisterRespDtoResult**](../model/RegisterSaasIndexV2UserPreRegisterRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="registerSaasMerchantV2"></a>
# **registerSaasMerchantV2**
RegisterSaasMerchantV2Response registerSaasMerchantV2(RegisterSaasMerchantV2Request request)

特约商户入网(企业/个体)

特约商户入网(企业/个体)

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//RegisterSaasMerchantV2Request中的参数说明参见Parameters章节
RegisterSaasMerchantV2Request request = new RegisterSaasMerchantV2Request();
request.setRequestNo("YBRWQQH20210622XXXXXX");
request.setBusinessRole("ORDINARY_MERCHANT");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantSubjectInfo("{         \"licenceUrl\":\"商户证件照片地址\",         \"signName\":\"商户签约名\",         \"signType\":\"商户签约类型\",         \"licenceNo\":\"商户证件号码\",         \"shortName\":\"商户简称\"     }");
request.setMerchantCorporationInfo("{ \"legalName\":\"法人名称\", \"legalLicenceType\":\"法人证件类型\", \"legalLicenceNo\":\"法人证件编号\", \"legalLicenceFrontUrl\":\"法人证件正面照片地址\", \"legalLicenceBackUrl\":\"法人证件背面照片地址\" }");
request.setMerchantContactInfo("{ \"contactName\":\"联系人姓名\", \"contactMobile\":\"联系人手机号\", \"contactEmail\":\"联系人邮箱\", \"contactLicenceNo\":\"联系人证件号码\" }");
request.setIndustryCategoryInfo("{ \"primaryIndustryCategory\":\"一级行业分类编码\", \"secondaryIndustryCategory\":\"二级行业分类编码\" }");
request.setBusinessAddressInfo("{ \"province\":\"经营省\", \"city\":\"经营市\", \"district\":\"经营区\", \"address\":\"经营地址\" }");
request.setSettlementAccountInfo("{ \"settlementDirection\":\"结算方向\", \"bankCode\":\"开户总行编码\", \"bankAccountType\":\"银行账户类型\", \"bankCardNo\":\"银行账户号码\" }");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setProductInfo("[{\"productCode\":\"MERCHANT_SCAN_ALIPAY_OFFLINE\",\"rateType\":\"SINGLE_PERCENT\",\"percentRate\":\"0.1\"},{\"productCode\":\"MERCHANT_SCAN_UNIONPAY_CREDIT\",\"rateType\":\"SINGLE_FIXED\",\"fixedRate\":\"1\"},{\"productCode\":\"T1\",\"rateType\":\"SINGLE_PERCENT\",\"percentRate\":\"0.1\"}]");
request.setProductQualificationInfo("{ \"paymentScene\": \"RLZYFW\",   \"systemScreenshotUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\",   \"specialPermitProcessUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\",   \"agreementPhotoUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\" }");
request.setFunctionService("[\"SHARE\"]");
request.setFunctionServiceQualificationInfo("{\"shareScene\":\"FZ_FJ001\",\"shareCertificate\":\"https://staticres.yeepay.com/xxx.文件后缀\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RegisterSaasMerchantV2Response response = api.registerSaasMerchantV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#registerSaasMerchantV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **businessRole** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantSubjectInfo** | **String**|  | [optional]
 **merchantCorporationInfo** | **String**|  | [optional]
 **merchantContactInfo** | **String**|  | [optional]
 **industryCategoryInfo** | **String**|  | [optional]
 **businessAddressInfo** | **String**|  | [optional]
 **settlementAccountInfo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **productInfo** | **String**|  | [optional]
 **productQualificationInfo** | **String**|  | [optional]
 **functionService** | **String**|  | [optional]
 **functionServiceQualificationInfo** | **String**|  | [optional]

### Return type
[**RegisterSaasMerchantV2ContributeMerchantNetInRespDtoResult**](../model/RegisterSaasMerchantV2ContributeMerchantNetInRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="registerSaasMicroV2"></a>
# **registerSaasMicroV2**
RegisterSaasMicroV2Response registerSaasMicroV2(RegisterSaasMicroV2Request request)

特约商户入网(小微)

SaaS服务商下特约商户入网(小微)

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//RegisterSaasMicroV2Request中的参数说明参见Parameters章节
RegisterSaasMicroV2Request request = new RegisterSaasMicroV2Request();
request.setRequestNo("YBRWQQH20210622XXXXXX");
request.setBusinessRole("SETTLED_MERCHANT");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantSubjectInfo("{ \"signName\":\"商户签约名\", \"shortName\":\"商户简称\" }");
request.setBusinessAddressInfo("{ \"province\":\"经营省\", \"city\":\"经营市\", \"district\":\"经营区\", \"address\":\"经营地址\" }");
request.setMerchantCorporationInfo("{ \"legalLicenceType\":\"法人证件类型\", \"legalLicenceNo\":\"法人证件编号\", \"legalLicenceFrontUrl\":\"法人证件正面照片地址\", \"legalLicenceBackUrl\":\"法人证件背面照片地址\",  \"mobile\":\"法人手机号\"  }");
request.setAccountInfo("{\"bankAccountType\":\"银行账户类型\",\"bankCardNo\":\"银行账户号码\",\"bankCode\":\"开户总行编码\"}");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setProductInfo("[{\"productCode\":\"MERCHANT_SCAN_ALIPAY_OFFLINE\",\"rateType\":\"SINGLE_PERCENT\",\"percentRate\":\"0.1\"},{\"productCode\":\"MERCHANT_SCAN_UNIONPAY_CREDIT\",\"rateType\":\"SINGLE_FIXED\",\"fixedRate\":\"1\"},{\"productCode\":\"T1\",\"rateType\":\"SINGLE_PERCENT\",\"percentRate\":\"0.1\"}]");
request.setProductQualificationInfo("{\"paymentScene\": \"RLZYFW\",   \"systemScreenshotUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\",   \"specialPermitProcessUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\",   \"agreementPhotoUrl\": \"https://staticres.yeepay.com/xxx.文件后缀\" }");
request.setFunctionService("[\"SHARE\"]");
request.setFunctionServiceQualificationInfo("{\"shareScene\":\"FZ_FJ001\",\"shareCertificate\":\"https://staticres.yeepay.com/xxx.文件后缀\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RegisterSaasMicroV2Response response = api.registerSaasMicroV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#registerSaasMicroV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **businessRole** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantSubjectInfo** | **String**|  | [optional]
 **businessAddressInfo** | **String**|  | [optional]
 **merchantCorporationInfo** | **String**|  | [optional]
 **accountInfo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **productInfo** | **String**|  | [optional]
 **productQualificationInfo** | **String**|  | [optional]
 **functionService** | **String**|  | [optional]
 **functionServiceQualificationInfo** | **String**|  | [optional]

### Return type
[**RegisterSaasMicroV2ContributeMicroMerchantNetInRespDtoResult**](../model/RegisterSaasMicroV2ContributeMicroMerchantNetInRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="registerSaasWebIndexV2"></a>
# **registerSaasWebIndexV2**
RegisterSaasWebIndexV2Response registerSaasWebIndexV2(RegisterSaasWebIndexV2Request request)

特约商户WEB页面入网（企业/个体）

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.mer.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MerClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MerClient api = MerClientBuilder.builder().build();

//RegisterSaasWebIndexV2Request中的参数说明参见Parameters章节
RegisterSaasWebIndexV2Request request = new RegisterSaasWebIndexV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setRequestNo("fba1dd39fd3846b4901f5a833fa3baa3");
request.setSignType("ENTERPRISE");
request.setNotifyUrl("http://www.yeepay.com/merchant/notify");
request.setReturnUrl("http://www.yeepay.com");
request.setProductTemplateNo("CP166748***3516");
request.setMerchantBaseInfo("{ \"signName\":\"商户签约名\", \"licenceNo\":\"商户证件号码\"}");
request.setCorporationInfo("{ \"legalName\":\"法人名称\",  \"legalLicenceNo\":\"法人证件编号\"}");
request.setContactInfo("{ \"contactName\":\"联系人姓名\", \"contactMobile\":\"联系人手机号\", \"contactEmail\":\"联系人邮箱\", \"contactLicenceNo\":\"联系人证件号码\" ,\"servicePhone\":\"客服电话\"}");
request.setBusinessAddressInfo("{ \"address\":\"商户实际经营地址\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RegisterSaasWebIndexV2Response response = api.registerSaasWebIndexV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MerClient#registerSaasWebIndexV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **signType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **productTemplateNo** | **String**|  | [optional]
 **merchantBaseInfo** | **String**|  | [optional]
 **corporationInfo** | **String**|  | [optional]
 **contactInfo** | **String**|  | [optional]
 **businessAddressInfo** | **String**|  | [optional]

### Return type
[**RegisterSaasWebIndexV2CreateNetInUrlRespDTOResult**](../model/RegisterSaasWebIndexV2CreateNetInUrlRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

