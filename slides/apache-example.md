```java
...
    try {
        for (Map.Entry<String,String> pair: requestData._headers.entrySet()) {
            httpPost.setHeader(pair.getKey(), pair.getValue());
        }

        List<NameValuePair> nvPair = new ArrayList<NameValuePair>(1);
        nvPair.add(new BasicNameValuePair(requestData.formBaseKey, requestData.payload));
        httpPost.setEntity(new UrlEncodedFormEntity(nvPair));

        httpResp = httpClient.execute(httpPost);
    } catch(UnsupportedEncodingException e) { // Redacted
    } catch (ClientProtocolException e) {
    } catch (SocketTimeoutException e) {
    } catch (Exception e) {
    }
...
```
