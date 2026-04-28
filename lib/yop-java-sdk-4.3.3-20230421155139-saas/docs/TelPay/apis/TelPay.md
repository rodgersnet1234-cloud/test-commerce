# TelPayClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**qrcodeBatchGenerate**](TelPayClient.md#qrcodeBatchGenerate) | **POST** /rest/v1.0/tel-pay/qrcode/batch-generate | 批量生成二维码接口
[**qrcodeQuery**](TelPayClient.md#qrcodeQuery) | **GET** /rest/v1.0/tel-pay/qrcode/query | 查询二维码信息


<a name="qrcodeBatchGenerate"></a>
# **qrcodeBatchGenerate**
QrcodeBatchGenerateResponse qrcodeBatchGenerate(QrcodeBatchGenerateRequest request)

批量生成二维码接口

支持商户生成易宝通台牌二维码，支持批量生成多个二维码

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.tel_pay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TelPayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TelPayClient api = TelPayClientBuilder.builder().build();

//QrcodeBatchGenerateRequest中的参数说明参见Parameters章节
QrcodeBatchGenerateRequest request = new QrcodeBatchGenerateRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestId("requestId_example");
request.setQrCodeInfo("qrCodeInfo_example");
request.setDistrictCode("districtCode_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QrcodeBatchGenerateResponse response = api.qrcodeBatchGenerate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TelPayClient#qrcodeBatchGenerate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestId** | **String**|  | [optional]
 **qrCodeInfo** | **String**|  | [optional]
 **districtCode** | **String**|  | [optional]

### Return type
[**QrcodeBatchGenerateBatchGenerateQrCodeResponseDTOResult**](../model/QrcodeBatchGenerateBatchGenerateQrCodeResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="qrcodeQuery"></a>
# **qrcodeQuery**
QrcodeQueryResponse qrcodeQuery(QrcodeQueryRequest request)

查询二维码信息

支持查询商户下的易宝通台牌二维码信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.tel_pay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TelPayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TelPayClient api = TelPayClientBuilder.builder().build();

//QrcodeQueryRequest中的参数说明参见Parameters章节
QrcodeQueryRequest request = new QrcodeQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestId("requestId_example");
request.setPageSize(56);
request.setPageNo(56);
request.setQrId("qrId_example");
request.setStartTime("startTime_example");
request.setEndTime("endTime_example");
request.setQrStatus("qrStatus_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QrcodeQueryResponse response = api.qrcodeQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TelPayClient#qrcodeQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  |
 **merchantNo** | **String**|  |
 **requestId** | **String**|  |
 **pageSize** | **Integer**|  |
 **pageNo** | **Integer**|  |
 **qrId** | **String**|  | [optional]
 **startTime** | **String**| yyyy-MM-dd HH:mm:ss | [optional]
 **endTime** | **String**| yyyy-MM-dd HH:mm:ss | [optional]
 **qrStatus** | **String**| 二维码状态&lt;br&gt;可选项如下:&lt;br&gt;INACTIVE:已关闭&lt;br&gt;ACTIVE:已开通 | [optional]

### Return type
[**QrcodeQueryQueryQrCodeApiResponseDTOResult**](../model/QrcodeQueryQueryQrCodeApiResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

