# SysClient

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**merchantQualUpload**](SysClient.md#merchantQualUpload) | **POST** /yos/v1.0/sys/merchant/qual/upload | 子商户入网资质文件上传


<a name="merchantQualUpload"></a>
# **merchantQualUpload**
MerchantQualUploadResponse merchantQualUpload(MerchantQualUploadRequest request)

子商户入网资质文件上传

&lt;p&gt;子商户入网资质文件上传，程序实现方式请参考，&lt;a href&#x3D;\&quot;https://open.yeepay.com/docs/v2/products/opr/others/5e941bd9c73481001a17bd85/index.html\&quot;&gt;文件上传程序实现样例&lt;/a &gt;&lt;/p &gt; &lt;p&gt;银行卡图片、身份证正反面不能超过5M&lt;/p &gt; &lt;p class&#x3D;\&quot;p1\&quot;&gt;营业执照图片 不能超过4M&lt;/p &gt; &lt;p class&#x3D;\&quot;p1\&quot;&gt;格式为 JPG（JPEG），BMP，PNG，GIF，TIFF，PDF&lt;/p &gt;

### Example
```java
//import com.yeepay.yop.sdk.exception.YopClientException;

//import com.yeepay.yop.sdk.service.sys.model.*;
// 日志框架slf4j
//import org.slf4j.Logger;
//import org.slf4j.LoggerFactory;

private static final Logger LOGGER = LoggerFactory.getLogger(SysClient.class);

// 该Client线程安全，请使用单例模式，多次请求共用
SysClient api = SysClientBuilder.builder().build();

//MerchantQualUploadRequest中的参数说明参见Parameters章节
MerchantQualUploadRequest request = new MerchantQualUploadRequest();
request.setMerQual(new File("/path/to/file"));

//多appKey请求需在请求时指定appKey
//  request.getRequestConfig().setAppKey("test");

//加密请求需要在requestConfig中指定加密选项
//  request.getRequestConfig().setNeedEncrypt(true);

try {
    MerchantQualUploadResponse response = api.merchantQualUpload(request);
    LOGGER.info("result:{}", response.getResult());
} catch (YopClientException e) {
    LOGGER.error("Exception when calling SysClient#merchantQualUpload, ex:", e);
}


```
### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **merQual** | **File**|  | [optional]

### Return type
[**MerchantQualUploadMerFileUploadRespDtoResult**](../model/MerchantQualUploadMerFileUploadRespDtoResult.md)

### Authorization
YOP-SM2-SM3


### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

