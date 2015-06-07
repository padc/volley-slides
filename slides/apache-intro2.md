```java
public static ResponseData postData(final RequestData requestData) {
    HttpResponse httpResp;
    HttpParams httpParams = new BasicHttpParams();

    HttpConnectionParams.setConnectionTimeout(httpParams, 10000);
    HttpConnectionParams.setSoTimeout(httpParams, 10000);

    HttpClient httpClient = new DefaultHttpClient(httpParams);
    HttpPost httpPost = new HttpPost(requestData.url);

    ResponseData responseData = new ResponseData();
    responseData.url = requestData.url;
    ...
```
