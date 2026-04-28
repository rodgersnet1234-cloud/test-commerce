# CnppayClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**installmentPayRequest**](CnppayClient.md#installmentPayRequest) | **POST** /rest/v1.0/cnppay/installment/pay/request | 分期支付统一下单
[**installmentQuerybankcfg**](CnppayClient.md#installmentQuerybankcfg) | **GET** /rest/v1.0/cnppay/installment/querybankcfg | 分期支付商户支持银行信息查询


<a name="installmentPayRequest"></a>
# **installmentPayRequest**
InstallmentPayRequestResponse installmentPayRequest(InstallmentPayRequestRequest request)

分期支付统一下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.cnppay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(CnppayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
CnppayClient api = CnppayClientBuilder.builder().build();

//InstallmentPayRequestRequest中的参数说明参见Parameters章节
InstallmentPayRequestRequest request = new InstallmentPayRequestRequest();
request.setParentMerchantNo("10012345677");
request.setMerchantNo("10012345677");
request.setOrderAmount(new BigDecimal("0"));
request.setOrderId("221007104428249784269");
request.setFundProcessType("fundProcessType_example");
request.setBankId("bankId_example");
request.setExpireTime("expireTime_example");
request.setGoodsName("goodsName_example");
request.setNumOfInstallment(56);
request.setRiskInfo("riskInfo_example");
request.setRedirectUrl("redirectUrl_example");
request.setNotifyUrl("notifyUrl_example");
request.setCsUrl("csUrl_example");
request.setMemo("memo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    InstallmentPayRequestResponse response = api.installmentPayRequest(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling CnppayClient#installmentPayRequest, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **orderId** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **bankId** | **String**|  | [optional]
 **expireTime** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **numOfInstallment** | **Integer**|  | [optional]
 **riskInfo** | **String**|  | [optional]
 **redirectUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]

### Return type
[**InstallmentPayRequestInstallmentPayResponseDTOResult**](../model/InstallmentPayRequestInstallmentPayResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="installmentQuerybankcfg"></a>
# **installmentQuerybankcfg**
InstallmentQuerybankcfgResponse installmentQuerybankcfg(InstallmentQuerybankcfgRequest request)

分期支付商户支持银行信息查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.cnppay.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(CnppayClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
CnppayClient api = CnppayClientBuilder.builder().build();

//InstallmentQuerybankcfgRequest中的参数说明参见Parameters章节
InstallmentQuerybankcfgRequest request = new InstallmentQuerybankcfgRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("10012345677");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    InstallmentQuerybankcfgResponse response = api.installmentQuerybankcfg(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling CnppayClient#installmentQuerybankcfg, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;*标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**|  |

### Return type
[**InstallmentQuerybankcfgInstallmentBankCfgResponseDTOResult**](../model/InstallmentQuerybankcfgInstallmentBankCfgResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

