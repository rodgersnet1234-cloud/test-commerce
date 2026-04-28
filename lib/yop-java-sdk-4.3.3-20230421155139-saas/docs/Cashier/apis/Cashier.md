# CashierClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**payLinkOrder**](CashierClient.md#payLinkOrder) | **POST** /rest/v1.0/cashier/pay-link/order | 生成聚合订单码
[**unifiedOrder**](CashierClient.md#unifiedOrder) | **POST** /rest/v1.0/cashier/unified/order | 收银台统一下单


<a name="payLinkOrder"></a>
# **payLinkOrder**
PayLinkOrderResponse payLinkOrder(PayLinkOrderRequest request)

生成聚合订单码

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.cashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(CashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
CashierClient api = CashierClientBuilder.builder().build();

//PayLinkOrderRequest中的参数说明参见Parameters章节
PayLinkOrderRequest request = new PayLinkOrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setGoodsName("goodsName_example");
request.setAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:06");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setScene("scene_example");
request.setFundProcessType("fundProcessType_example");
request.setAppId("appId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayLinkOrderResponse response = api.payLinkOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling CashierClient#payLinkOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **scene** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **appId** | **String**|  | [optional]

### Return type
[**PayLinkOrderAggregationPayLinkResponseDTOResult**](../model/PayLinkOrderAggregationPayLinkResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="unifiedOrder"></a>
# **unifiedOrder**
UnifiedOrderResponse unifiedOrder(UnifiedOrderRequest request)

收银台统一下单

为商户提供收银台服务，支持多种支付方式。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.cashier.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(CashierClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
CashierClient api = CashierClientBuilder.builder().build();

//UnifiedOrderRequest中的参数说明参见Parameters章节
UnifiedOrderRequest request = new UnifiedOrderRequest();
request.setParentMerchantNo("10040012345");
request.setMerchantNo("10040012345");
request.setOrderId("orderId12345");
request.setOrderAmount(new BigDecimal("0"));
request.setGoodsName("旺仔牛奶");
request.setFundProcessType("REAL_TIME");
request.setNotifyUrl("https://notify.merchant.com/xxx");
request.setMemo("memo_example");
request.setExpiredTime("2023-05-07 10:49:06");
request.setReturnUrl("https://notify.merchant.com/xxx");
request.setCsNotifyUrl("csNotifyUrl_example");
request.setBusinessInfo("businessInfo_example");
request.setPayerInfo("{\"bankCardNo\":\"6225750005831234\",\"cardName\":\"爱丽丝\",\"idCardNo\":\"130225199006093323\",\"mobilePhoneNo\":\"13902092131\",\"userID\":\"20056788\"}");
request.setLimitPayType("\"YJZF,EBANK_B2B,BANK_TRANSFER_PAY\");
request.setCardType("DEBIT");
request.setAggParam("{“appId”:”wx9e13bd68a8f1921e”,”openId”:”zml_wechat”}");
request.setNoCardParam("{\"userNo\":\"111\",\"userType\":\"USER_ID\"}");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UnifiedOrderResponse response = api.unifiedOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling CashierClient#unifiedOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **csNotifyUrl** | **String**|  | [optional]
 **businessInfo** | **String**|  | [optional]
 **payerInfo** | **String**|  | [optional]
 **limitPayType** | **String**|  | [optional]
 **cardType** | **String**|  | [optional]
 **aggParam** | **String**|  | [optional]
 **noCardParam** | **String**|  | [optional]

### Return type
[**UnifiedOrderUnifiedCashierOrderResponseDTOResult**](../model/UnifiedOrderUnifiedCashierOrderResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

