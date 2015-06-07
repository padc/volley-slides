```java
    } catch (FileNotFoundException e) { // Redacted
    } catch(SocketTimeoutException e) {
    } catch(UnknownHostException e) {
    } catch (Exception e) {
    } finally {
        if (conn != null) conn.disconnect();
    }

    return responseData;
}
```
