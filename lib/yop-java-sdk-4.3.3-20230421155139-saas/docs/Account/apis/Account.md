# AccountClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountBookQueryRefund**](AccountClient.md#accountBookQueryRefund) | **GET** /rest/v1.0/account/account-book/query-refund | 记账簿退款查询
[**accountBookRefund**](AccountClient.md#accountBookRefund) | **POST** /rest/v1.0/account/account-book/refund | 记账簿退款
[**accountManageAccountOpen**](AccountClient.md#accountManageAccountOpen) | **POST** /rest/v1.0/account/account-manage/account/open | 开立记账簿
[**accountManageAccountQuery**](AccountClient.md#accountManageAccountQuery) | **GET** /rest/v1.0/account/account-manage/account/query | 查询记账簿
[**accountManageBankAccountOpen**](AccountClient.md#accountManageBankAccountOpen) | **POST** /rest/v1.0/account/account-manage/bank-account/open | 开立银行账户
[**accountManageBankAccountQuery**](AccountClient.md#accountManageBankAccountQuery) | **GET** /rest/v1.0/account/account-manage/bank-account/query | 开立银行账户查询
[**account_individual_apply**](AccountClient.md#account_individual_apply) | **POST** /rest/v1.0/account/individual/apply | 付款到个人--申请添加个人用户
[**account_individual_query**](AccountClient.md#account_individual_query) | **POST** /rest/v1.0/account/individual/query | 付款到个人--查询已添加的个人用户
[**account_individual_query_progress**](AccountClient.md#account_individual_query_progress) | **POST** /rest/v1.0/account/individual/query-progress | 付款到个人--查询申请进度
[**accountinfosQuery**](AccountClient.md#accountinfosQuery) | **GET** /rest/v1.0/account/accountinfos/query | 全部账户余额查询
[**autoWithdrawRuleCancel**](AccountClient.md#autoWithdrawRuleCancel) | **POST** /rest/v1.0/account/auto-withdraw-rule/cancel | 自动提现-规则作废
[**autoWithdrawRuleQuery**](AccountClient.md#autoWithdrawRuleQuery) | **GET** /rest/v1.0/account/auto-withdraw-rule/query | 自动提现-规则查询
[**autoWithdrawRuleSet**](AccountClient.md#autoWithdrawRuleSet) | **POST** /rest/v1.0/account/auto-withdraw-rule/set | 自动提现-规则设置
[**balanceQuery**](AccountClient.md#balanceQuery) | **GET** /rest/v1.0/account/balance/query | 资金账户余额查询
[**bankPaymentOrder**](AccountClient.md#bankPaymentOrder) | **POST** /rest/v1.0/account/bank/payment/order | 银行账户支付
[**enterpriseAccountBookPayOrder**](AccountClient.md#enterpriseAccountBookPayOrder) | **POST** /rest/v1.0/account/enterprise/account-book-pay/order | 记账薄支付
[**enterpriseAccountPayOrder**](AccountClient.md#enterpriseAccountPayOrder) | **POST** /rest/v1.0/account/enterprise/account-pay/order | 企业账户支付-下单
[**enterpriseAutoPaymentOrder**](AccountClient.md#enterpriseAutoPaymentOrder) | **POST** /rest/v1.0/account/enterprise/auto-payment/order | 企业账户支付-自动付款
[**enterpriseAutoPaymentQuery**](AccountClient.md#enterpriseAutoPaymentQuery) | **GET** /rest/v1.0/account/enterprise/auto-payment/query | 企业账户支付-自动付款订单查询
[**enterpriseTokenPayOrder**](AccountClient.md#enterpriseTokenPayOrder) | **POST** /rest/v1.0/account/enterprise/token-pay/order | 企业账户支付-token支付
[**enterpriseWithholdingOrder**](AccountClient.md#enterpriseWithholdingOrder) | **POST** /rest/v1.0/account/enterprise/withholding/order | 企业账户支付-关系扣款
[**externalOrder**](AccountClient.md#externalOrder) | **POST** /rest/v1.0/account/external/order | 银行账户支付-外部订单同步
[**payBatchOrder**](AccountClient.md#payBatchOrder) | **POST** /rest/v1.0/account/pay/batch-order | 付款-批量下单
[**payBatchQuery**](AccountClient.md#payBatchQuery) | **GET** /rest/v1.0/account/pay/batch-query | 付款-批次查询
[**payCancel**](AccountClient.md#payCancel) | **POST** /rest/v1.0/account/pay/cancel | 付款-撤销
[**payOrder**](AccountClient.md#payOrder) | **POST** /rest/v1.0/account/pay/order | 付款-下单
[**payQuery**](AccountClient.md#payQuery) | **GET** /rest/v1.0/account/pay/query | 付款-查询
[**paySystemQuery**](AccountClient.md#paySystemQuery) | **GET** /rest/v1.0/account/pay/system/query | 付款-查询
[**receiptGather**](AccountClient.md#receiptGather) | **POST** /rest/v1.0/account/receipt/gather | 获取资金汇总凭证
[**receiptGet**](AccountClient.md#receiptGet) | **GET** /rest/v1.0/account/receipt/get | 电子回单-下载
[**recharge**](AccountClient.md#recharge) | **POST** /rest/v1.0/account/recharge | 充值-下单（多种支付）
[**rechargeAccountBookQuery**](AccountClient.md#rechargeAccountBookQuery) | **GET** /rest/v1.0/account/recharge/account-book/query | 批量查询记账簿来账流水
[**rechargeBatchQuery**](AccountClient.md#rechargeBatchQuery) | **GET** /rest/v1.0/account/recharge/batch-query | 充值订单批量查询
[**rechargeOnlinebankOrder**](AccountClient.md#rechargeOnlinebankOrder) | **POST** /rest/v1.0/account/recharge/onlinebank/order | 充值-网银下单
[**rechargeOrder**](AccountClient.md#rechargeOrder) | **POST** /rest/v1.0/account/recharge/order | 充值-银行汇款下单
[**rechargeQuery**](AccountClient.md#rechargeQuery) | **GET** /rest/v1.0/account/recharge/query | 充值-查询
[**setWithdrawRule**](AccountClient.md#setWithdrawRule) | **POST** /rest/v1.0/account/set-withdraw-rule | 设置提现规则
[**supplierApply**](AccountClient.md#supplierApply) | **POST** /rest/v1.0/account/supplier/apply | 付款到供应商--申请添加供应商
[**supplierPayOrder**](AccountClient.md#supplierPayOrder) | **POST** /rest/v1.0/account/supplier/pay/order | 付款到供应商-下单
[**supplierQuery**](AccountClient.md#supplierQuery) | **GET** /rest/v1.0/account/supplier/query | 付款到供应商--查询已添加的供应商
[**supplierQueryProgress**](AccountClient.md#supplierQueryProgress) | **GET** /rest/v1.0/account/supplier/query-progress | 付款到供应商--查询申请进度
[**transferB2bOrder**](AccountClient.md#transferB2bOrder) | **POST** /rest/v1.0/account/transfer/b2b/order | 转账-下单
[**transferB2bQuery**](AccountClient.md#transferB2bQuery) | **GET** /rest/v1.0/account/transfer/b2b/query | 转账-查询
[**transferSystemQuery**](AccountClient.md#transferSystemQuery) | **GET** /rest/v1.0/account/transfer/system/query | 转账-查询
[**transferWechatOrder**](AccountClient.md#transferWechatOrder) | **POST** /rest/v1.0/account/transfer/wechat/order | 转账到微信零钱-下单
[**transferWechatQuery**](AccountClient.md#transferWechatQuery) | **GET** /rest/v1.0/account/transfer/wechat/query | 转账到微信零钱-查询
[**withdrawCardBind**](AccountClient.md#withdrawCardBind) | **POST** /rest/v1.0/account/withdraw/card/bind | 提现卡-添加
[**withdrawCardModify**](AccountClient.md#withdrawCardModify) | **POST** /rest/v1.0/account/withdraw/card/modify | 提现卡-修改/注销
[**withdrawCardQuery**](AccountClient.md#withdrawCardQuery) | **GET** /rest/v1.0/account/withdraw/card/query | 提现卡查询
[**withdrawOrder**](AccountClient.md#withdrawOrder) | **POST** /rest/v1.0/account/withdraw/order | 提现-下单
[**withdrawQuery**](AccountClient.md#withdrawQuery) | **GET** /rest/v1.0/account/withdraw/query | 提现-查询
[**withdrawSystemQuery**](AccountClient.md#withdrawSystemQuery) | **GET** /rest/v1.0/account/withdraw/system/query | 提现-查询


<a name="accountBookQueryRefund"></a>
# **accountBookQueryRefund**
AccountBookQueryRefundResponse accountBookQueryRefund(AccountBookQueryRefundRequest request)

记账簿退款查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountBookQueryRefundRequest中的参数说明参见Parameters章节
AccountBookQueryRefundRequest request = new AccountBookQueryRefundRequest();
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantRefundRequestNo("merchantRefundRequestNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountBookQueryRefundResponse response = api.accountBookQueryRefund(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountBookQueryRefund, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 收款商户商编 |
 **parentMerchantNo** | **String**| 发起方商户编号。&lt;br&gt;*标准商户收付款方案中此参数与收款商户编号一致；&lt;br&gt;*平台商户收付款方案中此参数为平台商商户编号；&lt;br&gt;*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantRefundRequestNo** | **String**| 商户退款请求号。可包含字母、数字、下划线；需保证在商户端不重复 |

### Return type
[**AccountBookQueryRefundQueryAccountBookRefundRespDTOResult**](../model/AccountBookQueryRefundQueryAccountBookRefundRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountBookRefund"></a>
# **accountBookRefund**
AccountBookRefundResponse accountBookRefund(AccountBookRefundRequest request)

记账簿退款

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountBookRefundRequest中的参数说明参见Parameters章节
AccountBookRefundRequest request = new AccountBookRefundRequest();
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantRefundRequestNo("merchantRefundRequestNo_example");
request.setOriginalOrderNo("originalOrderNo_example");
request.setRefundAmount(new BigDecimal("0"));
request.setBankPostscrip("bankPostscrip_example");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountBookRefundResponse response = api.accountBookRefund(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountBookRefund, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantRefundRequestNo** | **String**|  | [optional]
 **originalOrderNo** | **String**|  | [optional]
 **refundAmount** | **BigDecimal**|  | [optional]
 **bankPostscrip** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**AccountBookRefundAccountBookRefundRespDTOResult**](../model/AccountBookRefundAccountBookRefundRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountManageAccountOpen"></a>
# **accountManageAccountOpen**
AccountManageAccountOpenResponse accountManageAccountOpen(AccountManageAccountOpenRequest request)

开立记账簿

商户请求该接口，申请开通买家记账簿

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountManageAccountOpenRequest中的参数说明参见Parameters章节
AccountManageAccountOpenRequest request = new AccountManageAccountOpenRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantAccountBookNo("merchantAccountBookNo_example");
request.setMerchantAccountBookName("merchantAccountBookName_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountManageAccountOpenResponse response = api.accountManageAccountOpen(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountManageAccountOpen, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantAccountBookNo** | **String**|  | [optional]
 **merchantAccountBookName** | **String**|  | [optional]

### Return type
[**AccountManageAccountOpenAccountBookCreateResponseDtoResult**](../model/AccountManageAccountOpenAccountBookCreateResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountManageAccountQuery"></a>
# **accountManageAccountQuery**
AccountManageAccountQueryResponse accountManageAccountQuery(AccountManageAccountQueryRequest request)

查询记账簿

商户请求该接口，查询相应记账簿余额。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountManageAccountQueryRequest中的参数说明参见Parameters章节
AccountManageAccountQueryRequest request = new AccountManageAccountQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantAccountBookNo("merchantAccountBookNo_example");
request.setYpAccountBookNo("ypAccountBookNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountManageAccountQueryResponse response = api.accountManageAccountQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountManageAccountQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号 |
 **merchantNo** | **String**| 记账簿所属的商户编号 |
 **merchantAccountBookNo** | **String**| 商户侧记账簿编号和易宝记账簿编号至少有其中一个 | [optional]
 **ypAccountBookNo** | **String**| 商户侧记账簿编号和易宝记账簿编号至少有其中一个 | [optional]

### Return type
[**AccountManageAccountQueryAccountBalanceQueryResponseDtoResult**](../model/AccountManageAccountQueryAccountBalanceQueryResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountManageBankAccountOpen"></a>
# **accountManageBankAccountOpen**
AccountManageBankAccountOpenResponse accountManageBankAccountOpen(AccountManageBankAccountOpenRequest request)

开立银行账户

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountManageBankAccountOpenRequest中的参数说明参见Parameters章节
AccountManageBankAccountOpenRequest request = new AccountManageBankAccountOpenRequest();
request.setBody(new AccountManageBankAccountOpenStandardOpenAccountRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountManageBankAccountOpenResponse response = api.accountManageBankAccountOpen(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountManageBankAccountOpen, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AccountManageBankAccountOpenStandardOpenAccountRequestDTOParam**](../model/AccountManageBankAccountOpenStandardOpenAccountRequestDTOParam.md)|  |

### Return type
[**AccountManageBankAccountOpenStandardOpenAccountResponseDTOResult**](../model/AccountManageBankAccountOpenStandardOpenAccountResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="accountManageBankAccountQuery"></a>
# **accountManageBankAccountQuery**
AccountManageBankAccountQueryResponse accountManageBankAccountQuery(AccountManageBankAccountQueryRequest request)

开立银行账户查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountManageBankAccountQueryRequest中的参数说明参见Parameters章节
AccountManageBankAccountQueryRequest request = new AccountManageBankAccountQueryRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountManageBankAccountQueryResponse response = api.accountManageBankAccountQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountManageBankAccountQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**| 商户订单号 |
 **parentMerchantNo** | **String**| *标准商户收付款方案中此参数与开户商户编号一致；*平台商户收付款方案中此参数为平台商商户编号；*服务商解决方案中，①所属标准商户申请开户时，该参数为服务商商编 ②所属平台商申请开户且以服务资质在银行开立母户时，此参数填写服务商商户编号 ②所属平台商入驻商户申请开户时需以平台资质在银行开立母户，该参数填写平台商商编 |
 **merchantNo** | **String**| 业务主体商编 |

### Return type
[**AccountManageBankAccountQueryStandardOpenAccountQueryResponseDTOResult**](../model/AccountManageBankAccountQueryStandardOpenAccountQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_individual_apply"></a>
# **account_individual_apply**
AccountIndividualApplyResponse account_individual_apply(AccountIndividualApplyRequest request)

付款到个人--申请添加个人用户

此服务针对于有付款给个人收款方且不满足使用企业付款场景的商户使用。商户向常用个人用户付款前，请先通过此接口申请添加个人用户信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountIndividualApplyRequest中的参数说明参见Parameters章节
AccountIndividualApplyRequest request = new AccountIndividualApplyRequest();
request.setMerchantNo("merchantNo_example");
request.setRequestNo("requestNo_example");
request.setName("name_example");
request.setCertificateType("IDCARD");
request.setCertificateNo("certificateNo_example");
request.setPhone("phone_example");
request.setFrontUrl("frontUrl_example");
request.setContraryUrl("contraryUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountIndividualApplyResponse response = api.account_individual_apply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#account_individual_apply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **certificateType** | **String**|  | [optional] [enum: IDCARD]
 **certificateNo** | **String**|  | [optional]
 **phone** | **String**|  | [optional]
 **frontUrl** | **String**|  | [optional]
 **contraryUrl** | **String**|  | [optional]

### Return type
[**ApplyIndividualRespDTO**](../model/ApplyIndividualRespDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_individual_query"></a>
# **account_individual_query**
AccountIndividualQueryResponse account_individual_query(AccountIndividualQueryRequest request)

付款到个人--查询已添加的个人用户

通过此服务查询付款商户已经添加的个人用户信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountIndividualQueryRequest中的参数说明参见Parameters章节
AccountIndividualQueryRequest request = new AccountIndividualQueryRequest();
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountIndividualQueryResponse response = api.account_individual_query(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#account_individual_query, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]

### Return type
[**QueryIndividualRespDTO**](../model/QueryIndividualRespDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_individual_query_progress"></a>
# **account_individual_query_progress**
AccountIndividualQueryProgressResponse account_individual_query_progress(AccountIndividualQueryProgressRequest request)

付款到个人--查询申请进度

通过此接口服务查询个人用户添加进度

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountIndividualQueryProgressRequest中的参数说明参见Parameters章节
AccountIndividualQueryProgressRequest request = new AccountIndividualQueryProgressRequest();
request.setRequestNo("requestNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountIndividualQueryProgressResponse response = api.account_individual_query_progress(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#account_individual_query_progress, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]

### Return type
[**ApplyIndivdualProgressRespDTO**](../model/ApplyIndivdualProgressRespDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountinfosQuery"></a>
# **accountinfosQuery**
AccountinfosQueryResponse accountinfosQuery(AccountinfosQueryRequest request)

全部账户余额查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AccountinfosQueryRequest中的参数说明参见Parameters章节
AccountinfosQueryRequest request = new AccountinfosQueryRequest();
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountinfosQueryResponse response = api.accountinfosQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#accountinfosQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |

### Return type
[**AccountinfosQueryQueryAccountInfoListRespDTOResult**](../model/AccountinfosQueryQueryAccountInfoListRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="autoWithdrawRuleCancel"></a>
# **autoWithdrawRuleCancel**
AutoWithdrawRuleCancelResponse autoWithdrawRuleCancel(AutoWithdrawRuleCancelRequest request)

自动提现-规则作废

自动提现-规则作废

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AutoWithdrawRuleCancelRequest中的参数说明参见Parameters章节
AutoWithdrawRuleCancelRequest request = new AutoWithdrawRuleCancelRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRuleId("ruleId_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoWithdrawRuleCancelResponse response = api.autoWithdrawRuleCancel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#autoWithdrawRuleCancel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **ruleId** | **String**|  | [optional]

### Return type
[**AutoWithdrawRuleCancelYopAutoWithdrawRuleCancelResponseDTOResult**](../model/AutoWithdrawRuleCancelYopAutoWithdrawRuleCancelResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="autoWithdrawRuleQuery"></a>
# **autoWithdrawRuleQuery**
AutoWithdrawRuleQueryResponse autoWithdrawRuleQuery(AutoWithdrawRuleQueryRequest request)

自动提现-规则查询

自动提现-规则查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AutoWithdrawRuleQueryRequest中的参数说明参见Parameters章节
AutoWithdrawRuleQueryRequest request = new AutoWithdrawRuleQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoWithdrawRuleQueryResponse response = api.autoWithdrawRuleQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#autoWithdrawRuleQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号。*标准商户收付款方案中此参数与收款商户编号一致；*平台商户收付款方案中此参数为平台商商户编号；*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编。 |
 **merchantNo** | **String**| 提现商户编号 |

### Return type
[**AutoWithdrawRuleQueryYopAutoWithdrawRuleQueryResponseDTOResult**](../model/AutoWithdrawRuleQueryYopAutoWithdrawRuleQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="autoWithdrawRuleSet"></a>
# **autoWithdrawRuleSet**
AutoWithdrawRuleSetResponse autoWithdrawRuleSet(AutoWithdrawRuleSetRequest request)

自动提现-规则设置

自动提现-规则设置

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//AutoWithdrawRuleSetRequest中的参数说明参见Parameters章节
AutoWithdrawRuleSetRequest request = new AutoWithdrawRuleSetRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setBindId("bindId_example");
request.setBankAccountNo("bankAccountNo_example");
request.setReceiveType("receiveType_example");
request.setTriggerTime("triggerTime_example");
request.setRemainAmount(new BigDecimal("0"));
request.setRemark("remark_example");
request.setNotifyAddress("notifyAddress_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoWithdrawRuleSetResponse response = api.autoWithdrawRuleSet(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#autoWithdrawRuleSet, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **bindId** | **String**|  | [optional]
 **bankAccountNo** | **String**|  | [optional]
 **receiveType** | **String**|  | [optional]
 **triggerTime** | **String**|  | [optional]
 **remainAmount** | **BigDecimal**|  | [optional]
 **remark** | **String**|  | [optional]
 **notifyAddress** | **String**|  | [optional]

### Return type
[**AutoWithdrawRuleSetYopAutoWithdrawRuleSetResponseDTOResult**](../model/AutoWithdrawRuleSetYopAutoWithdrawRuleSetResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="balanceQuery"></a>
# **balanceQuery**
BalanceQueryResponse balanceQuery(BalanceQueryRequest request)

资金账户余额查询

查询商户余额

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//BalanceQueryRequest中的参数说明参见Parameters章节
BalanceQueryRequest request = new BalanceQueryRequest();
request.setMerchantNo("10080006026");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BalanceQueryResponse response = api.balanceQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#balanceQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |

### Return type
[**BalanceQueryAccountInfoRespDTOResult**](../model/BalanceQueryAccountInfoRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankPaymentOrder"></a>
# **bankPaymentOrder**
BankPaymentOrderResponse bankPaymentOrder(BankPaymentOrderRequest request)

银行账户支付

提供银行账户支付服务

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//BankPaymentOrderRequest中的参数说明参见Parameters章节
BankPaymentOrderRequest request = new BankPaymentOrderRequest();
request.setBody(new BankPaymentOrderBankAccountPaymentRequestDtoParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankPaymentOrderResponse response = api.bankPaymentOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#bankPaymentOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**BankPaymentOrderBankAccountPaymentRequestDtoParam**](../model/BankPaymentOrderBankAccountPaymentRequestDtoParam.md)|  |

### Return type
[**BankPaymentOrderBankAccountPaymentRespDtoResult**](../model/BankPaymentOrderBankAccountPaymentRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="enterpriseAccountBookPayOrder"></a>
# **enterpriseAccountBookPayOrder**
EnterpriseAccountBookPayOrderResponse enterpriseAccountBookPayOrder(EnterpriseAccountBookPayOrderRequest request)

记账薄支付

记账薄支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseAccountBookPayOrderRequest中的参数说明参见Parameters章节
EnterpriseAccountBookPayOrderRequest request = new EnterpriseAccountBookPayOrderRequest();
request.setBody(new EnterpriseAccountBookPayOrderAccountBookPaymentRequestDtoParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseAccountBookPayOrderResponse response = api.enterpriseAccountBookPayOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseAccountBookPayOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**EnterpriseAccountBookPayOrderAccountBookPaymentRequestDtoParam**](../model/EnterpriseAccountBookPayOrderAccountBookPaymentRequestDtoParam.md)|  |

### Return type
[**EnterpriseAccountBookPayOrderAccountBookPaymentRespDtoResult**](../model/EnterpriseAccountBookPayOrderAccountBookPaymentRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="enterpriseAccountPayOrder"></a>
# **enterpriseAccountPayOrder**
EnterpriseAccountPayOrderResponse enterpriseAccountPayOrder(EnterpriseAccountPayOrderRequest request)

企业账户支付-下单

企业账户支付提供商户支付给其他商家的能力，主要解决收单场景中商户余额付款需求，如购买机票等

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseAccountPayOrderRequest中的参数说明参见Parameters章节
EnterpriseAccountPayOrderRequest request = new EnterpriseAccountPayOrderRequest();
request.setBody(new EnterpriseAccountPayOrderAccountPaymentRequestDtoParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseAccountPayOrderResponse response = api.enterpriseAccountPayOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseAccountPayOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**EnterpriseAccountPayOrderAccountPaymentRequestDtoParam**](../model/EnterpriseAccountPayOrderAccountPaymentRequestDtoParam.md)|  |

### Return type
[**EnterpriseAccountPayOrderAccountPaymentRespDtoResult**](../model/EnterpriseAccountPayOrderAccountPaymentRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="enterpriseAutoPaymentOrder"></a>
# **enterpriseAutoPaymentOrder**
EnterpriseAutoPaymentOrderResponse enterpriseAutoPaymentOrder(EnterpriseAutoPaymentOrderRequest request)

企业账户支付-自动付款

付款方主动发起的付款请求

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseAutoPaymentOrderRequest中的参数说明参见Parameters章节
EnterpriseAutoPaymentOrderRequest request = new EnterpriseAutoPaymentOrderRequest();
request.setMerchantNo("10014242006");
request.setOrderId("merchant12345");
request.setOrderAmount(new BigDecimal("0"));
request.setFundProcessType("fundProcessType_example");
request.setGoodsName("旺仔牛奶");
request.setExpiredTime("2021-05-12 13:23:45");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("memo_example");
request.setPayerNotifyUrl("payerNotifyUrl_example");
request.setCsUrl("csUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseAutoPaymentOrderResponse response = api.enterpriseAutoPaymentOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseAutoPaymentOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **payerNotifyUrl** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]

### Return type
[**EnterpriseAutoPaymentOrderAutoPaymentRespDtoResult**](../model/EnterpriseAutoPaymentOrderAutoPaymentRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="enterpriseAutoPaymentQuery"></a>
# **enterpriseAutoPaymentQuery**
EnterpriseAutoPaymentQueryResponse enterpriseAutoPaymentQuery(EnterpriseAutoPaymentQueryRequest request)

企业账户支付-自动付款订单查询

查询自动付款订单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseAutoPaymentQueryRequest中的参数说明参见Parameters章节
EnterpriseAutoPaymentQueryRequest request = new EnterpriseAutoPaymentQueryRequest();
request.setMerchantNo("10014242004");
request.setOrderId("merchant12345");
request.setOrderDate("orderDate_example");
request.setUniqueOrderNo("uniqueOrderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseAutoPaymentQueryResponse response = api.enterpriseAutoPaymentQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseAutoPaymentQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **orderId** | **String**| 商户系统内部生成的订单号&lt;br&gt;如填写易宝内部订单号则可以不填，否则必填 | [optional]
 **orderDate** | **String**| 订单日期&lt;br&gt;如填写易宝内部订单号则可以不填，否则必填 | [optional]
 **uniqueOrderNo** | **String**| 易宝内部订单号&lt;br&gt;如填写此项，订单号及订单日期可以不填。如同时填写将以易宝内部订单号为准 | [optional]

### Return type
[**EnterpriseAutoPaymentQueryAutoPaymentQueryRespDtoResult**](../model/EnterpriseAutoPaymentQueryAutoPaymentQueryRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="enterpriseTokenPayOrder"></a>
# **enterpriseTokenPayOrder**
EnterpriseTokenPayOrderResponse enterpriseTokenPayOrder(EnterpriseTokenPayOrderRequest request)

企业账户支付-token支付

企业账户支付-token支付

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseTokenPayOrderRequest中的参数说明参见Parameters章节
EnterpriseTokenPayOrderRequest request = new EnterpriseTokenPayOrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setToken("token_example");
request.setPayerMerchantNo("payerMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseTokenPayOrderResponse response = api.enterpriseTokenPayOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseTokenPayOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **token** | **String**|  | [optional]
 **payerMerchantNo** | **String**|  | [optional]

### Return type
[**EnterpriseTokenPayOrderTokenPaymentResponseDtoResult**](../model/EnterpriseTokenPayOrderTokenPaymentResponseDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="enterpriseWithholdingOrder"></a>
# **enterpriseWithholdingOrder**
EnterpriseWithholdingOrderResponse enterpriseWithholdingOrder(EnterpriseWithholdingOrderRequest request)

企业账户支付-关系扣款

企业账户支付-关系扣款

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//EnterpriseWithholdingOrderRequest中的参数说明参见Parameters章节
EnterpriseWithholdingOrderRequest request = new EnterpriseWithholdingOrderRequest();
request.setParentMerchantNo("10012426723");
request.setMerchantNo("10014242004");
request.setPayerMerchantNo("10014242005");
request.setOrderId("merchant12345");
request.setOrderAmount(new BigDecimal("0"));
request.setFundProcessType("fundProcessType_example");
request.setGoodsName("旺仔牛奶");
request.setExpiredTime("2017-12-12 13:23:45");
request.setNotifyUrl("notifyUrl_example");
request.setMemo("费用");
request.setPayerNotifyUrl("payerNotifyUrl_example");
request.setCsUrl("csUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    EnterpriseWithholdingOrderResponse response = api.enterpriseWithholdingOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#enterpriseWithholdingOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **payerMerchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **payerNotifyUrl** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]

### Return type
[**EnterpriseWithholdingOrderWithholdingPaymentRespDtoResult**](../model/EnterpriseWithholdingOrderWithholdingPaymentRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="externalOrder"></a>
# **externalOrder**
ExternalOrderResponse externalOrder(ExternalOrderRequest request)

银行账户支付-外部订单同步

用于报送非易宝订单信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//ExternalOrderRequest中的参数说明参见Parameters章节
ExternalOrderRequest request = new ExternalOrderRequest();
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setChannelName("channelName_example");
request.setOrderId("orderId_example");
request.setMerchantName("merchantName_example");
request.setGoodsName("goodsName_example");
request.setTrxDate("trxDate_example");
request.setFinishDate("finishDate_example");
request.setOrderAmount(new BigDecimal("0"));
request.setRealAmount(new BigDecimal("0"));
request.setPayerUserId("payerUserId_example");
request.setPayWay("payWay_example");
request.setPayCardNo("payCardNo_example");
request.setPayCardType("payCardType_example");
request.setUserRequestIp("userRequestIp_example");
request.setTrxType("trxType_example");
request.setBatchNo("batchNo_example");
request.setChannelExtInfo("{   \"channelMerchantInfos\": [     {       \"channelMrchantName\": \"商户名称\",       \"channelMrchantNo\": \"10020320020\"     },     {       \"channelMrchantName\": \"商户名称2\",       \"channelMrchantNo\": \"10020320021\"     }   ] }");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ExternalOrderResponse response = api.externalOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#externalOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **channelName** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **merchantName** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **trxDate** | **String**|  | [optional]
 **finishDate** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **realAmount** | **BigDecimal**|  | [optional]
 **payerUserId** | **String**|  | [optional]
 **payWay** | **String**|  | [optional]
 **payCardNo** | **String**|  | [optional]
 **payCardType** | **String**|  | [optional]
 **userRequestIp** | **String**|  | [optional]
 **trxType** | **String**|  | [optional]
 **batchNo** | **String**|  | [optional]
 **channelExtInfo** | **String**|  | [optional]

### Return type
[**ExternalOrderExternalOrderSubmitOrderRespDtoResult**](../model/ExternalOrderExternalOrderSubmitOrderRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="payBatchOrder"></a>
# **payBatchOrder**
PayBatchOrderResponse payBatchOrder(PayBatchOrderRequest request)

付款-批量下单

为了保证出款成功，各农信社卡或账号16位以下的农业银行卡，建议或尽可能填写支行编码； &lt;/br&gt;有报错信息并不代表未受理，具体是否受理参看batchAcceptDetailList中受理明细

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PayBatchOrderRequest中的参数说明参见Parameters章节
PayBatchOrderRequest request = new PayBatchOrderRequest();
request.setBody(new PayBatchOrderBatchRemitReqDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayBatchOrderResponse response = api.payBatchOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#payBatchOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PayBatchOrderBatchRemitReqDTOParam**](../model/PayBatchOrderBatchRemitReqDTOParam.md)|  |

### Return type
[**PayBatchOrderBatchRemitRespDTOResult**](../model/PayBatchOrderBatchRemitRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="payBatchQuery"></a>
# **payBatchQuery**
PayBatchQueryResponse payBatchQuery(PayBatchQueryRequest request)

付款-批次查询

付款-批次查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PayBatchQueryRequest中的参数说明参见Parameters章节
PayBatchQueryRequest request = new PayBatchQueryRequest();
request.setBatchNo("batchNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayBatchQueryResponse response = api.payBatchQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#payBatchQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchNo** | **String**| 批次号,需要查询的批次号 |

### Return type
[**PayBatchQueryBatchRemitQueryRespDTOResult**](../model/PayBatchQueryBatchRemitQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="payCancel"></a>
# **payCancel**
PayCancelResponse payCancel(PayCancelRequest request)

付款-撤销

撤销预约付款请求

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PayCancelRequest中的参数说明参见Parameters章节
PayCancelRequest request = new PayCancelRequest();
request.setParentMerchantNo("100400612345");
request.setOrderNo("20200720110033a171b64e");
request.setCancelReason("业务需要撤销此次付款");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayCancelResponse response = api.payCancel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#payCancel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **orderNo** | **String**|  | [optional]
 **cancelReason** | **String**|  | [optional]

### Return type
[**PayCancelRemitCancelRespDTOResult**](../model/PayCancelRemitCancelRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="payOrder"></a>
# **payOrder**
PayOrderResponse payOrder(PayOrderRequest request)

付款-下单

为了保证出款成功，各农信社卡或账号16位以下的农业银行卡，建议或尽可能填写支行编码；

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PayOrderRequest中的参数说明参见Parameters章节
PayOrderRequest request = new PayOrderRequest();
request.setParentMerchantNo("100400612345");
request.setMerchantNo("100400612345");
request.setRequestNo("PAY2133213124");
request.setOrderAmount(new BigDecimal("0"));
request.setFeeChargeSide("当商户承担且计费方式为预付实扣或后收时，不支持收款方承担；当平台商或服务商承担时无需指定此手续费承担方；");
request.setReceiveType("REAL_TIME");
request.setReceiverAccountNo("6212260200062388891");
request.setReceiverAccountName("receiverAccountName_example");
request.setReceiverBankCode("ICBC");
request.setBankAccountType("DEBIT_CARD");
request.setBranchBankCode("branchBankCode_example");
request.setComments("xx平台付款");
request.setTerminalType("PC");
request.setNotifyUrl("http://www.baidu.com");
request.setRemark("remark_example");
request.setReceiptComments("receiptComments_example");
request.setRiskInfo("riskInfo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayOrderResponse response = api.payOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#payOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **receiveType** | **String**|  | [optional]
 **receiverAccountNo** | **String**|  | [optional]
 **receiverAccountName** | **String**|  | [optional]
 **receiverBankCode** | **String**|  | [optional]
 **bankAccountType** | **String**|  | [optional]
 **branchBankCode** | **String**|  | [optional]
 **comments** | **String**|  | [optional]
 **terminalType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **receiptComments** | **String**|  | [optional]
 **riskInfo** | **String**|  | [optional]

### Return type
[**PayOrderRemitRespDTOResult**](../model/PayOrderRemitRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="payQuery"></a>
# **payQuery**
PayQueryResponse payQuery(PayQueryRequest request)

付款-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PayQueryRequest中的参数说明参见Parameters章节
PayQueryRequest request = new PayQueryRequest();
request.setParentMerchantNo("100400612345");
request.setRequestNo("REMIT20200327103027");
request.setOrderNo("8af60c56b35b42d3a7e985fe55a6c54c");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PayQueryResponse response = api.payQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#payQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号）&lt;!--5f39ae17-8c62-4a45-bc43-b32064c9388a:W3siYmxvY2tJZCI6IjM4NzAtMTU5ODQwOTgyNDQ4MCIsImJsb2NrVHlwZSI6InBhcmFncmFwaCIsInN0eWxlcyI6eyJhbGlnbiI6ImxlZnQiLCJpbmRlbnQiOjAsInRleHQtaW5kZW50IjowLCJsaW5lLWhlaWdodCI6MS43NSwiYmFjay1jb2xvciI6IiIsInBhZGRpbmciOiIifSwidHlwZSI6InBhcmFncmFwaCIsInJpY2hUZXh0Ijp7ImRhdGEiOlt7ImNoYXIiOiLmoIcifSx7ImNoYXIiOiLlh4YifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLmiLcifSx7ImNoYXIiOiLmlLYifSx7ImNoYXIiOiLku5gifSx7ImNoYXIiOiLmrL4ifSx7ImNoYXIiOiLmlrkifSx7ImNoYXIiOiLmoYgifSx7ImNoYXIiOiLkuK0ifSx7ImNoYXIiOiLmraQifSx7ImNoYXIiOiLlj4IifSx7ImNoYXIiOiLmlbAifSx7ImNoYXIiOiLkuI4ifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLnvJYifSx7ImNoYXIiOiLkuIAifSx7ImNoYXIiOiLoh7QifSx7ImNoYXIiOiLvvIwifSx7ImNoYXIiOiLlubMifSx7ImNoYXIiOiLlj7AifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLmiLcifSx7ImNoYXIiOiLmlLYifSx7ImNoYXIiOiLku5gifSx7ImNoYXIiOiLmrL4ifSx7ImNoYXIiOiLmlrkifSx7ImNoYXIiOiLmoYgifSx7ImNoYXIiOiLkuK0ifSx7ImNoYXIiOiLmraQifSx7ImNoYXIiOiLlj4IifSx7ImNoYXIiOiLmlbAifSx7ImNoYXIiOiLkuLoifSx7ImNoYXIiOiLlubMifSx7ImNoYXIiOiLlj7AifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLmiLcifSx7ImNoYXIiOiLnvJYifSx7ImNoYXIiOiLlj7cifV0sImlzUmljaFRleHQiOnRydWUsImtlZXBMaW5lQnJlYWsiOnRydWV9fV0&#x3D;--&gt;&lt;!--5f39ae17-8c62-4a45-bc43-b32064c9388a:W3siYmxvY2tJZCI6IjI3MTEtMTU5ODQwOTgyNDE3NSIsImJsb2NrVHlwZSI6InBhcmFncmFwaCIsInN0eWxlcyI6eyJhbGlnbiI6ImxlZnQiLCJpbmRlbnQiOjAsInRleHQtaW5kZW50IjowLCJsaW5lLWhlaWdodCI6MS43NSwiYmFjay1jb2xvciI6IiIsInBhZGRpbmciOiIifSwidHlwZSI6InBhcmFncmFwaCIsInJpY2hUZXh0Ijp7ImRhdGEiOlt7ImNoYXIiOiLlj5EifSx7ImNoYXIiOiLotbcifSx7ImNoYXIiOiLmlrkifSx7ImNoYXIiOiLllYYifSx7ImNoYXIiOiLmiLcifSx7ImNoYXIiOiLnvJYifSx7ImNoYXIiOiLlj7cifV0sImlzUmljaFRleHQiOnRydWUsImtlZXBMaW5lQnJlYWsiOnRydWV9fV0&#x3D;--&gt; |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成（与易宝付款订单号两者填其一） | [optional]
 **orderNo** | **String**| 易宝订单号&lt;br&gt;易宝支付系统生成的付款订单号（与商户请求号两者填其一） | [optional]

### Return type
[**PayQueryRemitOrderQueryRespDTOResult**](../model/PayQueryRemitOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="paySystemQuery"></a>
# **paySystemQuery**
PaySystemQueryResponse paySystemQuery(PaySystemQueryRequest request)

付款-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//PaySystemQueryRequest中的参数说明参见Parameters章节
PaySystemQueryRequest request = new PaySystemQueryRequest();
request.setMerchantNo("易宝支付分配的的商户唯一标识;示例值:100400612345");
request.setRequestNo("REMIT20200327103027");
request.setOrderNo("8af60c56b35b42d3a7e985fe55a6c54c");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PaySystemQueryResponse response = api.paySystemQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#paySystemQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成（与易宝付款订单号两者填其一） | [optional]
 **orderNo** | **String**| 易宝订单号&lt;br&gt;易宝支付系统生成的付款订单号（与商户请求号两者填其一） | [optional]

### Return type
[**PaySystemQueryRemitOrderQueryRespDTOResult**](../model/PaySystemQueryRemitOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="receiptGather"></a>
# **receiptGather**
ReceiptGatherResponse receiptGather(ReceiptGatherRequest request)

获取资金汇总凭证

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//ReceiptGatherRequest中的参数说明参见Parameters章节
ReceiptGatherRequest request = new ReceiptGatherRequest();
request.setMerchantNo("merchantNo_example");
request.setRemark("remark_example");
request.setCounterpartyNo("counterpartyNo_example");
request.setOrderNos("orderNos_example");
request.setBizDate("bizDate_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ReceiptGatherResponse response = api.receiptGather(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#receiptGather, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **counterpartyNo** | **String**|  | [optional]
 **orderNos** | **String**|  | [optional]
 **bizDate** | **String**|  | [optional]

### Return type
[**ReceiptGatherBatchReceiptRespDTOResult**](../model/ReceiptGatherBatchReceiptRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="receiptGet"></a>
# **receiptGet**
ReceiptGetResponse receiptGet(ReceiptGetRequest request)

电子回单-下载

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//ReceiptGetRequest中的参数说明参见Parameters章节
ReceiptGetRequest request = new ReceiptGetRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setTradeType("tradeType_example");
request.setOrderNo("示例值：8af60c56b35b42d3a7e985fe55a6c54c");
request.setRequestNo("示例值：REMIT20200327103027");
request.setOrderDate("orderDate_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    ReceiptGetResponse response = api.receiptGet(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#receiptGet, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **tradeType** | **String**| 可选项如下:&lt;br&gt;TRANSFER:企业账户转账&lt;br&gt;PAY:企业付款&lt;br&gt;RECHARGE:企业账户充值&lt;br&gt;WITHDRAW:企业账户提现&lt;br&gt;ADVANCE:记账薄收款 |
 **orderNo** | **String**| 易宝支付系统生成的付款订单号（与商户请求号两者填其一） | [optional]
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成（与易宝付款订单号两者填其一） | [optional]
 **orderDate** | **String**| 如果传了商户请求号requestNo，orderDate也是必填的，格式 yyyy-MM/yyyy-MM-dd | [optional]
 **merchantNo** | **String**| 商户编号，易宝支付分配的的商户唯一标识，如果传了商户请求号requestNo，那么merchantNo也是必填的。 | [optional]

### Return type
[**ReceiptGetReceiptRespDTOResult**](../model/ReceiptGetReceiptRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="recharge"></a>
# **recharge**
RechargeResponse recharge(RechargeRequest request)

充值-下单（多种支付）

提供商户资金进入易宝商户账户的能力，充值方式支持企业网银和个人网银、银行汇款、银行扣款等

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeRequest中的参数说明参见Parameters章节
RechargeRequest request = new RechargeRequest();
request.setBody(new RechargeRechargeApiV2RequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeResponse response = api.recharge(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#recharge, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**RechargeRechargeApiV2RequestDTOParam**](../model/RechargeRechargeApiV2RequestDTOParam.md)|  |

### Return type
[**RechargeRechargeApiV2ResponseDTOResult**](../model/RechargeRechargeApiV2ResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="rechargeAccountBookQuery"></a>
# **rechargeAccountBookQuery**
RechargeAccountBookQueryResponse rechargeAccountBookQuery(RechargeAccountBookQueryRequest request)

批量查询记账簿来账流水

通过此接口可批量查询记账簿来账流水

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeAccountBookQueryRequest中的参数说明参见Parameters章节
RechargeAccountBookQueryRequest request = new RechargeAccountBookQueryRequest();
request.setYpAccountBookNo("ypAccountBookNo_example");
request.setQueryStartDate("2022-01-01 00:00:00");
request.setQueryEndDate("2022-01-02 23:59:59");
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setPageNo(56);
request.setPageSize(56);

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeAccountBookQueryResponse response = api.rechargeAccountBookQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#rechargeAccountBookQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ypAccountBookNo** | **String**| 易宝记账簿编号 |
 **queryStartDate** | **String**| 查询时间范围-开始日期 格式:yyyy-MM-dd HH:mm:ss&lt;br&gt;与结束时间间隔不能超过2天 |
 **queryEndDate** | **String**| 查询时间范围-结束时间 格式:yyyy-MM-dd HH:mm:ss&lt;br&gt;与开始时间间隔不能超过2天 |
 **merchantNo** | **String**| 收款商户编号 |
 **parentMerchantNo** | **String**| 标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号 |
 **pageNo** | **Integer**| 页码,从1开始,默认为1 | [optional]
 **pageSize** | **Integer**| 页大小,默认30 | [optional]

### Return type
[**RechargeAccountBookQueryRechargePageQueryResponseDTOResult**](../model/RechargeAccountBookQueryRechargePageQueryResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeBatchQuery"></a>
# **rechargeBatchQuery**
RechargeBatchQueryResponse rechargeBatchQuery(RechargeBatchQueryRequest request)

充值订单批量查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeBatchQueryRequest中的参数说明参见Parameters章节
RechargeBatchQueryRequest request = new RechargeBatchQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setQueryStartDate("queryStartDate_example");
request.setQueryEndDate("queryEndDate_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeBatchQueryResponse response = api.rechargeBatchQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#rechargeBatchQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） | [optional]
 **merchantNo** | **String**|  | [optional]
 **queryStartDate** | **String**| 查询开始时间&lt;br&gt;（支持获取最长周期为30天的充值记录,&lt;br&gt;支持yyyy-MM-dd格式，示例：2021-09-17 即2021-09-17 00:00:00开始） | [optional]
 **queryEndDate** | **String**| 查询结束时间&lt;br&gt;（支持获取最长周期为30天的充值记录，&lt;br&gt;支持yyyy-MM-dd格式，示例：2021-09-17 即2021-09-17 23:59:59结束) | [optional]

### Return type
[**RechargeBatchQueryRechargeQueryMultiApiRespDTOResult**](../model/RechargeBatchQueryRechargeQueryMultiApiRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeOnlinebankOrder"></a>
# **rechargeOnlinebankOrder**
RechargeOnlinebankOrderResponse rechargeOnlinebankOrder(RechargeOnlinebankOrderRequest request)

充值-网银下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeOnlinebankOrderRequest中的参数说明参见Parameters章节
RechargeOnlinebankOrderRequest request = new RechargeOnlinebankOrderRequest();
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setRequestNo("requestNo_example");
request.setAmount(new BigDecimal("0"));
request.setPayType("payType_example");
request.setBankCode("bankCode_example");
request.setNotifyUrl("notifyUrl_example");
request.setRemark("remark_example");
request.setReturnUrl("returnUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeOnlinebankOrderResponse response = api.rechargeOnlinebankOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#rechargeOnlinebankOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **payType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]

### Return type
[**RechargeOnlinebankOrderOnlineBankRechargeApiRespDTOResult**](../model/RechargeOnlinebankOrderOnlineBankRechargeApiRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeOrder"></a>
# **rechargeOrder**
RechargeOrderResponse rechargeOrder(RechargeOrderRequest request)

充值-银行汇款下单

发起充值

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeOrderRequest中的参数说明参见Parameters章节
RechargeOrderRequest request = new RechargeOrderRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("100400612345");
request.setRequestNo("requestNo_example");
request.setAmount(new BigDecimal("0"));
request.setRemark("remark_example");
request.setPayType("payType_example");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeOrderResponse response = api.rechargeOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#rechargeOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **remark** | **String**|  | [optional]
 **payType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**RechargeOrderRechargeApiRespDTOResult**](../model/RechargeOrderRechargeApiRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeQuery"></a>
# **rechargeQuery**
RechargeQueryResponse rechargeQuery(RechargeQueryRequest request)

充值-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//RechargeQueryRequest中的参数说明参见Parameters章节
RechargeQueryRequest request = new RechargeQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderNo("orderNo_example");
request.setRequestNo("requestNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeQueryResponse response = api.rechargeQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#rechargeQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**|  |
 **orderNo** | **String**| 充值订单号&lt;br&gt;充值订单号和商户请求号不能同时为空 | [optional]
 **requestNo** | **String**| 商户请求号&lt;br&gt;充值订单号和商户请求号不能同时为空 | [optional]

### Return type
[**RechargeQueryRechargeQueryApiRespDTOResult**](../model/RechargeQueryRechargeQueryApiRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="setWithdrawRule"></a>
# **setWithdrawRule**
SetWithdrawRuleResponse setWithdrawRule(SetWithdrawRuleRequest request)

设置提现规则

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//SetWithdrawRuleRequest中的参数说明参见Parameters章节
SetWithdrawRuleRequest request = new SetWithdrawRuleRequest();
request.setFromMerchantNo("fromMerchantNo_example");
request.setTomerchantNo("tomerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SetWithdrawRuleResponse response = api.setWithdrawRule(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#setWithdrawRule, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fromMerchantNo** | **String**|  | [optional]
 **tomerchantNo** | **String**|  | [optional]

### Return type
[**SetWithdrawRuleWithdrawRuleRespDTOResult**](../model/SetWithdrawRuleWithdrawRuleRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="supplierApply"></a>
# **supplierApply**
SupplierApplyResponse supplierApply(SupplierApplyRequest request)

付款到供应商--申请添加供应商

付款到供应商--申请添加供应商

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//SupplierApplyRequest中的参数说明参见Parameters章节
SupplierApplyRequest request = new SupplierApplyRequest();
request.setBody(new SupplierApplyApplySupplierRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SupplierApplyResponse response = api.supplierApply(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#supplierApply, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SupplierApplyApplySupplierRequestDTOParam**](../model/SupplierApplyApplySupplierRequestDTOParam.md)|  |

### Return type
[**SupplierApplyApplySupplierRespDTOResult**](../model/SupplierApplyApplySupplierRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="supplierPayOrder"></a>
# **supplierPayOrder**
SupplierPayOrderResponse supplierPayOrder(SupplierPayOrderRequest request)

付款到供应商-下单

付款到供应商-下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//SupplierPayOrderRequest中的参数说明参见Parameters章节
SupplierPayOrderRequest request = new SupplierPayOrderRequest();
request.setParentMerchantNo("100400612345");
request.setMerchantNo("100400612345");
request.setRequestNo("requestNo111");
request.setOrderAmount(new BigDecimal("0"));
request.setReceiverAccountNo("6212260200062388891");
request.setSupplierId(17L);
request.setReceiverBankCode("ICBC");
request.setBankAccountType("DEBIT_CARD");
request.setComments("xx平台付款");
request.setFeeChargeSide("PAYER");
request.setTerminalType("PC");
request.setReceiveType("REAL_TIME");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SupplierPayOrderResponse response = api.supplierPayOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#supplierPayOrder, ex:", e);
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
 **supplierId** | **Long**|  | [optional]
 **receiverBankCode** | **String**|  | [optional]
 **bankAccountType** | **String**|  | [optional]
 **comments** | **String**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **terminalType** | **String**|  | [optional]
 **receiveType** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**SupplierPayOrderRemitRespDTOResult**](../model/SupplierPayOrderRemitRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="supplierQuery"></a>
# **supplierQuery**
SupplierQueryResponse supplierQuery(SupplierQueryRequest request)

付款到供应商--查询已添加的供应商

付款到供应商--查询已添加的供应商

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//SupplierQueryRequest中的参数说明参见Parameters章节
SupplierQueryRequest request = new SupplierQueryRequest();
request.setMerchantNo("10080011111");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SupplierQueryResponse response = api.supplierQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#supplierQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |

### Return type
[**SupplierQueryQuerySupplierRespDTOResult**](../model/SupplierQueryQuerySupplierRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="supplierQueryProgress"></a>
# **supplierQueryProgress**
SupplierQueryProgressResponse supplierQueryProgress(SupplierQueryProgressRequest request)

付款到供应商--查询申请进度

付款到供应商--查询申请进度

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//SupplierQueryProgressRequest中的参数说明参见Parameters章节
SupplierQueryProgressRequest request = new SupplierQueryProgressRequest();
request.setRequestNo("requestNo1111");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SupplierQueryProgressResponse response = api.supplierQueryProgress(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#supplierQueryProgress, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |

### Return type
[**SupplierQueryProgressApplySupplierProgressRespDTOResult**](../model/SupplierQueryProgressApplySupplierProgressRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferB2bOrder"></a>
# **transferB2bOrder**
TransferB2bOrderResponse transferB2bOrder(TransferB2bOrderRequest request)

转账-下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//TransferB2bOrderRequest中的参数说明参见Parameters章节
TransferB2bOrderRequest request = new TransferB2bOrderRequest();
request.setParentMerchantNo("100400612345");
request.setRequestNo("商户请求号，由商户自定义生成;示例值：TRANS2133213124");
request.setFromMerchantNo("易宝支付分配的的商户唯一标识;示例值:100400612345");
request.setToMerchantNo("易宝支付分配的的商户唯一标识;示例值:100400612346");
request.setToAccountType("默认FUND_ACCOUNT");
request.setOrderAmount("单位：元（RMB），精确到分;示例值：0.01 元");
request.setUsage("usage_example");
request.setFeeChargeSide("当商户承担且计费方式为预付实扣或后收时，不支持转入方承担；当平台商或服务商承担时无需指定此手续费承担方；");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferB2bOrderResponse response = api.transferB2bOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#transferB2bOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **fromMerchantNo** | **String**|  | [optional]
 **toMerchantNo** | **String**|  | [optional]
 **toAccountType** | **String**|  | [optional]
 **orderAmount** | **String**|  | [optional]
 **usage** | **String**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**TransferB2bOrderMgTransferOrderRespDTOResult**](../model/TransferB2bOrderMgTransferOrderRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferB2bQuery"></a>
# **transferB2bQuery**
TransferB2bQueryResponse transferB2bQuery(TransferB2bQueryRequest request)

转账-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//TransferB2bQueryRequest中的参数说明参见Parameters章节
TransferB2bQueryRequest request = new TransferB2bQueryRequest();
request.setParentMerchantNo("100400612345");
request.setRequestNo("商户请求号，由商户自定义生成 ;示例值：TRANS2133213124");
request.setOrderNo("orderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferB2bQueryResponse response = api.transferB2bQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#transferB2bQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成(与易宝转账订单号两者填其一) | [optional]
 **orderNo** | **String**| 易宝转账订单号&lt;br&gt;易宝支付系统生成的转账订单号(与商户请求号两者填其一) | [optional]

### Return type
[**TransferB2bQueryMgTransferOrderQueryRespDTOResult**](../model/TransferB2bQueryMgTransferOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferSystemQuery"></a>
# **transferSystemQuery**
TransferSystemQueryResponse transferSystemQuery(TransferSystemQueryRequest request)

转账-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//TransferSystemQueryRequest中的参数说明参见Parameters章节
TransferSystemQueryRequest request = new TransferSystemQueryRequest();
request.setMerchantNo("易宝支付分配的的商户唯一标识;示例值:100400612345");
request.setRequestNo("商户请求号，由商户自定义生成 ;示例值：TRANS2133213124");
request.setOrderNo("orderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferSystemQueryResponse response = api.transferSystemQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#transferSystemQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成(与易宝转账订单号两者填其一) | [optional]
 **orderNo** | **String**| 易宝转账订单号&lt;br&gt;易宝支付系统生成的转账订单号(与商户请求号两者填其一) | [optional]

### Return type
[**TransferSystemQueryMgTransferOrderQueryRespDTOResult**](../model/TransferSystemQueryMgTransferOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferWechatOrder"></a>
# **transferWechatOrder**
TransferWechatOrderResponse transferWechatOrder(TransferWechatOrderRequest request)

转账到微信零钱-下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//TransferWechatOrderRequest中的参数说明参见Parameters章节
TransferWechatOrderRequest request = new TransferWechatOrderRequest();
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setAmount(new BigDecimal("0"));
request.setAppId("appId_example");
request.setScene("scene_example");
request.setOpenId("openId_example");
request.setUserName("userName_example");
request.setRemark("remark_example");
request.setNotifyUrl("notifyUrl_example");
request.setParentMerchantNo("parentMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferWechatOrderResponse response = api.transferWechatOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#transferWechatOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **amount** | **BigDecimal**|  | [optional]
 **appId** | **String**|  | [optional]
 **scene** | **String**|  | [optional]
 **openId** | **String**|  | [optional]
 **userName** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**TransferWechatOrderWechatTransferRespDTOResult**](../model/TransferWechatOrderWechatTransferRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferWechatQuery"></a>
# **transferWechatQuery**
TransferWechatQueryResponse transferWechatQuery(TransferWechatQueryRequest request)

转账到微信零钱-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//TransferWechatQueryRequest中的参数说明参见Parameters章节
TransferWechatQueryRequest request = new TransferWechatQueryRequest();
request.setMerchantNo("merchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setRequestNo("requestNo_example");
request.setOrderNo("orderNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferWechatQueryResponse response = api.transferWechatQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#transferWechatQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **requestNo** | **String**| 商户请求号&lt;br&gt;由商户自定义生成 | [optional]
 **orderNo** | **String**| 易宝转账订单号&lt;br&gt;易宝支付系统生成的转账订单号（跟商户请求号二选一） | [optional]

### Return type
[**TransferWechatQueryQueryWechatTransferRespDTOResult**](../model/TransferWechatQueryQueryWechatTransferRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawCardBind"></a>
# **withdrawCardBind**
WithdrawCardBindResponse withdrawCardBind(WithdrawCardBindRequest request)

提现卡-添加

为了保证出款成功，各农信社卡或账号16位以下的农业银行卡，建议或尽可能填写支行编码；

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawCardBindRequest中的参数说明参见Parameters章节
WithdrawCardBindRequest request = new WithdrawCardBindRequest();
request.setMerchantNo("100400612345");
request.setBankCardType("bankCardType_example");
request.setAccountNo("accountNo_example");
request.setBankCode("当bankCardType为ENTERPRISE_ACCOUNT时必填；  示例值：ICBC");
request.setBranchCode("102100000048");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawCardBindResponse response = api.withdrawCardBind(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawCardBind, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **bankCardType** | **String**|  | [optional]
 **accountNo** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **branchCode** | **String**|  | [optional]

### Return type
[**WithdrawCardBindBindCardRespDTOResult**](../model/WithdrawCardBindBindCardRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawCardModify"></a>
# **withdrawCardModify**
WithdrawCardModifyResponse withdrawCardModify(WithdrawCardModifyRequest request)

提现卡-修改/注销

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawCardModifyRequest中的参数说明参见Parameters章节
WithdrawCardModifyRequest request = new WithdrawCardModifyRequest();
request.setMerchantNo("merchantNo_example");
request.setAccountNo("accountNo_example");
request.setBindId(789L);
request.setBankCardOperateType("bankCardOperateType_example");
request.setBankCode("ICBC");
request.setBranchCode("102100000048");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawCardModifyResponse response = api.withdrawCardModify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawCardModify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **accountNo** | **String**|  | [optional]
 **bindId** | **Long**|  | [optional]
 **bankCardOperateType** | **String**|  | [optional]
 **bankCode** | **String**|  | [optional]
 **branchCode** | **String**|  | [optional]

### Return type
[**WithdrawCardModifyModifyBindCardRespDTOResult**](../model/WithdrawCardModifyModifyBindCardRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawCardQuery"></a>
# **withdrawCardQuery**
WithdrawCardQueryResponse withdrawCardQuery(WithdrawCardQueryRequest request)

提现卡查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawCardQueryRequest中的参数说明参见Parameters章节
WithdrawCardQueryRequest request = new WithdrawCardQueryRequest();
request.setMerchantNo("易宝支付分配的的商户唯一标识  示例值:100400612345");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawCardQueryResponse response = api.withdrawCardQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawCardQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |

### Return type
[**WithdrawCardQueryBindCardQueryRespDTOResult**](../model/WithdrawCardQueryBindCardQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawOrder"></a>
# **withdrawOrder**
WithdrawOrderResponse withdrawOrder(WithdrawOrderRequest request)

提现-下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawOrderRequest中的参数说明参见Parameters章节
WithdrawOrderRequest request = new WithdrawOrderRequest();
request.setParentMerchantNo("100400612345");
request.setRequestNo("WITHDRAW20200327103027");
request.setMerchantNo("100400612345");
request.setBankCardId("11103");
request.setBankAccountNo("6212260200019388841");
request.setReceiveType("REAL_TIME");
request.setOrderAmount(new BigDecimal("0"));
request.setNotifyUrl("www.baidu.com");
request.setRemark("XXX平台提现");
request.setTerminalType("PC");
request.setFeeDeductType("feeDeductType_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawOrderResponse response = api.withdrawOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **bankCardId** | **String**|  | [optional]
 **bankAccountNo** | **String**|  | [optional]
 **receiveType** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **terminalType** | **String**|  | [optional]
 **feeDeductType** | **String**|  | [optional]

### Return type
[**WithdrawOrderWithdrawOrderRespDTOResult**](../model/WithdrawOrderWithdrawOrderRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawQuery"></a>
# **withdrawQuery**
WithdrawQueryResponse withdrawQuery(WithdrawQueryRequest request)

提现-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawQueryRequest中的参数说明参见Parameters章节
WithdrawQueryRequest request = new WithdrawQueryRequest();
request.setParentMerchantNo("100400612345");
request.setRequestNo("WITHDRAW20200327103027");
request.setOrderNo("be54b037a981440a8cfcb0549aaf5344");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawQueryResponse response = api.withdrawQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成(与易宝提现订单号两者填其一) | [optional]
 **orderNo** | **String**| 易宝提现订单号&lt;br&gt;易宝支付系统生成的提现订单号(与商户请求号两者填其一) | [optional]

### Return type
[**WithdrawQueryMGWithdrawOrderQueryRespDTOResult**](../model/WithdrawQueryMGWithdrawOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawSystemQuery"></a>
# **withdrawSystemQuery**
WithdrawSystemQueryResponse withdrawSystemQuery(WithdrawSystemQueryRequest request)

提现-查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.account.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(AccountClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
AccountClient api = AccountClientBuilder.builder().build();

//WithdrawSystemQueryRequest中的参数说明参见Parameters章节
WithdrawSystemQueryRequest request = new WithdrawSystemQueryRequest();
request.setMerchantNo("易宝支付分配的的商户唯一标识;示例值:100400612345");
request.setRequestNo("WITHDRAW20200327103027");
request.setOrderNo("be54b037a981440a8cfcb0549aaf5344");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawSystemQueryResponse response = api.withdrawSystemQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling AccountClient#withdrawSystemQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  |
 **requestNo** | **String**| 商户请求号&lt;br&gt;商户请求号，由商户自定义生成(与易宝提现订单号两者填其一) | [optional]
 **orderNo** | **String**| 易宝提现订单号&lt;br&gt;易宝支付系统生成的提现订单号(与商户请求号两者填其一) | [optional]

### Return type
[**WithdrawSystemQueryMGWithdrawOrderQueryRespDTOResult**](../model/WithdrawSystemQueryMGWithdrawOrderQueryRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

