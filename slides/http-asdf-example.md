```java
HttpURLConnection conn = null;
ResponseData responseData = new ResponseData();
responseData.url = requestData.url;

try {
    conn = (HttpURLConnection) (new URL(requestData.url).openConnection());

    for (Map.Entry<String, String> entry: requestData.headers.entrySet()) {
        conn.setRequestProperty(entry.getKey(), entry.getValue());
    }
    ...
```
