```java
successListener = new Response.Listener<FeedResponse>() {
    @Override
    public void onResponse(FeedResponse response) {
        ...
    }
};

errorListener = new Response.ErrorListener() {
    @Override
    public void onErrorResponse(VolleyError error) {
        ...
    }
};
```
