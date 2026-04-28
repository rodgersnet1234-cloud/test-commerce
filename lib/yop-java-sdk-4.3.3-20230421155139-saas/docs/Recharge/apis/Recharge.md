# RechargeClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bankAccountQuery**](RechargeClient.md#bankAccountQuery) | **GET** /rest/v1.0/recharge/bank-account/query | 银行账户查询余额


<a name="bankAccountQuery"></a>
# **bankAccountQuery**
BankAccountQueryResponse bankAccountQuery(BankAccountQueryRequest request)

银行账户查询余额

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.recharge.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(RechargeClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
RechargeClient api = RechargeClientBuilder.builder().build();

//BankAccountQueryRequest中的参数说明参见Parameters章节
BankAccountQueryRequest request = new BankAccountQueryRequest();
request.setBankCode("bankCode_example");
request.setAccountNo("accountNo_example");
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryResponse response = api.bankAccountQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling RechargeClient#bankAccountQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bankCode** | **String**| FJHTB 华通银行&lt;br&gt;XIB 厦门银行&lt;br&gt;WHZBB 众邦银行 |
 **accountNo** | **String**|  |
 **merchantNo** | **String**| 需查询余额的银行账号对应的易宝商编 |
 **parentMerchantNo** | **String**| *标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为服务商商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |

### Return type
[**BankAccountQueryQueryBankAccountRespDTOResult**](../model/BankAccountQueryQueryBankAccountRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

