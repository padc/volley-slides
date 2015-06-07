```java
import com.android.volley.RequestQueue;
import com.android.volley.Response;
import com.android.volley.toolbox.Volley;

public static RequestQueue sRequestQueue;

@Override
protected void onCreate(Bundle savedInstanceState) {
    sRequestQueue = Volley.newRequestQueue(this);
}
```

```java
GsonRequest<FeedResponse> gsonRequest = new GsonRequest<FeedResponse>(
        url, FeedResponse.class, null, params, successListener, errorListener);

mRequestQueue.add(gsonRequest);
```
