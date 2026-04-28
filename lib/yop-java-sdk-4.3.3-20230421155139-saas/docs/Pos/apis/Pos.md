# PosClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPosInfoDtos**](PosClient.md#getPosInfoDtos) | **POST** /rest/v1.0/pos/get-pos-info-dtos | 机具信息查询
[**installPosWithProduct**](PosClient.md#installPosWithProduct) | **POST** /rest/v1.0/pos/install-pos-with-product | 代理商绑机接口
[**unSynBindPos**](PosClient.md#unSynBindPos) | **POST** /rest/v1.0/pos/un-syn-bind-pos | 代理商解绑接口


<a name="getPosInfoDtos"></a>
# **getPosInfoDtos**
GetPosInfoDtosResponse getPosInfoDtos(GetPosInfoDtosRequest request)

机具信息查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.pos.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PosClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PosClient api = PosClientBuilder.builder().build();

//GetPosInfoDtosRequest中的参数说明参见Parameters章节
GetPosInfoDtosRequest request = new GetPosInfoDtosRequest();
request.setCustomerNumber("customerNumber_example");
request.setPosCati("0000010484250011");
request.setSerialNumber("15706413");
request.setShopName("shopName_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    GetPosInfoDtosResponse response = api.getPosInfoDtos(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PosClient#getPosInfoDtos, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerNumber** | **String**|  | [optional]
 **posCati** | **String**|  | [optional]
 **serialNumber** | **String**|  | [optional]
 **shopName** | **String**|  | [optional]

### Return type
[**GetPosInfoDtosPosInfoResponseParamResult**](../model/GetPosInfoDtosPosInfoResponseParamResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="installPosWithProduct"></a>
# **installPosWithProduct**
InstallPosWithProductResponse installPosWithProduct(InstallPosWithProductRequest request)

代理商绑机接口

代理商绑机接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.pos.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PosClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PosClient api = PosClientBuilder.builder().build();

//InstallPosWithProductRequest中的参数说明参见Parameters章节
InstallPosWithProductRequest request = new InstallPosWithProductRequest();
request.setBody(new InstallPosWithProductInstallPosWithProductParamParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    InstallPosWithProductResponse response = api.installPosWithProduct(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PosClient#installPosWithProduct, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**InstallPosWithProductInstallPosWithProductParamParam**](../model/InstallPosWithProductInstallPosWithProductParamParam.md)|  |

### Return type
**String**

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="unSynBindPos"></a>
# **unSynBindPos**
UnSynBindPosResponse unSynBindPos(UnSynBindPosRequest request)

代理商解绑接口

代理商解绑接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.pos.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(PosClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
PosClient api = PosClientBuilder.builder().build();

//UnSynBindPosRequest中的参数说明参见Parameters章节
UnSynBindPosRequest request = new UnSynBindPosRequest();
request.setCustomerNumber("customerNumber_example");
request.setPoscati("0000010484250011");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UnSynBindPosResponse response = api.unSynBindPos(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling PosClient#unSynBindPos, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customerNumber** | **String**|  | [optional]
 **poscati** | **String**|  | [optional]

### Return type
**String**

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

