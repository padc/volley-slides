```javas
...
    conn.setRequestProperty("Accept-Charset", "utf-8");
    conn.setRequestProperty("User-Agent", "imnotabrowser");
    conn.setConnectTimeout(10000);
    conn.setReadTimeout(10000);

    responseData.statusCode = conn.getResponseCode();

    if (responseData.statusCode / 100 != 2) {
        InputStream errorResponse = new BufferedInputStream(conn.getErrorStream());
        responseData.data = readContent(errorResponse);

        debugHeaders(conn);
        return responseData;
    }
    InputStream response = new BufferedInputStream(conn.getInputStream());
    responseData.data = readContent(response);
...
```
