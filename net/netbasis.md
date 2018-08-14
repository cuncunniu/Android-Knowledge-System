# okhttp基本用法
## 1.get请求

  get请求的基本用法:
  java
  String url = "http://blog.csdn.net/itachi85";
        final Request request = new Request.Builder()
                .method("GET", null)
                .url(url)
                .build();
        OkHttpClient client = new OkHttpClient.Builder()
                .connectTimeout(1000, TimeUnit.MINUTES)
                .readTimeout(1000, TimeUnit.MINUTES)
                .writeTimeout(1000, TimeUnit.MINUTES)
                .build();
        Call call = client.newCall(request);
        call.enqueue(new Callback() {
            @Override
            public void onFailure(Call call, IOException e) {

            }

            @Override
            public void onResponse(Call call, Response response) throws IOException {
            }
        });
