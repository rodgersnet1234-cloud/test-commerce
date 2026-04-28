# SettleClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**balanceQuery**](SettleClient.md#balanceQuery) | **GET** /rest/v1.0/settle/balance/query | 待结算金额查询
[**fileGet**](SettleClient.md#fileGet) | **GET** /yos/v1.0/settle/file/get | 结算对账文件获取接口
[**recordsQuery**](SettleClient.md#recordsQuery) | **GET** /rest/v1.0/settle/records/query | 结算记录查询
[**selfSettleApply**](SettleClient.md#selfSettleApply) | **POST** /rest/v1.0/settle/self-settle/apply | 自助结算申请
[**settleCardAdd**](SettleClient.md#settleCardAdd) | **POST** /rest/v1.0/settle/settle-card/add | 新增结算卡
[**settleCardModify**](SettleClient.md#settleCardModify) | **POST** /rest/v1.0/settle/settle-card/modify | 修改结算卡
[**settleWayModifyRatio**](SettleClient.md#settleWayModifyRatio) | **POST** /rest/v1.0/settle/settle-way/modify-ratio | 修改结算方向比例
[**settleWayQuery**](SettleClient.md#settleWayQuery) | **GET** /rest/v1.0/settle/settle-way/query | 查询结算账户


<a name="balanceQuery"></a>
# **balanceQuery**
BalanceQueryResponse balanceQuery(BalanceQueryRequest request)

待结算金额查询

查询商户自助结算下未结算的交易统计信息。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//BalanceQueryRequest中的参数说明参见Parameters章节
BalanceQueryRequest request = new BalanceQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOperatePeriod("operatePeriod_example");
request.setEndTime("2023-05-07 10:49:05");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BalanceQueryResponse response = api.balanceQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#balanceQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号。&lt;br&gt;*标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**|  |
 **operatePeriod** | **String**| 查询时间范围。&lt;br&gt;PERIOD:指定时间范围，按照传入的统计截止时间查询未结算可结算金额&lt;br&gt;ALL:查询当前全部 |
 **endTime** | **String**| 统计截止时间。当查询范围按PERIOD时，需要必填此参数。 | [optional]

### Return type
[**BalanceQuerySelfSettleQueryResponseDtoResult**](../model/BalanceQuerySelfSettleQueryResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="fileGet"></a>
# **fileGet**
YosDownloadResponse fileGet(FileGetRequest request)

结算对账文件获取接口

支持商户进行对账文件下载。 受理失败，返回响应错误码；受理成功，返回文件

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//FileGetRequest中的参数说明参见Parameters章节
FileGetRequest request = new FileGetRequest();
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setSettleRequestNo("settleRequestNo_example");
request.setSettleDate("settleDate_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.fileGet(request);
    // 及时关闭文件流，避免连接泄漏
    YosDownloadInputStream result = null;
    try {
        result = response.getResult();
        saveFile(result);
    } catch (IOException e) {
        LOGGER.error("error when download, ex:", e);
    }  finally {
        if (null != result) {
            try {
                result.close();
            } catch (IOException e) {
                LOGGER.error("error when close YosDownloadInputStream, ex:", e);
            }
        }
    }
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#fileGet, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **parentMerchantNo** | **String**|  |
 **settleRequestNo** | **String**| 商户发起自助结算时的请求号，当结算日期为空时，此参数必填 | [optional]
 **settleDate** | **String**| 需要获取的结算文件对应的结算日期，当结算订单号为空时，此参数必填 | [optional]

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

<a name="recordsQuery"></a>
# **recordsQuery**
RecordsQueryResponse recordsQuery(RecordsQueryRequest request)

结算记录查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//RecordsQueryRequest中的参数说明参见Parameters章节
RecordsQueryRequest request = new RecordsQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setSettleRequestNo("settleRequestNo_example");
request.setSettleRequestBeginTime("2023-05-07 10:49:05");
request.setSettleRequestEndTime("2023-05-07 10:49:05");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RecordsQueryResponse response = api.recordsQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#recordsQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **settleRequestNo** | **String**| 结算请求号(结算请求号与结算申请起止时间二选一必填) | [optional]
 **settleRequestBeginTime** | **String**| 结算申请起始时间（结算申请起止时间与结算请求号二选一必填） | [optional]
 **settleRequestEndTime** | **String**| 结算申请截止时间（结算申请起止时间与结算请求号二选一必填） | [optional]

### Return type
[**RecordsQuerySettleRecordQueryResponseDtoResult**](../model/RecordsQuerySettleRecordQueryResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="selfSettleApply"></a>
# **selfSettleApply**
SelfSettleApplyResponse selfSettleApply(SelfSettleApplyRequest request)

自助结算申请

支持商户发起自助结算申请。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//SelfSettleApplyRequest中的参数说明参见Parameters章节
SelfSettleApplyRequest request = new SelfSettleApplyRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setSettleRequestNo("settleRequestNo_example");
request.setOperatePeriod("operatePeriod_example");
request.setEndTime("2023-05-07 10:49:05");
request.setNotifyUrl("notifyUrl_example");
request.setBankRemark("bankRemark_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SelfSettleApplyResponse response = api.selfSettleApply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#selfSettleApply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **settleRequestNo** | **String**|  | [optional]
 **operatePeriod** | **String**|  | [optional]
 **endTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **bankRemark** | **String**|  | [optional]

### Return type
[**SelfSettleApplySelfSettleResponseDtoResult**](../model/SelfSettleApplySelfSettleResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="settleCardAdd"></a>
# **settleCardAdd**
SettleCardAddResponse settleCardAdd(SettleCardAddRequest request)

新增结算卡

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//SettleCardAddRequest中的参数说明参见Parameters章节
SettleCardAddRequest request = new SettleCardAddRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10040062484");
request.setBankCardNo("bankCardNo_example");
request.setBankCardType("bankCardType_example");
request.setBankCode("bankCode_example");
request.setDefaultSettleCard(true);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SettleCardAddResponse response = api.settleCardAdd(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#settleCardAdd, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **bankCardType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **defaultSettleCard** | **Boolean**|  | [optional]

### Return type
[**SettleCardAddMerchantSettleCardResponseDTOResult**](../model/SettleCardAddMerchantSettleCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="settleCardModify"></a>
# **settleCardModify**
SettleCardModifyResponse settleCardModify(SettleCardModifyRequest request)

修改结算卡

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//SettleCardModifyRequest中的参数说明参见Parameters章节
SettleCardModifyRequest request = new SettleCardModifyRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10040062484");
request.setBankCardNo("bankCardNo_example");
request.setBankCardType("bankCardType_example");
request.setBankCode("bankCode_example");
request.setBrancgCode("brancgCode_example");
request.setDefaultSettleCard(true);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SettleCardModifyResponse response = api.settleCardModify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#settleCardModify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **bankCardType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **brancgCode** | **String**|  | [optional]
 **defaultSettleCard** | **Boolean**|  | [optional]

### Return type
[**SettleCardModifyMerchantSettleCardResponseDTOResult**](../model/SettleCardModifyMerchantSettleCardResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="settleWayModifyRatio"></a>
# **settleWayModifyRatio**
SettleWayModifyRatioResponse settleWayModifyRatio(SettleWayModifyRatioRequest request)

修改结算方向比例

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//SettleWayModifyRatioRequest中的参数说明参见Parameters章节
SettleWayModifyRatioRequest request = new SettleWayModifyRatioRequest();
request.setBody(new SettleWayModifyRatioModifySettleWayRatioRequestDtoParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SettleWayModifyRatioResponse response = api.settleWayModifyRatio(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#settleWayModifyRatio, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SettleWayModifyRatioModifySettleWayRatioRequestDtoParam**](../model/SettleWayModifyRatioModifySettleWayRatioRequestDtoParam.md)|  |

### Return type
[**SettleWayModifyRatioModifySettleWayRatioResponseDtoResult**](../model/SettleWayModifyRatioModifySettleWayRatioResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="settleWayQuery"></a>
# **settleWayQuery**
SettleWayQueryResponse settleWayQuery(SettleWayQueryRequest request)

查询结算账户

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.settle.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SettleClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SettleClient api = SettleClientBuilder.builder().build();

//SettleWayQueryRequest中的参数说明参见Parameters章节
SettleWayQueryRequest request = new SettleWayQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10040062484");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SettleWayQueryResponse response = api.settleWayQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SettleClient#settleWayQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号。&lt;br&gt;*标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**| 收款商户编号 |

### Return type
[**SettleWayQuerySettleWayQueryYOPResponseDtoResult**](../model/SettleWayQuerySettleWayQueryYOPResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

