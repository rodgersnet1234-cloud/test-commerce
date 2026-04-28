# SupplierRemitClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**billDownload**](SupplierRemitClient.md#billDownload) | **GET** /yos/v1.0/supplier-remit/bill/download | 付款对账文件获取接口


<a name="billDownload"></a>
# **billDownload**
YosDownloadResponse billDownload(BillDownloadRequest request)

付款对账文件获取接口

支持商户进行对账文件下载。 受理失败，返回响应错误码；受理成功，返回文件

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;
//import com.yeepay.yop.sdk.model.yos.YosDownloadInputStream;
//import com.yeepay.yop.sdk.service.supplier_remit.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;
//import java.io.IOException;
//import org.apache.commons.io.IOUtils;

private static final Logger LOGGER = LoggerFactory.getLogger(SupplierRemitClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SupplierRemitClient api = SupplierRemitClientBuilder.builder().build();

//BillDownloadRequest中的参数说明参见Parameters章节
BillDownloadRequest request = new BillDownloadRequest();
request.setRemitDate("remitDate_example");

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    YosDownloadResponse response = api.billDownload(request);
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
    LOGGER.error("Exception when calling SupplierRemitClient#billDownload, ex:", e);
}

private static void saveFile(YosDownloadInputStream in) throws java.io.IOException {
    //todo save
    LOGGER.debug(IOUtils.toString(in, "UTF-8"));
}

```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **remitDate** | **String**| 付款日期 |

### Return type
YosDownloadInputStream

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/octet-stream

