# StdClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**billDividedaydownload**](StdClient.md#billDividedaydownload) | **GET** /yos/v1.0/std/bill/dividedaydownload | 分账日对账下载
[**billFundbillApply**](StdClient.md#billFundbillApply) | **POST** /rest/v1.0/std/bill/fundbill/apply | 资金账单申请
[**billFundbillDownload**](StdClient.md#billFundbillDownload) | **GET** /yos/v1.0/std/bill/fundbill/download | 资金账单下载
[**billFundbillEndbalanceApply**](StdClient.md#billFundbillEndbalanceApply) | **POST** /rest/v1.0/std/bill/fundbill-endbalance/apply | 日终余额账单申请
[**billFundbillFlowQuery**](StdClient.md#billFundbillFlowQuery) | **GET** /rest/v1.0/std/bill/fundbill/flow/query | 资金流水明细查询
[**billFundbillFlowSum**](StdClient.md#billFundbillFlowSum) | **GET** /rest/v1.0/std/bill/fundbill/flow/sum | 资金流水汇总查询
[**billSettlebillDownload**](StdClient.md#billSettlebillDownload) | **GET** /yos/v1.0/std/bill/settlebill/download | 下载结算账单
[**billTradedaydownload**](StdClient.md#billTradedaydownload) | **POST** /yos/v1.0/std/bill/tradedaydownload | 交易日对账下载
[**certOrder**](StdClient.md#certOrder) | **POST** /rest/v1.0/std/cert/order | 新信息认证系统-认证请求


<a name="billDividedaydownload"></a>
# **billDividedaydownload**
YosDownloadResponse billDividedaydownload(BillDividedaydownloadRequest request)

分账日对账下载

强调：获取对账文件时请以行号来获取对账文件信息，后期易宝可能在后追加参表头参数分账日对账下载，9点后下载前一天的对账文件，具体请参考对账文件说明&amp;lt;/a&amp;gt;&amp;lt;/p&amp;gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillDividedaydownloadRequest中的参数说明参见Parameters章节
BillDividedaydownloadRequest request = new BillDividedaydownloadRequest();
request.setMerchantNo("merchantNo_example");
request.setDayString("dayString_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.billDividedaydownload(request);
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
    LOGGER.error("Exception when calling StdClient#billDividedaydownload, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 标准商户:标准商户编号&lt;br&gt;平台商:平台商商户编号, 文件包含平台商及平台商下所有入驻商户的交易信息 | [optional]
 **dayString** | **String**| e.g.: 2017-09-09 | [optional]

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

<a name="billFundbillApply"></a>
# **billFundbillApply**
BillFundbillApplyResponse billFundbillApply(BillFundbillApplyRequest request)

资金账单申请

资金账单申请

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillFundbillApplyRequest中的参数说明参见Parameters章节
BillFundbillApplyRequest request = new BillFundbillApplyRequest();
request.setStartDate("startDate_example");
request.setEndDate("endDate_example");
request.setMerchantNo("merchantNo_example");
request.setSubMerchantNo("subMerchantNo_example");
request.setAccountType("accountType_example");
request.setNotifyUrl("notifyUrl_example");
request.setBillFormat("billFormat_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillFundbillApplyResponse response = api.billFundbillApply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling StdClient#billFundbillApply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**|  | [optional]
 **endDate** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **subMerchantNo** | **String**|  | [optional]
 **accountType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **billFormat** | **String**|  | [optional]

### Return type
[**BillFundbillApplyManualGenerationResponseDTOResult**](../model/BillFundbillApplyManualGenerationResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="billFundbillDownload"></a>
# **billFundbillDownload**
YosDownloadResponse billFundbillDownload(BillFundbillDownloadRequest request)

资金账单下载

资金账单下载

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillFundbillDownloadRequest中的参数说明参见Parameters章节
BillFundbillDownloadRequest request = new BillFundbillDownloadRequest();
request.setMerchantNo("merchantNo_example");
request.setFileId("fileId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.billFundbillDownload(request);
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
    LOGGER.error("Exception when calling StdClient#billFundbillDownload, ex:", e);
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
 **fileId** | **String**|  |

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

<a name="billFundbillEndbalanceApply"></a>
# **billFundbillEndbalanceApply**
BillFundbillEndbalanceApplyResponse billFundbillEndbalanceApply(BillFundbillEndbalanceApplyRequest request)

日终余额账单申请

日终余额账单申请

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillFundbillEndbalanceApplyRequest中的参数说明参见Parameters章节
BillFundbillEndbalanceApplyRequest request = new BillFundbillEndbalanceApplyRequest();
request.setBookDate("bookDate_example");
request.setMerchantNo("merchantNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setSubMerchantNo("subMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillFundbillEndbalanceApplyResponse response = api.billFundbillEndbalanceApply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling StdClient#billFundbillEndbalanceApply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bookDate** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **subMerchantNo** | **String**|  | [optional]

### Return type
[**BillFundbillEndbalanceApplyManualGenerationEndBalanceResponseDTOResult**](../model/BillFundbillEndbalanceApplyManualGenerationEndBalanceResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="billFundbillFlowQuery"></a>
# **billFundbillFlowQuery**
BillFundbillFlowQueryResponse billFundbillFlowQuery(BillFundbillFlowQueryRequest request)

资金流水明细查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillFundbillFlowQueryRequest中的参数说明参见Parameters章节
BillFundbillFlowQueryRequest request = new BillFundbillFlowQueryRequest();
request.setStartDate("startDate_example");
request.setEndDate("endDate_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setPage(56);
request.setSize(56);
request.setTrxCode("trxCode_example");
request.setAccountType("accountType_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillFundbillFlowQueryResponse response = api.billFundbillFlowQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling StdClient#billFundbillFlowQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| 格式应为yyyy-MM-dd |
 **endDate** | **String**| 格式应为yyyy-MM-dd,与startDate最大日期间隔为31天 |
 **parentMerchantNo** | **String**| 1.父商编与子商户一致查父商编自己流水;  2.父商编与子商户不一致，查子商户流水（服务商解决方案下，查平台下的入驻商户时,父商编传平台商商编）;  3.子商户编号为空，查父商编下所有流水 |
 **page** | **Integer**| 默认1，最小为1 |
 **size** | **Integer**| 默认20,最小为1,最大100 |
 **trxCode** | **String**| 商户传入1001,接口返回中文收单。&lt;br&gt;业务类型可选项如下:&lt;br&gt;1001:收单&lt;br&gt;1002:分账&lt;br&gt;1003:分账退回&lt;br&gt;1004:退款&lt;br&gt;1005:充值&lt;br&gt;1006:转账&lt;br&gt;1010:退款撤销&lt;br&gt;2004:提现&lt;br&gt;2005:企业付款&lt;br&gt;2006:收费(鉴权)&lt;br&gt;2007:收费撤销&lt;br&gt;2009:支付账户支付&lt;br&gt;2011:日结通&lt;br&gt;2012:快速实名认证&lt;br&gt;2026:划拨&lt;br&gt;2027:资金归集&lt;br&gt;2028:营销账户退款&lt;br&gt;2029:营销账户支付&lt;br&gt;2035:补贴商户入账&lt;br&gt;2037:OCR识别&lt;br&gt;2038:OCR识别撤销&lt;br&gt;4001:结算 | [optional]
 **accountType** | **String**| 账户类型可选项如下:&lt;br&gt;FUND_ACCOUNT:资金账户&lt;br&gt;SETTLE_ACCOUNT:待结算账户&lt;br&gt;DIVIDE_ACCOUNT:待分账账户&lt;br&gt;FEE_ACCOUNT:手续费账户&lt;br&gt;BASIC_ACCOUNT:基本账户&lt;br&gt;MARKET_ACCOUNT:营销账&lt;br&gt;SPECIAL_FUND_ACCOUNT:专款账户&lt;br&gt;ADVANCE_ACCOUNT:预收账户 | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BillFundbillFlowQueryYopQueryFundBillFlowResponseDTOResult**](../model/BillFundbillFlowQueryYopQueryFundBillFlowResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="billFundbillFlowSum"></a>
# **billFundbillFlowSum**
BillFundbillFlowSumResponse billFundbillFlowSum(BillFundbillFlowSumRequest request)

资金流水汇总查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillFundbillFlowSumRequest中的参数说明参见Parameters章节
BillFundbillFlowSumRequest request = new BillFundbillFlowSumRequest();
request.setStartDate("startDate_example");
request.setEndDate("endDate_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setTrxCode("trxCode_example");
request.setAccountType("accountType_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillFundbillFlowSumResponse response = api.billFundbillFlowSum(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling StdClient#billFundbillFlowSum, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| 格式应为yyyy-MM-dd |
 **endDate** | **String**| 格式应为yyyy-MM-dd,与startDate最大日期间隔为31天 |
 **parentMerchantNo** | **String**| 1.父商编与子商户一致查父商编自己流水;  2.父商编与子商户不一致，查子商户流水（服务商解决方案下，查平台下的入驻商户时,父商编传平台商商编）;  3.子商户编号为空，查父商编下所有流水 |
 **trxCode** | **String**| 商户传入1001,接口返回中文收单。&lt;br&gt;业务类型可选项如下:&lt;br&gt;1001:收单&lt;br&gt;1002:分账&lt;br&gt;1003:分账退回&lt;br&gt;1004:退款&lt;br&gt;1005:充值&lt;br&gt;1006:转账&lt;br&gt;1010:退款撤销&lt;br&gt;2004:提现&lt;br&gt;2005:企业付款&lt;br&gt;2006:收费(鉴权)&lt;br&gt;2007:收费撤销&lt;br&gt;2009:支付账户支付&lt;br&gt;2011:日结通&lt;br&gt;2012:快速实名认证&lt;br&gt;2026:划拨&lt;br&gt;2027:资金归集&lt;br&gt;2028:营销账户退款&lt;br&gt;2029:营销账户支付&lt;br&gt;2035:补贴商户入账&lt;br&gt;2037:OCR识别&lt;br&gt;2038:OCR识别撤销&lt;br&gt;4001:结算 | [optional]
 **accountType** | **String**| 账户类型可选项如下:&lt;br&gt;FUND_ACCOUNT:资金账户&lt;br&gt;SETTLE_ACCOUNT:待结算账户&lt;br&gt;DIVIDE_ACCOUNT:待分账账户&lt;br&gt;FEE_ACCOUNT:手续费账户&lt;br&gt;BASIC_ACCOUNT:基本账户&lt;br&gt;MARKET_ACCOUNT:营销账&lt;br&gt;SPECIAL_FUND_ACCOUNT:专款账户&lt;br&gt;ADVANCE_ACCOUNT:预收账户 | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BillFundbillFlowSumYopQueryFundBillSumResponseDTOResult**](../model/BillFundbillFlowSumYopQueryFundBillSumResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="billSettlebillDownload"></a>
# **billSettlebillDownload**
YosDownloadResponse billSettlebillDownload(BillSettlebillDownloadRequest request)

下载结算账单

下载结算账单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillSettlebillDownloadRequest中的参数说明参见Parameters章节
BillSettlebillDownloadRequest request = new BillSettlebillDownloadRequest();
request.setSettleDate("settleDate_example");
request.setMerchantNo("merchantNo_example");
request.setSettleBatchNo("settleBatchNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.billSettlebillDownload(request);
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
    LOGGER.error("Exception when calling StdClient#billSettlebillDownload, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **settleDate** | **String**| 格式yyyy-mm-dd |
 **merchantNo** | **String**|  |
 **settleBatchNo** | **String**|  | [optional]

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

<a name="billTradedaydownload"></a>
# **billTradedaydownload**
YosDownloadResponse billTradedaydownload(BillTradedaydownloadRequest request)

交易日对账下载

交易日对账下载，具体请参考对账文件说明&amp;lt;/a&amp;gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//BillTradedaydownloadRequest中的参数说明参见Parameters章节
BillTradedaydownloadRequest request = new BillTradedaydownloadRequest();
request.setMerchantNo("merchantNo_example");
request.setDayString("dayString_example");
request.setDataType("dataType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.billTradedaydownload(request);
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
    LOGGER.error("Exception when calling StdClient#billTradedaydownload, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **dayString** | **String**|  | [optional]
 **dataType** | **String**|  | [optional]

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

<a name="certOrder"></a>
# **certOrder**
CertOrderResponse certOrder(CertOrderRequest request)

新信息认证系统-认证请求



### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.std.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(StdClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
StdClient api = StdClientBuilder.builder().build();

//CertOrderRequest中的参数说明参见Parameters章节
CertOrderRequest request = new CertOrderRequest();
request.setMerchantNo("100000000000");
request.setAuthType("authType_example");
request.setRequestNo("requestNo_example");
request.setIdCardNo("230231199510101010");
request.setUserName("易小宝");
request.setBankCardNo("6217876555556554324");
request.setRequestTime("2019-09-09 00:00:00");
request.setRemark("remark_example");
request.setMobilePhone("mobilePhone_example");
request.setIdCardType("idCardType_example");
request.setClientSource("clientSource_example");
request.setExtMap("{\"verifyBsnSceneDesc\":\"描述\",\"sourceIP\":\"AD80:0000:0000:0000:ABAA:0000:00C 2:0002\",\"appType\":\"01\",\"appName\":\"某某银行直销银行\",\"verifyBsnScene\":\"99\",\"ipType\":\"06\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CertOrderResponse response = api.certOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling StdClient#certOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **authType** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **idCardNo** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **bankCardNo** | **String**|  | [optional]
 **requestTime** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **mobilePhone** | **String**|  | [optional]
 **idCardType** | **String**|  | [optional]
 **clientSource** | **String**|  | [optional]
 **extMap** | **String**|  | [optional]

### Return type
[**CertOrderAuthResponseDTOResult**](../model/CertOrderAuthResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

