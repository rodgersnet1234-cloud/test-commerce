# TravelResourcesClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createOrder**](TravelResourcesClient.md#createOrder) | **POST** /rest/v1.0/travel-resources/create-order | 创建电影票订单
[**kfcOrder**](TravelResourcesClient.md#kfcOrder) | **POST** /rest/v1.0/travel-resources/kfc-order | 创建KFC订单
[**queryKfcOrder**](TravelResourcesClient.md#queryKfcOrder) | **POST** /rest/v1.0/travel-resources/query-kfc-order | 查询KFC订单
[**queryOrder**](TravelResourcesClient.md#queryOrder) | **POST** /rest/v1.0/travel-resources/query-cinema-order | 查询电影票订单


<a name="createOrder"></a>
# **createOrder**
CreateOrderResponse createOrder(CreateOrderRequest request)

创建电影票订单

电影票品类下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.travel_resources.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TravelResourcesClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TravelResourcesClient api = TravelResourcesClientBuilder.builder().build();

//CreateOrderRequest中的参数说明参见Parameters章节
CreateOrderRequest request = new CreateOrderRequest();
request.setBody(new CinemaOrderRequestDTO());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CreateOrderResponse response = api.createOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TravelResourcesClient#createOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CinemaOrderRequestDTO**](../model/CinemaOrderRequestDTO.md)|  | [optional]

### Return type
[**OrderBaseResponseDTO**](../model/OrderBaseResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="kfcOrder"></a>
# **kfcOrder**
KfcOrderResponse kfcOrder(KfcOrderRequest request)

创建KFC订单

创建KFC订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.travel_resources.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TravelResourcesClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TravelResourcesClient api = TravelResourcesClientBuilder.builder().build();

//KfcOrderRequest中的参数说明参见Parameters章节
KfcOrderRequest request = new KfcOrderRequest();
request.setBody(new KfcOrderRequestDTO());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    KfcOrderResponse response = api.kfcOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TravelResourcesClient#kfcOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**KfcOrderRequestDTO**](../model/KfcOrderRequestDTO.md)|  | [optional]

### Return type
[**OrderBaseResponseDTO**](../model/OrderBaseResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="queryKfcOrder"></a>
# **queryKfcOrder**
QueryKfcOrderResponse queryKfcOrder(QueryKfcOrderRequest request)

查询KFC订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.travel_resources.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TravelResourcesClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TravelResourcesClient api = TravelResourcesClientBuilder.builder().build();

//QueryKfcOrderRequest中的参数说明参见Parameters章节
QueryKfcOrderRequest request = new QueryKfcOrderRequest();
request.setBody(new QueryOrderRequestDTO());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryKfcOrderResponse response = api.queryKfcOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TravelResourcesClient#queryKfcOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**QueryOrderRequestDTO**](../model/QueryOrderRequestDTO.md)|  | [optional]

### Return type
[**QueryKfcOrderResponseDTO**](../model/QueryKfcOrderResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="queryOrder"></a>
# **queryOrder**
QueryOrderResponse queryOrder(QueryOrderRequest request)

查询电影票订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.travel_resources.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(TravelResourcesClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
TravelResourcesClient api = TravelResourcesClientBuilder.builder().build();

//QueryOrderRequest中的参数说明参见Parameters章节
QueryOrderRequest request = new QueryOrderRequest();
request.setBody(new QueryOrderRequestDTO());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryOrderResponse response = api.queryOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling TravelResourcesClient#queryOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**QueryOrderRequestDTO**](../model/QueryOrderRequestDTO.md)|  | [optional]

### Return type
[**QueryCinemaOrderResponseDTO**](../model/QueryCinemaOrderResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

