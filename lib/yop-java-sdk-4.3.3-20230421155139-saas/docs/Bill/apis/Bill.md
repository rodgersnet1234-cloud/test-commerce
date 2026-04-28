# BillClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**download**](BillClient.md#download) | **GET** /yos/v1.0/bill/download | 账户对账单-下载


<a name="download"></a>
# **download**
YosDownloadResponse download(DownloadRequest request)

账户对账单-下载

&lt;p&gt;请求成功返回的是一个数据流，把数据流处理后进行对账。获取对账文件时请不要以表头长度来截取对账文件信息，后期可能会新增表头参数，每天凌晨定时生成前一天的对账文件，故请商户9:00 之后下载前一天的对账文件,具体请参考&lt;a href&#x3D;\&quot;https://open.yeepay.com/docs/v2/products/ptssfk/others/5f9a6ea1f8301e001b1a870f/index.html\&quot;&gt;对账文件说明&lt;/a&gt;&lt;/p&gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.bill.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(BillClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
BillClient api = BillClientBuilder.builder().build();

//DownloadRequest中的参数说明参见Parameters章节
DownloadRequest request = new DownloadRequest();
request.setBizType("bizType_example");
request.setBillDate("2020-07-01");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.download(request);
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
    LOGGER.error("Exception when calling BillClient#download, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bizType** | **String**| 账单类型&lt;br&gt;UA_PAY:企业付款 &lt;br&gt;UA_PAY_REFUND:企业付款冲退 &lt;br&gt;UA_WITHDRAW:企业账户提现 &lt;br&gt;UA_WITHDRAW_REFUND:企业账户提现冲退 &lt;br&gt;UA_TRANSFER:企业账户转账 &lt;br&gt;UA_RECHARGE:企业账户充值 &lt;br&gt;TOGETHERANDALLOCATE:集团资金划拨 |
 **billDate** | **String**| 账单日期&lt;br&gt;不填默认昨日 | [optional]

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

