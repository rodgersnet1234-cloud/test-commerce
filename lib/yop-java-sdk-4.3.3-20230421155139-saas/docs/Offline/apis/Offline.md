# OfflineClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bind**](OfflineClient.md#bind) | **POST** /rest/v1.0/offline/bind | 绑机
[**createShop**](OfflineClient.md#createShop) | **POST** /rest/v1.0/offline/create-shop | 创建网点
[**getShop**](OfflineClient.md#getShop) | **GET** /rest/v1.0/offline/get-shop | 查询网点
[**operateShop**](OfflineClient.md#operateShop) | **POST** /rest/v1.0/offline/operate-shop | 关闭/启用网点
[**queryAgentList**](OfflineClient.md#queryAgentList) | **GET** /rest/v1.0/offline/query-agent-list | 查询代理关系
[**queryShopBindList**](OfflineClient.md#queryShopBindList) | **GET** /rest/v1.0/offline/query-shop-bind-list | 查询绑机关系
[**unbind**](OfflineClient.md#unbind) | **POST** /rest/v1.0/offline/unbind | 解绑
[**updateShop**](OfflineClient.md#updateShop) | **POST** /rest/v1.0/offline/update-shop | 修改网点信息


<a name="bind"></a>
# **bind**
BindResponse bind(BindRequest request)

绑机

此接口提供给商户调用，用于终端绑机。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//BindRequest中的参数说明参见Parameters章节
BindRequest request = new BindRequest();
request.setBody(new YopBindTerminalRequestDto());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    BindResponse response = api.bind(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#bind, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**YopBindTerminalRequestDto**](../model/YopBindTerminalRequestDto.md)|  | [optional]

### Return type
[**YopBindTerminalResponseDto**](../model/YopBindTerminalResponseDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createShop"></a>
# **createShop**
CreateShopResponse createShop(CreateShopRequest request)

创建网点

此接口提供给商户调用，用于创建网点。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//CreateShopRequest中的参数说明参见Parameters章节
CreateShopRequest request = new CreateShopRequest();
request.setAddress("address_example");
request.setProvince("province_example");
request.setCity("city_example");
request.setDistrict("district_example");
request.setMobile("mobile_example");
request.setShopName("shopName_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setLinkman("linkman_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    CreateShopResponse response = api.createShop(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#createShop, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **String**|  | [optional]
 **province** | **String**|  | [optional]
 **city** | **String**|  | [optional]
 **district** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **shopName** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **linkman** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**YopCreateShopRspDTO**](../model/YopCreateShopRspDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="getShop"></a>
# **getShop**
GetShopResponse getShop(GetShopRequest request)

查询网点

此接口提供给商户调用，用于查询网点。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//GetShopRequest中的参数说明参见Parameters章节
GetShopRequest request = new GetShopRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setMerchantNo("merchantNo_example");
request.setShopName("shopName_example");
request.setShopNo("shopNo_example");
request.setStatus("status_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    GetShopResponse response = api.getShop(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#getShop, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| &lt;div&gt;发起方商户编号。*标准商户收付款方案中此参数与收款商户编号一致；*平台商户收付款方案中此参数为平台商商户编号；*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编&lt;/div&gt; |
 **merchantNo** | **String**| &lt;pre&gt;收单商编&lt;/pre&gt; |
 **shopName** | **String**| &lt;pre&gt;网点名&lt;/pre&gt; | [optional]
 **shopNo** | **String**| &lt;pre&gt;网点编号&lt;/pre&gt; | [optional]
 **status** | **String**| &lt;pre&gt;&amp;nbsp;&lt;/pre&gt; &lt;div&gt;网点状态：&lt;/div&gt; &lt;div&gt;&lt;span class&#x3D;\&quot;text-only\&quot; data-eleid&#x3D;\&quot;5\&quot;&gt;&lt;span class&#x3D;\&quot;text-only text-with-abbreviation text-with-abbreviation-bottomline\&quot;&gt;枚举&lt;/span&gt;值：&lt;/span&gt;&lt;/div&gt; &lt;div&gt;&lt;span class&#x3D;\&quot;text-only\&quot; data-eleid&#x3D;\&quot;7\&quot;&gt;&lt;em&gt;PERMIT&lt;/em&gt;：&lt;em&gt;活跃&lt;/em&gt;&lt;/span&gt;&lt;/div&gt; &lt;div&gt;&lt;span class&#x3D;\&quot;text-only\&quot; data-eleid&#x3D;\&quot;9\&quot;&gt;&lt;em&gt;FORBID&lt;/em&gt;：&lt;em&gt;关闭&lt;/em&gt;&lt;/span&gt;&lt;/div&gt; &lt;pre&gt;&amp;nbsp;&lt;/pre&gt; | [optional]

### Return type
[**YopGetShopRspDTO**](../model/YopGetShopRspDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="operateShop"></a>
# **operateShop**
OperateShopResponse operateShop(OperateShopRequest request)

关闭/启用网点

此接口提供给商户调用，用于关闭/启用网点。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//OperateShopRequest中的参数说明参见Parameters章节
OperateShopRequest request = new OperateShopRequest();
request.setOperateType("operateType_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setShopNo("shopNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    OperateShopResponse response = api.operateShop(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#operateShop, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **operateType** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **shopNo** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**YopBaseRspDTO**](../model/YopBaseRspDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="queryAgentList"></a>
# **queryAgentList**
QueryAgentListResponse queryAgentList(QueryAgentListRequest request)

查询代理关系

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//QueryAgentListRequest中的参数说明参见Parameters章节
QueryAgentListRequest request = new QueryAgentListRequest();
request.setAgentMerchantNo("agentMerchantNo_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setTerminalNo("terminalNo_example");
request.setSerialNo("serialNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryAgentListResponse response = api.queryAgentList(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#queryAgentList, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agentMerchantNo** | **String**| &lt;div&gt;代理商商编，指付款采购终端的商编&lt;/div&gt; |
 **parentMerchantNo** | **String**| &lt;div&gt;代理商上级商户编号 *标准商户收付款方案中此参数与代理商商户编号一致；*平台商户收付款方案中此参数为平台商商编；*服务商解决方案中，①代理商为标准商户时，该参数为标准商户商编 ②代理商为平台商收款或平台商入驻时，该参数为平台商商编&lt;/div&gt; |
 **terminalNo** | **String**| &lt;pre&gt;终端号&lt;/pre&gt; | [optional]
 **serialNo** | **String**| &lt;pre&gt;终端序列号&lt;/pre&gt; | [optional]

### Return type
[**YopQueryAgentRspDto**](../model/YopQueryAgentRspDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="queryShopBindList"></a>
# **queryShopBindList**
QueryShopBindListResponse queryShopBindList(QueryShopBindListRequest request)

查询绑机关系

此接口提供给商户调用，用于查询旗下网点信息。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//QueryShopBindListRequest中的参数说明参见Parameters章节
QueryShopBindListRequest request = new QueryShopBindListRequest();
request.setParentMerchantNo("parentMerchantNo_example");
request.setShopNo("shopNo_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    QueryShopBindListResponse response = api.queryShopBindList(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#queryShopBindList, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parentMerchantNo** | **String**| &lt;div&gt;发起方商户编号。*标准商户收付款方案中此参数与收款商户编号一致；*平台商户收付款方案中此参数为平台商商户编号；*服务商解决方案中，①标准商户收款时，该参数为标准商户商编 ②平台商收款或平台商入驻商户收款时，该参数为平台商商编&lt;/div&gt; |
 **shopNo** | **String**| &lt;pre&gt;网点编号&lt;/pre&gt; |
 **merchantNo** | **String**| &lt;pre&gt;收单商编&lt;/pre&gt; |

### Return type
[**YopQueryShopBindRspDto**](../model/YopQueryShopBindRspDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

<a name="unbind"></a>
# **unbind**
UnbindResponse unbind(UnbindRequest request)

解绑

此接口提供给商户调用，用于终端解绑。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//UnbindRequest中的参数说明参见Parameters章节
UnbindRequest request = new UnbindRequest();
request.setBody(new YopUnBindTerminalRequestDto());

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UnbindResponse response = api.unbind(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#unbind, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**YopUnBindTerminalRequestDto**](../model/YopUnBindTerminalRequestDto.md)|  | [optional]

### Return type
[**YopUnBindTerminalResponseDto**](../model/YopUnBindTerminalResponseDto.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateShop"></a>
# **updateShop**
UpdateShopResponse updateShop(UpdateShopRequest request)

修改网点信息

此接口提供给商户调用，用于修改网点，只支持修改联系人、手机号码和网点地址。

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.offline.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(OfflineClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
OfflineClient api = OfflineClientBuilder.builder().build();

//UpdateShopRequest中的参数说明参见Parameters章节
UpdateShopRequest request = new UpdateShopRequest();
request.setAddress("address_example");
request.setMobile("mobile_example");
request.setParentMerchantNo("parentMerchantNo_example");
request.setShopNo("shopNo_example");
request.setLinkman("linkman_example");
request.setMerchantNo("merchantNo_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    UpdateShopResponse response = api.updateShop(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling OfflineClient#updateShop, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **String**|  | [optional]
 **mobile** | **String**|  | [optional]
 **parentMerchantNo** | **String**|  | [optional]
 **shopNo** | **String**|  | [optional]
 **linkman** | **String**|  | [optional]
 **merchantNo** | **String**|  | [optional]

### Return type
[**YopBaseRspDTO**](../model/YopBaseRspDTO.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

