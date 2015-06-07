```java
private static String readContent(InputStream inputStream) throws IOException {
    BufferedReader bufferedReader = new BufferedReader(
            new InputStreamReader(inputStream, "utf-8"));
    StringBuffer content = new StringBuffer();

    try {
        for (String line; (line = bufferedReader.readLine()) != null; ) {
            content.append(line);
        }
    } finally {
        bufferedReader.close();
    }

    return content.toString();
}
```
