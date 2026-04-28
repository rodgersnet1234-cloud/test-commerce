# MWalletClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountOpen**](MWalletClient.md#accountOpen) | **POST** /rest/v1.0/m-wallet/account/open | 开立钱包账户
[**accountQuery**](MWalletClient.md#accountQuery) | **GET** /rest/v1.0/m-wallet/account/query | 查询钱包账户信息
[**accountQueryBalance**](MWalletClient.md#accountQueryBalance) | **GET** /rest/v1.0/m-wallet/account/query-balance | 会员银行账户余额查询
[**account_face_certify_open**](MWalletClient.md#account_face_certify_open) | **POST** /rest/v1.0/m-wallet/account/face-certify-open | 开立钱包账户(支持人脸识别)
[**account_open_notify**](MWalletClient.md#account_open_notify) | **POST** /rest/v1.0/m-wallet/account/open/notify | 钱包开户成功通知
[**account_query_quota**](MWalletClient.md#account_query_quota) | **POST** /rest/v1.0/m-wallet/account/query-quota | 会员账户限额查询
[**agreementPaymentCancel**](MWalletClient.md#agreementPaymentCancel) | **POST** /rest/v1.0/m-wallet/agreement/payment-cancel | 发起免密支付解约
[**agreementPaymentSign**](MWalletClient.md#agreementPaymentSign) | **POST** /rest/v1.0/m-wallet/agreement/payment-sign | 发起免密支付签约
[**agreement_payment_query**](MWalletClient.md#agreement_payment_query) | **POST** /rest/v1.0/m-wallet/agreement/payment-query | 钱包免密支付协议查询接口
[**agreement_payment_request_v1**](MWalletClient.md#agreement_payment_request_v1) | **POST** /rest/v1.0/m-wallet/agreement/payment-request | 钱包免密支付协议请求接口
[**auto_deduction_create**](MWalletClient.md#auto_deduction_create) | **POST** /rest/v1.0/m-wallet/trade/auto-deduction/create | 会员自动扣款下单
[**auto_deduction_query**](MWalletClient.md#auto_deduction_query) | **POST** /rest/v1.0/m-wallet/trade/auto-deduction/query | 会员自动扣款查询
[**auto_withdraw**](MWalletClient.md#auto_withdraw) | **POST** /rest/v1.0/m-wallet/auto-withdraw | 发起会员自动提现
[**auto_withdraw_query**](MWalletClient.md#auto_withdraw_query) | **POST** /rest/v1.0/m-wallet/auto-withdraw-query | 自动提现查询
[**bankAccountActivation**](MWalletClient.md#bankAccountActivation) | **POST** /rest/v1.0/m-wallet/bank-account/activation | 会员银行账户一分钱激活
[**bankAccountConfirm**](MWalletClient.md#bankAccountConfirm) | **POST** /rest/v1.0/m-wallet/bank-account/confirm | 会员银行账户开户确认
[**bankAccountOpen**](MWalletClient.md#bankAccountOpen) | **POST** /rest/v1.0/m-wallet/bank-account/open | 会员银行账户开户接口
[**bankAccountQueryActivation**](MWalletClient.md#bankAccountQueryActivation) | **GET** /rest/v1.0/m-wallet/bank-account/query-activation | 会员银行账户一分钱激活结果查询
[**bankAccountQueryComplaint**](MWalletClient.md#bankAccountQueryComplaint) | **GET** /rest/v1.0/m-wallet/bank-account/query-complaint | 会员银行账户客诉订单查询
[**bankAccountQueryOpenResult**](MWalletClient.md#bankAccountQueryOpenResult) | **GET** /rest/v1.0/m-wallet/bank-account/query-open-result | 会员银行账户开户结果查询
[**bankAccountQueryTrade**](MWalletClient.md#bankAccountQueryTrade) | **GET** /rest/v1.0/m-wallet/bank-account/query-trade | 会员银行账户交易流水查询
[**bankAccountQueryWithdraw**](MWalletClient.md#bankAccountQueryWithdraw) | **GET** /rest/v1.0/m-wallet/bank-account/query-withdraw | 会员银行账户提现查询
[**bankAccountSendMsg**](MWalletClient.md#bankAccountSendMsg) | **POST** /rest/v1.0/m-wallet/bank-account/send-msg | 会员银行账户开户发送短验
[**bankAccountUpdateKeyWords**](MWalletClient.md#bankAccountUpdateKeyWords) | **POST** /rest/v1.0/m-wallet/bank-account/update-key-words | 会员银行账户关键字维护
[**bankAccountWithdraw**](MWalletClient.md#bankAccountWithdraw) | **POST** /rest/v1.0/m-wallet/bank-account/withdraw | 会员银行账户提现
[**bill_query_detail**](MWalletClient.md#bill_query_detail) | **POST** /rest/v1.0/m-wallet/bill/query-detail | 钱包账单详情查询
[**bill_query_list**](MWalletClient.md#bill_query_list) | **POST** /rest/v1.0/m-wallet/bill/query-list | 钱包账单列表查询
[**bill_query_overview**](MWalletClient.md#bill_query_overview) | **POST** /rest/v1.0/m-wallet/bill/query-overview | 钱包账单总览查询
[**cardQuery**](MWalletClient.md#cardQuery) | **POST** /rest/v1.0/m-wallet/card/query | 查询及绑定银行卡
[**memberQuery**](MWalletClient.md#memberQuery) | **GET** /rest/v1.0/m-wallet/member/query | 钱包账户信息查询
[**member_card_list**](MWalletClient.md#member_card_list) | **POST** /rest/v1.0/m-wallet/member/card-list | 会员绑卡列表查询
[**passwordManage**](MWalletClient.md#passwordManage) | **POST** /rest/v1.0/m-wallet/password/manage | 安全设置
[**rechargeInitiate**](MWalletClient.md#rechargeInitiate) | **POST** /rest/v1.0/m-wallet/recharge/initiate | 发起充值
[**rechargeQuery**](MWalletClient.md#rechargeQuery) | **GET** /rest/v1.0/m-wallet/recharge/query | 充值查询
[**subscribe_expire_notify**](MWalletClient.md#subscribe_expire_notify) | **POST** /rest/v1.0/m-wallet/subscribe-expire-notify | 会员主体订阅有效期变更通知
[**tradeOrder**](MWalletClient.md#tradeOrder) | **POST** /rest/v1.0/m-wallet/trade/order | 钱包交易支付
[**tradeOrderV2**](MWalletClient.md#tradeOrderV2) | **POST** /rest/v2.0/m-wallet/trade/order | 钱包交易下单
[**transferB2cInitiate**](MWalletClient.md#transferB2cInitiate) | **POST** /rest/v1.0/m-wallet/transfer/b2c/initiate | 发起B2C转账
[**transferB2cMarket**](MWalletClient.md#transferB2cMarket) | **POST** /rest/v1.0/m-wallet/transfer/b2c/market | 营销红包转账
[**transferB2cQuery**](MWalletClient.md#transferB2cQuery) | **GET** /rest/v1.0/m-wallet/transfer/b2c/query | B2C转账查询
[**walletCancel**](MWalletClient.md#walletCancel) | **POST** /rest/v1.0/m-wallet/wallet/cancel | 注销会员钱包
[**walletIndexV2**](MWalletClient.md#walletIndexV2) | **POST** /rest/v2.0/m-wallet/wallet/index | 钱包注册/登录接口
[**withdrawInitiate**](MWalletClient.md#withdrawInitiate) | **POST** /rest/v1.0/m-wallet/withdraw/initiate | 发起提现
[**withdrawQuery**](MWalletClient.md#withdrawQuery) | **GET** /rest/v1.0/m-wallet/withdraw/query | 提现查询


<a name="accountOpen"></a>
# **accountOpen**
AccountOpenResponse accountOpen(AccountOpenRequest request)

开立钱包账户

&lt;p&gt;商户调用此接口，输入用户的真实身份信息，易宝通过公安认证渠道认证通过后，会对应开立钱包账户。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountOpenRequest中的参数说明参见Parameters章节
AccountOpenRequest request = new AccountOpenRequest();
request.setName("张三");
request.setCertificateType("IDENTITY_CARD");
request.setCertificateNo("certificateNo_example");
request.setRequestNo("REQ6437657876");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User10232");
request.setMobile("15522919123");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountOpenResponse response = api.accountOpen(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#accountOpen, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**|  | [optional]
 **certificateType** | **String**|  | [optional]
 **certificateNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**AccountOpenWalletRequestRecordResponseDTOResult**](../model/AccountOpenWalletRequestRecordResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountQuery"></a>
# **accountQuery**
AccountQueryResponse accountQuery(AccountQueryRequest request)

查询钱包账户信息

&lt;p&gt;商户在易宝为会员开通钱包账户后，可通过接入该接口查询会员在易宝的钱包账户信息，包括钱包用户个人信息、钱包账户状态、钱包余额、认证情况及账户级别等&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountQueryRequest中的参数说明参见Parameters章节
AccountQueryRequest request = new AccountQueryRequest();
request.setMerchantUserNo("User001");
request.setMerchantNo("10012345679");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountQueryResponse response = api.accountQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#accountQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantUserNo** | **String**|  |
 **merchantNo** | **String**| 易宝支付分配的的商户唯一标识 |
 **parentMerchantNo** | **String**| 发起方商户编号（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |

### Return type
[**AccountQueryWalletMemberResponseDTOResult**](../model/AccountQueryWalletMemberResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="accountQueryBalance"></a>
# **accountQueryBalance**
AccountQueryBalanceResponse accountQueryBalance(AccountQueryBalanceRequest request)

会员银行账户余额查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountQueryBalanceRequest中的参数说明参见Parameters章节
AccountQueryBalanceRequest request = new AccountQueryBalanceRequest();
request.setMerchantMemberNo("merchantMemberNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setAccountType("accountType_example");
request.setElecAccount("elecAccount_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountQueryBalanceResponse response = api.accountQueryBalance(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#accountQueryBalance, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantMemberNo** | **String**| 商户侧存的会员编号，不同人的会员编号不能相同 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |
 **accountType** | **String**| 可选项如下:&lt;br&gt;CNCB:中信银行 | [optional]
 **elecAccount** | **String**|  | [optional]

### Return type
[**AccountQueryBalanceQueryBalanceResponseDTOResult**](../model/AccountQueryBalanceQueryBalanceResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_face_certify_open"></a>
# **account_face_certify_open**
AccountFaceCertifyOpenResponse account_face_certify_open(AccountFaceCertifyOpenRequest request)

开立钱包账户(支持人脸识别)

商户调用此接口，输入用户的真实身份信息，易宝进行人脸识别认证通过后，会对应开立钱包账户。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountFaceCertifyOpenRequest中的参数说明参见Parameters章节
AccountFaceCertifyOpenRequest request = new AccountFaceCertifyOpenRequest();
request.setName("name_example");
request.setCertificateType("IDENTITY_CARD");
request.setCertificateNo("certificateNo_example");
request.setRequestNo("requestNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setMobile("mobile_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setReturnUrl("returnUrl_example");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountFaceCertifyOpenResponse response = api.account_face_certify_open(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#account_face_certify_open, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **String**|  | [optional]
 **certificateType** | **String**|  | [optional] [enum: IDENTITY_CARD]
 **certificateNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**WalletOpenByFaceResponseDTO**](../model/WalletOpenByFaceResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_open_notify"></a>
# **account_open_notify**
AccountOpenNotifyResponse account_open_notify(AccountOpenNotifyRequest request)

钱包开户成功通知

调用此接口，通知商户开户成功结果

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountOpenNotifyRequest中的参数说明参见Parameters章节
AccountOpenNotifyRequest request = new AccountOpenNotifyRequest();
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setWalletUserNo("walletUserNo_example");
request.setNotifyUrl("notifyUrl_example");
request.setRequestNo("requestNo_example");
request.setBusinessNo("businessNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountOpenNotifyResponse response = api.account_open_notify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#account_open_notify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **walletUserNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **businessNo** | **String**|  | [optional]

### Return type
[**OpenSuccessNotifyResponseDTO**](../model/OpenSuccessNotifyResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="account_query_quota"></a>
# **account_query_quota**
AccountQueryQuotaResponse account_query_quota(AccountQueryQuotaRequest request)

会员账户限额查询

商户调用该接口，查询会员账户限额信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AccountQueryQuotaRequest中的参数说明参见Parameters章节
AccountQueryQuotaRequest request = new AccountQueryQuotaRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AccountQueryQuotaResponse response = api.account_query_quota(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#account_query_quota, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]

### Return type
[**YopQueryMemberBalanceQuotaRespDTO**](../model/YopQueryMemberBalanceQuotaRespDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="agreementPaymentCancel"></a>
# **agreementPaymentCancel**
AgreementPaymentCancelResponse agreementPaymentCancel(AgreementPaymentCancelRequest request)

发起免密支付解约

&lt;p&gt;用户在商户端发起协议解约，商户调用此接口发起解约操作。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AgreementPaymentCancelRequest中的参数说明参见Parameters章节
AgreementPaymentCancelRequest request = new AgreementPaymentCancelRequest();
request.setOperateReason("operateReason_example");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRequestNo("REQ1754364");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User89849");
request.setParentMerchantNo("parentMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AgreementPaymentCancelResponse response = api.agreementPaymentCancel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#agreementPaymentCancel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **operateReason** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**AgreementPaymentCancelFreeSecretCancelResponseDTOResult**](../model/AgreementPaymentCancelFreeSecretCancelResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="agreementPaymentSign"></a>
# **agreementPaymentSign**
AgreementPaymentSignResponse agreementPaymentSign(AgreementPaymentSignRequest request)

发起免密支付签约

&lt;p&gt;用户在商户端发起协议签约，商户调用此接口并打开对应url跳转到易宝验密签约页面，用户输入支付密码后验证并签约。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AgreementPaymentSignRequest中的参数说明参见Parameters章节
AgreementPaymentSignRequest request = new AgreementPaymentSignRequest();
request.setReturnUrl("http://www.shili.com");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRequestNo("REQ1754364");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User89849");
request.setParentMerchantNo("parentMerchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AgreementPaymentSignResponse response = api.agreementPaymentSign(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#agreementPaymentSign, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**AgreementPaymentSignRequestURLResponseDTOResult**](../model/AgreementPaymentSignRequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="agreement_payment_query"></a>
# **agreement_payment_query**
AgreementPaymentQueryResponse agreement_payment_query(AgreementPaymentQueryRequest request)

钱包免密支付协议查询接口

钱包免密支付协议查询接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AgreementPaymentQueryRequest中的参数说明参见Parameters章节
AgreementPaymentQueryRequest request = new AgreementPaymentQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AgreementPaymentQueryResponse response = api.agreement_payment_query(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#agreement_payment_query, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]

### Return type
[**FreeSecretQueryResponseDTO**](../model/FreeSecretQueryResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="agreement_payment_request_v1"></a>
# **agreement_payment_request_v1**
AgreementPaymentRequestV1Response agreement_payment_request_v1(AgreementPaymentRequestV1Request request)

钱包免密支付协议请求接口

钱包免密支付协议请求接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AgreementPaymentRequestV1Request中的参数说明参见Parameters章节
AgreementPaymentRequestV1Request request = new AgreementPaymentRequestV1Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setRequestNo("requestNo_example");
request.setReturnUrl("returnUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AgreementPaymentRequestV1Response response = api.agreement_payment_request_v1(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#agreement_payment_request_v1, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]

### Return type
[**RequestURLResponseDTO**](../model/RequestURLResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="auto_deduction_create"></a>
# **auto_deduction_create**
AutoDeductionCreateResponse auto_deduction_create(AutoDeductionCreateRequest request)

会员自动扣款下单

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AutoDeductionCreateRequest中的参数说明参见Parameters章节
AutoDeductionCreateRequest request = new AutoDeductionCreateRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setRequestNo("requestNo_example");
request.setAmount("amount_example");
request.setBindCardId("bindCardId_example");
request.setPayWay("BALANCE");
request.setExpireTime(new DateTime());
request.setGoodsName("goodsName_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoDeductionCreateResponse response = api.auto_deduction_create(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#auto_deduction_create, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **amount** | **String**|  | [optional]
 **bindCardId** | **String**|  | [optional]
 **payWay** | **String**|  | [optional] [enum: BALANCE, BIND_CARD]
 **expireTime** | **DateTime**|  | [optional]
 **goodsName** | **String**|  | [optional]

### Return type
[**AutoDeductionResponseDTO**](../model/AutoDeductionResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="auto_deduction_query"></a>
# **auto_deduction_query**
AutoDeductionQueryResponse auto_deduction_query(AutoDeductionQueryRequest request)

会员自动扣款查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AutoDeductionQueryRequest中的参数说明参见Parameters章节
AutoDeductionQueryRequest request = new AutoDeductionQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestNo("requestNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoDeductionQueryResponse response = api.auto_deduction_query(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#auto_deduction_query, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]

### Return type
[**AutoDeductionQueryResponseDTO**](../model/AutoDeductionQueryResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="auto_withdraw"></a>
# **auto_withdraw**
AutoWithdrawResponse auto_withdraw(AutoWithdrawRequest request)

发起会员自动提现

发起会员自动提现，用户可查询自动提现结果

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AutoWithdrawRequest中的参数说明参见Parameters章节
AutoWithdrawRequest request = new AutoWithdrawRequest();
request.setOperatedMerchantNo("operatedMerchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("User8232");
request.setRequestNo("requestNo_example");
request.setNotifyUrl("notifyUrl_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoWithdrawResponse response = api.auto_withdraw(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#auto_withdraw, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **operatedMerchantNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**AutoWithdrawResponseDTO**](../model/AutoWithdrawResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="auto_withdraw_query"></a>
# **auto_withdraw_query**
AutoWithdrawQueryResponse auto_withdraw_query(AutoWithdrawQueryRequest request)

自动提现查询

自动提现 订单 查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//AutoWithdrawQueryRequest中的参数说明参见Parameters章节
AutoWithdrawQueryRequest request = new AutoWithdrawQueryRequest();
request.setOperatedMerchantNo("operatedMerchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setRequestNo("REQ6437657876");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    AutoWithdrawQueryResponse response = api.auto_withdraw_query(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#auto_withdraw_query, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **operatedMerchantNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]

### Return type
[**AutoWithdrawQueryResponseDTO**](../model/AutoWithdrawQueryResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountActivation"></a>
# **bankAccountActivation**
BankAccountActivationResponse bankAccountActivation(BankAccountActivationRequest request)

会员银行账户一分钱激活

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountActivationRequest中的参数说明参见Parameters章节
BankAccountActivationRequest request = new BankAccountActivationRequest();
request.setMerchantMemberNo("merchantMemberNo_example");
request.setAccountNo("accountNo_example");
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountActivationResponse response = api.bankAccountActivation(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountActivation, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantMemberNo** | **String**|  | [optional]
 **accountNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BankAccountActivationBankAccountActivationRespDTOResult**](../model/BankAccountActivationBankAccountActivationRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountConfirm"></a>
# **bankAccountConfirm**
BankAccountConfirmResponse bankAccountConfirm(BankAccountConfirmRequest request)

会员银行账户开户确认

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountConfirmRequest中的参数说明参见Parameters章节
BankAccountConfirmRequest request = new BankAccountConfirmRequest();
request.setRequestNo("requestNo_example");
request.setShortMsg("shortMsg_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountConfirmResponse response = api.bankAccountConfirm(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountConfirm, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **shortMsg** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BankAccountConfirmConfirmBankAccountResponseDTOResult**](../model/BankAccountConfirmConfirmBankAccountResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountOpen"></a>
# **bankAccountOpen**
BankAccountOpenResponse bankAccountOpen(BankAccountOpenRequest request)

会员银行账户开户接口

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountOpenRequest中的参数说明参见Parameters章节
BankAccountOpenRequest request = new BankAccountOpenRequest();
request.setBody(new BankAccountOpenBankAccountRequestDTOParam());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountOpenResponse response = api.bankAccountOpen(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountOpen, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**BankAccountOpenBankAccountRequestDTOParam**](../model/BankAccountOpenBankAccountRequestDTOParam.md)|  |

### Return type
[**BankAccountOpenBankAccountResponseDTOResult**](../model/BankAccountOpenBankAccountResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bankAccountQueryActivation"></a>
# **bankAccountQueryActivation**
BankAccountQueryActivationResponse bankAccountQueryActivation(BankAccountQueryActivationRequest request)

会员银行账户一分钱激活结果查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountQueryActivationRequest中的参数说明参见Parameters章节
BankAccountQueryActivationRequest request = new BankAccountQueryActivationRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryActivationResponse response = api.bankAccountQueryActivation(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountQueryActivation, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**| 同一分钱激活里的请求号 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |

### Return type
[**BankAccountQueryActivationQueryBankAccountActivationRespDTOResult**](../model/BankAccountQueryActivationQueryBankAccountActivationRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountQueryComplaint"></a>
# **bankAccountQueryComplaint**
BankAccountQueryComplaintResponse bankAccountQueryComplaint(BankAccountQueryComplaintRequest request)

会员银行账户客诉订单查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountQueryComplaintRequest中的参数说明参见Parameters章节
BankAccountQueryComplaintRequest request = new BankAccountQueryComplaintRequest();
request.setMerchantMemberNo("merchantMemberNo_example");
request.setAccountNo("accountNo_example");
request.setBankTradeNo("bankTradeNo_example");
request.setTradeTime("tradeTime_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryComplaintResponse response = api.bankAccountQueryComplaint(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountQueryComplaint, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantMemberNo** | **String**| 商户侧存的会员编号，不同人的会员编号不能相同 |
 **accountNo** | **String**|  |
 **bankTradeNo** | **String**|  |
 **tradeTime** | **String**| 参数格式为：yyyyMMdd |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |

### Return type
[**BankAccountQueryComplaintQueryComplaintOrderRespDTOResult**](../model/BankAccountQueryComplaintQueryComplaintOrderRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountQueryOpenResult"></a>
# **bankAccountQueryOpenResult**
BankAccountQueryOpenResultResponse bankAccountQueryOpenResult(BankAccountQueryOpenResultRequest request)

会员银行账户开户结果查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountQueryOpenResultRequest中的参数说明参见Parameters章节
BankAccountQueryOpenResultRequest request = new BankAccountQueryOpenResultRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryOpenResultResponse response = api.bankAccountQueryOpenResult(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountQueryOpenResult, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**| 同开户申请的接口请求号一致 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |

### Return type
[**BankAccountQueryOpenResultQueryOpenResultResponseDTOResult**](../model/BankAccountQueryOpenResultQueryOpenResultResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountQueryTrade"></a>
# **bankAccountQueryTrade**
BankAccountQueryTradeResponse bankAccountQueryTrade(BankAccountQueryTradeRequest request)

会员银行账户交易流水查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountQueryTradeRequest中的参数说明参见Parameters章节
BankAccountQueryTradeRequest request = new BankAccountQueryTradeRequest();
request.setMerchantMemberNo("merchantMemberNo_example");
request.setAccountNo("accountNo_example");
request.setBeginDate("beginDate_example");
request.setEndDate("endDate_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setLoanFlag("loanFlag_example");
request.setStartNum(56);
request.setQueryNum(56);
request.setQueryToken("queryToken_example");
request.setQueryTime("queryTime_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryTradeResponse response = api.bankAccountQueryTrade(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountQueryTrade, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantMemberNo** | **String**| 商户侧存的会员编号，不同人的会员编号不能相同 |
 **accountNo** | **String**|  |
 **beginDate** | **String**| 日期参数格式（yyyyMMdd）&lt;br&gt;起始日期和截止日期间隔不能超过6个月 |
 **endDate** | **String**| 日期参数格式（yyyyMMdd）&lt;br&gt;起始日期和截止日期间隔不能超过6个月 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |
 **loanFlag** | **String**| 可选项如下:&lt;br&gt;INCOME:收入&lt;br&gt;PAY:支出 | [optional]
 **startNum** | **Integer**| 按此值查询其后交易流水，不填的话，默认是1。传1是首次查询，传其他值是非首次查询，非首次查询需要传queryToken和queryTime | [optional]
 **queryNum** | **Integer**| 不填的话默认是10，最大条数99 | [optional]
 **queryToken** | **String**| 首次查询不用传，非首次查询传上次查询的返回queryToken | [optional]
 **queryTime** | **String**| 首次查询不用传，非首次查询传上次查询的返回值queryTime | [optional]

### Return type
[**BankAccountQueryTradeQueryBankAccountTradeRespDTOResult**](../model/BankAccountQueryTradeQueryBankAccountTradeRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountQueryWithdraw"></a>
# **bankAccountQueryWithdraw**
BankAccountQueryWithdrawResponse bankAccountQueryWithdraw(BankAccountQueryWithdrawRequest request)

会员银行账户提现查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountQueryWithdrawRequest中的参数说明参见Parameters章节
BankAccountQueryWithdrawRequest request = new BankAccountQueryWithdrawRequest();
request.setRequestNo("requestNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountQueryWithdrawResponse response = api.bankAccountQueryWithdraw(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountQueryWithdraw, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**| 同会员银行账户提现接口的请求号 |
 **parentMerchantNo** | **String**| 发起方商户编号&lt;br&gt;（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 商户编号&lt;br&gt;易宝支付分配的的商户唯一标识 |

### Return type
[**BankAccountQueryWithdrawQueryBankAccountWithDrawRespDTOResult**](../model/BankAccountQueryWithdrawQueryBankAccountWithDrawRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountSendMsg"></a>
# **bankAccountSendMsg**
BankAccountSendMsgResponse bankAccountSendMsg(BankAccountSendMsgRequest request)

会员银行账户开户发送短验

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountSendMsgRequest中的参数说明参见Parameters章节
BankAccountSendMsgRequest request = new BankAccountSendMsgRequest();
request.setRequestNo("requestNo_example");
request.setMerchantMemberNo("merchantMemberNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountSendMsgResponse response = api.bankAccountSendMsg(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountSendMsg, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **merchantMemberNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BankAccountSendMsgBankShortMsgResponseDTOResult**](../model/BankAccountSendMsgBankShortMsgResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountUpdateKeyWords"></a>
# **bankAccountUpdateKeyWords**
BankAccountUpdateKeyWordsResponse bankAccountUpdateKeyWords(BankAccountUpdateKeyWordsRequest request)

会员银行账户关键字维护

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountUpdateKeyWordsRequest中的参数说明参见Parameters章节
BankAccountUpdateKeyWordsRequest request = new BankAccountUpdateKeyWordsRequest();
request.setOperateType("operateType_example");
request.setKeyWordStrs("keyWordStrs_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountUpdateKeyWordsResponse response = api.bankAccountUpdateKeyWords(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountUpdateKeyWords, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **operateType** | **String**|  | [optional]
 **keyWordStrs** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BankAccountUpdateKeyWordsBankKeyWordsResponseDTOResult**](../model/BankAccountUpdateKeyWordsBankKeyWordsResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bankAccountWithdraw"></a>
# **bankAccountWithdraw**
BankAccountWithdrawResponse bankAccountWithdraw(BankAccountWithdrawRequest request)

会员银行账户提现

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BankAccountWithdrawRequest中的参数说明参见Parameters章节
BankAccountWithdrawRequest request = new BankAccountWithdrawRequest();
request.setMerchantMemberNo("merchantMemberNo_example");
request.setRequestNo("requestNo_example");
request.setAccountNo("accountNo_example");
request.setAccountType("accountType_example");
request.setOneAccountBankNo("oneAccountBankNo_example");
request.setBindBankPhone("bindBankPhone_example");
request.setWithdrawPrice(new BigDecimal("0"));
request.setRemark("remark_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BankAccountWithdrawResponse response = api.bankAccountWithdraw(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bankAccountWithdraw, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantMemberNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **accountNo** | **String**|  | [optional]
 **accountType** | **String**|  | [optional]
 **oneAccountBankNo** | **String**|  | [optional]
 **bindBankPhone** | **String**|  | [optional]
 **withdrawPrice** | **BigDecimal**|  | [optional]
 **remark** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**BankAccountWithdrawBankAccountWithDrawRespDTOResult**](../model/BankAccountWithdrawBankAccountWithDrawRespDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bill_query_detail"></a>
# **bill_query_detail**
BillQueryDetailResponse bill_query_detail(BillQueryDetailRequest request)

钱包账单详情查询

商户通过调用该接口，查询账单详情信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BillQueryDetailRequest中的参数说明参见Parameters章节
BillQueryDetailRequest request = new BillQueryDetailRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setUniqueOrderNo("uniqueOrderNo_example");
request.setOrderType("WITHDRAW");
request.setOrderDate(new DateTime());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillQueryDetailResponse response = api.bill_query_detail(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bill_query_detail, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **uniqueOrderNo** | **String**|  | [optional]
 **orderType** | **String**|  | [optional] [enum: WITHDRAW, RECHARGE, PAYMENT, DIVIDE, DIVIDE_REFUND, REFUND, PAYMENT_MANAGE, BONUS]
 **orderDate** | **DateTime**|  | [optional]

### Return type
[**BillDetailResponseDto**](../model/BillDetailResponseDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bill_query_list"></a>
# **bill_query_list**
BillQueryListResponse bill_query_list(BillQueryListRequest request)

钱包账单列表查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BillQueryListRequest中的参数说明参见Parameters章节
BillQueryListRequest request = new BillQueryListRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setOrderType("WITHDRAW");
request.setPage(56);
request.setPageNum(56);
request.setEndTime(new DateTime());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillQueryListResponse response = api.bill_query_list(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bill_query_list, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **orderType** | **String**|  | [optional] [enum: WITHDRAW, RECHARGE, PAYMENT, DIVIDE, DIVIDE_REFUND, REFUND, PAYMENT_MANAGE, BONUS]
 **page** | **Integer**|  | [optional]
 **pageNum** | **Integer**|  | [optional]
 **endTime** | **DateTime**|  | [optional]

### Return type
[**BillListResponseDto**](../model/BillListResponseDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="bill_query_overview"></a>
# **bill_query_overview**
BillQueryOverviewResponse bill_query_overview(BillQueryOverviewRequest request)

钱包账单总览查询

商户调用该接口，查询钱包账单总览信息

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//BillQueryOverviewRequest中的参数说明参见Parameters章节
BillQueryOverviewRequest request = new BillQueryOverviewRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");
request.setStartMonth("startMonth_example");
request.setEndMonth("endMonth_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BillQueryOverviewResponse response = api.bill_query_overview(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#bill_query_overview, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **startMonth** | **String**|  | [optional]
 **endMonth** | **String**|  | [optional]

### Return type
[**BillOverviewResponseDto**](../model/BillOverviewResponseDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="cardQuery"></a>
# **cardQuery**
CardQueryResponse cardQuery(CardQueryRequest request)

查询及绑定银行卡

&lt;p&gt;商户调用该接口，易宝返回url可跳转至对应用户的银行卡列表，此页面支持用户查询绑卡列表、绑定新卡和解绑已有银行卡。&lt;/p&gt; &lt;p&gt;绑定银行卡：用户在银行卡列表页申请绑定新卡，提交银行卡信息（包括姓银行卡号、手机号）申请绑定银行卡，完成银行卡信息认证；同时系统会根据认证渠道规则升级用户钱包账户。&lt;/p&gt; &lt;p&gt;解绑银行卡：用户在银行卡列表页申请解绑银行卡，确认支付密码完成解绑。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//CardQueryRequest中的参数说明参见Parameters章节
CardQueryRequest request = new CardQueryRequest();
request.setReturnUrl("http://www.shili.com/");
request.setRequestNo("REQ394032930");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User53423");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CardQueryResponse response = api.cardQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#cardQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **returnUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**CardQueryRequestURLResponseDTOResult**](../model/CardQueryRequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="memberQuery"></a>
# **memberQuery**
MemberQueryResponse memberQuery(MemberQueryRequest request)

钱包账户信息查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//MemberQueryRequest中的参数说明参见Parameters章节
MemberQueryRequest request = new MemberQueryRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setExternalUserId("User8232");
request.setMemberNo("memberNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MemberQueryResponse response = api.memberQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#memberQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **merchantNo** | **String**| 易宝支付分配的的商户唯一标识 |
 **externalUserId** | **String**| 用户在商户侧的用户ID&lt;br&gt;与会员号二选一必填 | [optional]
 **memberNo** | **String**| 与商户用户ID二选一必填 | [optional]

### Return type
[**MemberQueryQueryMemberInfoResponseDTOResult**](../model/MemberQueryQueryMemberInfoResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="member_card_list"></a>
# **member_card_list**
MemberCardListResponse member_card_list(MemberCardListRequest request)

会员绑卡列表查询

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//MemberCardListRequest中的参数说明参见Parameters章节
MemberCardListRequest request = new MemberCardListRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("merchantUserNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MemberCardListResponse response = api.member_card_list(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#member_card_list, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]

### Return type
[**MemberQueryBindCardListResponseDTO**](../model/MemberQueryBindCardListResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="passwordManage"></a>
# **passwordManage**
PasswordManageResponse passwordManage(PasswordManageRequest request)

安全设置

&lt;p&gt;商户调用此接口，跳转到易宝密码管理页面，此页面用于用户修改或重新设置钱包支付密码。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//PasswordManageRequest中的参数说明参见Parameters章节
PasswordManageRequest request = new PasswordManageRequest();
request.setReturnUrl("http://www.shili.com");
request.setRequestNo("REQ4235232");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User8923");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    PasswordManageResponse response = api.passwordManage(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#passwordManage, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **returnUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**PasswordManageRequestURLResponseDTOResult**](../model/PasswordManageRequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeInitiate"></a>
# **rechargeInitiate**
RechargeInitiateResponse rechargeInitiate(RechargeInitiateRequest request)

发起充值

&lt;p&gt;用户在商户端发起充值，商户调用此接口并打开对应url跳转到易宝充值收银台，用户在收银台选择银行卡或绑定新卡并确认支付密码后完成充值。其中：充值的银行卡必须为借记卡即储蓄卡。&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//RechargeInitiateRequest中的参数说明参见Parameters章节
RechargeInitiateRequest request = new RechargeInitiateRequest();
request.setAmount("10.5");
request.setReturnUrl("http://www.shili.com");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRequestNo("REQ655498");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User89849");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeInitiateResponse response = api.rechargeInitiate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#rechargeInitiate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amount** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**RechargeInitiateRequestURLResponseDTOResult**](../model/RechargeInitiateRequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="rechargeQuery"></a>
# **rechargeQuery**
RechargeQueryResponse rechargeQuery(RechargeQueryRequest request)

充值查询

&lt;p&gt;商户通过请求该接口查询用户充值结果&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//RechargeQueryRequest中的参数说明参见Parameters章节
RechargeQueryRequest request = new RechargeQueryRequest();
request.setRequestNo("REQ8390423");
request.setMerchantNo("10012345679");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    RechargeQueryResponse response = api.rechargeQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#rechargeQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |
 **merchantNo** | **String**| 易宝支付分配的的商户唯一标识 |
 **parentMerchantNo** | **String**| 发起方商户编号（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |

### Return type
[**RechargeQueryQueryRechargeResponseDTOResult**](../model/RechargeQueryQueryRechargeResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="subscribe_expire_notify"></a>
# **subscribe_expire_notify**
SubscribeExpireNotifyResponse subscribe_expire_notify(SubscribeExpireNotifyRequest request)

会员主体订阅有效期变更通知

会员对应主体的订阅有效期变更通知

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//SubscribeExpireNotifyRequest中的参数说明参见Parameters章节
SubscribeExpireNotifyRequest request = new SubscribeExpireNotifyRequest();
request.setBody(new SubscribeNotifyRequestDTO());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    SubscribeExpireNotifyResponse response = api.subscribe_expire_notify(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#subscribe_expire_notify, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubscribeNotifyRequestDTO**](../model/SubscribeNotifyRequestDTO.md)|  | [optional]

### Return type
[**SubscribeNotifyResponseDTO**](../model/SubscribeNotifyResponseDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="tradeOrder"></a>
# **tradeOrder**
TradeOrderResponse tradeOrder(TradeOrderRequest request)

钱包交易支付

用户与商户之间发生商品交易行为，用户可使用钱包账户余额或绑定银行卡方式支付给商户，商户调用此接口完成支付行为。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//TradeOrderRequest中的参数说明参见Parameters章节
TradeOrderRequest request = new TradeOrderRequest();
request.setRequestNo("trade1564042424954");
request.setParentMerchantNo("10040040565");
request.setMerchantNo("10040020562");
request.setMerchantUserNo("LC1563447603047");
request.setPayAmount("0.01");
request.setNotifyUrl("https://www.testurl.com/callback");
request.setReturnUrl("https://www.testurl.com/html");
request.setProductName("电脑");
request.setRemark("remark_example");
request.setFundProcessType("DELAY_SETTLE");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TradeOrderResponse response = api.tradeOrder(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#tradeOrder, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **payAmount** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **productName** | **String**|  | [optional]
 **remark** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]

### Return type
[**TradeOrderMemberTradOrderRespResult**](../model/TradeOrderMemberTradOrderRespResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="tradeOrderV2"></a>
# **tradeOrderV2**
TradeOrderV2Response tradeOrderV2(TradeOrderV2Request request)

钱包交易下单

用户与商户之间发生商品交易行为，用户可使用钱包账户余额或绑定银行卡方式支付给商户，商户调用此接口完成支付行为。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//TradeOrderV2Request中的参数说明参见Parameters章节
TradeOrderV2Request request = new TradeOrderV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setOrderId("orderId_example");
request.setOrderAmount(new BigDecimal("0"));
request.setExpiredTime("2023-05-07 10:49:07");
request.setNotifyUrl("notifyUrl_example");
request.setCsUrl("csUrl_example");
request.setMemo("memo_example");
request.setGoodsName("goodsName_example");
request.setFundProcessType("fundProcessType_example");
request.setMemberNo("memberNo_example");
request.setPayerIp("payerIp_example");
request.setPayAgreement("payAgreement_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TradeOrderV2Response response = api.tradeOrderV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#tradeOrderV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **orderId** | **String**|  | [optional]
 **orderAmount** | **BigDecimal**|  | [optional]
 **expiredTime** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **csUrl** | **String**|  | [optional]
 **memo** | **String**|  | [optional]
 **goodsName** | **String**|  | [optional]
 **fundProcessType** | **String**|  | [optional]
 **memberNo** | **String**|  | [optional]
 **payerIp** | **String**|  | [optional]
 **payAgreement** | **String**|  | [optional]

### Return type
[**TradeOrderV2APIWalletPayResponseDTOResult**](../model/TradeOrderV2APIWalletPayResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferB2cInitiate"></a>
# **transferB2cInitiate**
TransferB2cInitiateResponse transferB2cInitiate(TransferB2cInitiateRequest request)

发起B2C转账

商户与用户之间发生的交易行为，商户可向用户的钱包账户转账，商户调用此接口完成转账行为

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//TransferB2cInitiateRequest中的参数说明参见Parameters章节
TransferB2cInitiateRequest request = new TransferB2cInitiateRequest();
request.setParentMerchantNo("10012345678");
request.setFromMerchantNo("10012345676");
request.setToMerchantNo("10012345679");
request.setToMerchantUserNo("User90958");
request.setRequestNo("REQ58290");
request.setOrderAmount("10.01");
request.setFeeChargeSide("feeChargeSide_example");
request.setNotifyUrl("http://www.shili.com/notify");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferB2cInitiateResponse response = api.transferB2cInitiate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#transferB2cInitiate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **fromMerchantNo** | **String**|  | [optional]
 **toMerchantNo** | **String**|  | [optional]
 **toMerchantUserNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **orderAmount** | **String**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]

### Return type
[**TransferB2cInitiateWalletTransferB2CResponseDTOResult**](../model/TransferB2cInitiateWalletTransferB2CResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferB2cMarket"></a>
# **transferB2cMarket**
TransferB2cMarketResponse transferB2cMarket(TransferB2cMarketRequest request)

营销红包转账

商户与用户之间发生的交易行为，商户可向用户的钱包账户转账，商户调用此接口完成转账行为

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//TransferB2cMarketRequest中的参数说明参见Parameters章节
TransferB2cMarketRequest request = new TransferB2cMarketRequest();
request.setParentMerchantNo("10012345678");
request.setFromMerchantNo("10012345676");
request.setToMerchantNo("10012345679");
request.setToMerchantUserNo("User90958");
request.setRequestNo("REQ58290");
request.setOrderAmount("10.01");
request.setFeeChargeSide("feeChargeSide_example");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRemark("remark_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferB2cMarketResponse response = api.transferB2cMarket(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#transferB2cMarket, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **fromMerchantNo** | **String**|  | [optional]
 **toMerchantNo** | **String**|  | [optional]
 **toMerchantUserNo** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **orderAmount** | **String**|  | [optional]
 **feeChargeSide** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **remark** | **String**|  | [optional]

### Return type
[**TransferB2cMarketWalletTransferB2CResponseDTOResult**](../model/TransferB2cMarketWalletTransferB2CResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="transferB2cQuery"></a>
# **transferB2cQuery**
TransferB2cQueryResponse transferB2cQuery(TransferB2cQueryRequest request)

B2C转账查询

商户通过请求该接口查询商户向用户转账的订单结果

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//TransferB2cQueryRequest中的参数说明参见Parameters章节
TransferB2cQueryRequest request = new TransferB2cQueryRequest();
request.setParentMerchantNo("10012345678");
request.setFromMerchantNo("10012345679");
request.setRequestNo("REQ12345678");
request.setBusinessNo("businessNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    TransferB2cQueryResponse response = api.transferB2cQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#transferB2cQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| 发起方商户编号（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |
 **fromMerchantNo** | **String**| 交易主体商编(转出方商编） |
 **requestNo** | **String**| 商户请求号，与易宝订单号不能同时为空 | [optional]
 **businessNo** | **String**| 转账发起完成后，易宝返回的唯一订单号 | [optional]

### Return type
[**TransferB2cQueryQueryMGB2CResponseDTOResult**](../model/TransferB2cQueryQueryMGB2CResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="walletCancel"></a>
# **walletCancel**
WalletCancelResponse walletCancel(WalletCancelRequest request)

注销会员钱包

商户注销会员钱包功能

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//WalletCancelRequest中的参数说明参见Parameters章节
WalletCancelRequest request = new WalletCancelRequest();
request.setMerchantNo("10012345678");
request.setMerchantUserNo("User90958");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WalletCancelResponse response = api.walletCancel(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#walletCancel, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**WalletCancelMemberCancelResponseDTOResult**](../model/WalletCancelMemberCancelResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="walletIndexV2"></a>
# **walletIndexV2**
WalletIndexV2Response walletIndexV2(WalletIndexV2Request request)

钱包注册/登录接口

&lt;p&gt;通过该接口获取钱包注册/登陆页面&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//WalletIndexV2Request中的参数说明参见Parameters章节
WalletIndexV2Request request = new WalletIndexV2Request();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setMerchantUserNo("User8232");
request.setUserMerchantNo("10012345678");
request.setName("张三");
request.setCertificateType("certificateType_example");
request.setCertificateNo("certificateNo_example");
request.setMobile("15522919123");
request.setReturnUrl("http://www.shili.com");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRequestNo("REQ6437657876");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WalletIndexV2Response response = api.walletIndexV2(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#walletIndexV2, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **userMerchantNo** | **String**|  | [optional]
 **name** | **String**|  | [optional]
 **certificateType** | **String**|  | [optional]
 **certificateNo** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]

### Return type
[**WalletIndexV2RequestURLResponseDTOResult**](../model/WalletIndexV2RequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawInitiate"></a>
# **withdrawInitiate**
WithdrawInitiateResponse withdrawInitiate(WithdrawInitiateRequest request)

发起提现

&lt;p&gt;用户在商户端发起提现，商户调用此接口并打开对应url跳转到易宝提现收银台，用户在收银台选择银行卡或绑定新卡并确认支付密码后完成提现。其中：提现的银行卡必须为借记卡即储蓄卡。&lt;/p&gt; &lt;p&gt;提现到账类型说明（商户据此引导用户）：&lt;br /&gt;1）实时到账，用户提交提现申请成功后，资金于（一小时以内）到账。&lt;br /&gt;2）2小时到账，用户提交提现申请成功后，资金将于两小时后到账。&lt;br /&gt;3）次日到账，用户提交提现申请成功后，资金将于次日7：00以后到账（例：周六发起周日7：00以后到账）&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//WithdrawInitiateRequest中的参数说明参见Parameters章节
WithdrawInitiateRequest request = new WithdrawInitiateRequest();
request.setAmount("10.5");
request.setWithdrawType("0");
request.setReturnUrl("http://www.shili.com");
request.setNotifyUrl("http://www.shili.com/notify");
request.setRequestNo("REQ85293");
request.setMerchantNo("10012345679");
request.setMerchantUserNo("User8232");
request.setFeeInnerType("解释说明：内扣即用户发起10元，手续费0.1元，则用户提现到账9.9，扣用户余额10元；外扣即用户发起10元，手续费0.1元，用户提现到账10元，扣用户余额10.1元");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawInitiateResponse response = api.withdrawInitiate(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#withdrawInitiate, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amount** | **String**|  | [optional]
 **withdrawType** | **String**|  | [optional]
 **returnUrl** | **String**|  | [optional]
 **notifyUrl** | **String**|  | [optional]
 **requestNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]
 **merchantUserNo** | **String**|  | [optional]
 **feeInnerType** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]

### Return type
[**WithdrawInitiateRequestURLResponseDTOResult**](../model/WithdrawInitiateRequestURLResponseDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="withdrawQuery"></a>
# **withdrawQuery**
WithdrawQueryResponse withdrawQuery(WithdrawQueryRequest request)

提现查询

&lt;p&gt;商户通过请求该接口查询用户提现信息&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.m_wallet.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(MWalletClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
MWalletClient api = MWalletClientBuilder.builder().build();

//WithdrawQueryRequest中的参数说明参见Parameters章节
WithdrawQueryRequest request = new WithdrawQueryRequest();
request.setRequestNo("REQ82942");
request.setMerchantNo("10012345679");
request.setParentMerchantNo("10012345678");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    WithdrawQueryResponse response = api.withdrawQuery(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling MWalletClient#withdrawQuery, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestNo** | **String**|  |
 **merchantNo** | **String**| 易宝支付分配的的商户唯一标识 |
 **parentMerchantNo** | **String**| 发起方商户编号（标准商户收付款方案中此参数与商编一致，平台商户收付款方案中此参数为平台商商户编号） |

### Return type
[**WithdrawQueryWalletQueryWithdrawResultDTOResult**](../model/WithdrawQueryWalletQueryWithdrawResultDTOResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

