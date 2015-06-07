```java
    if (httpResp != null) {
        try {
            HttpEntity entity = httpResp.getEntity();

            responseData.statusCode = httpResp.getStatusLine().getStatusCode();
            if (entity != null) {
                responseData.data = readContent(entity.getContent());
                entity.consumeContent();
            }
        } catch (UnsupportedEncodingException e) { // Redacted
        } catch (Exception e) {
        }
    }

    return responseData;
}
```
