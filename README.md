# Gemini AI Notes app 

This was my old notes app using `sql-lite` build that is now gets Upgraded

__Gemini ai apikey__ 
using free `api` and implementing that to get the results 
this just gives the implementation of __text to text__ feature and get responses 
try the [App](https://drive.google.com/file/d/1VRBzX4uQj4vxgTZeTSuc1ZZxUvoFDBdm/view?usp=sharing) 

``system prompt: write in minimum words about ``

***
## check the official Gemini AI documentation - [Gemini AI](https://ai.google.dev/tutorials/android_quickstart#multi-turn-conversations-chat)

I used `java` code from documentations , adviced to check that out for more features like : **chat** | **history** | **image recognition** |
```
// For text-only input, use the gemini-pro model
GenerativeModel gm = new GenerativeModel(/* modelName */ "gemini-pro",
// Access your API key as a Build Configuration variable (see "Set up your API key" above)
    /* apiKey */ BuildConfig.apiKey);
GenerativeModelFutures model = GenerativeModelFutures.from(gm);

Content content = new Content.Builder()
    .addText("Write a story about a magic backpack.")
    .build();

Executor executor = //Executors.newSingleThreadExecutor();//for this , we used this

ListenableFuture<GenerateContentResponse> response = model.generateContent(content);
Futures.addCallback(response, new FutureCallback<GenerateContentResponse>() {
    @Override
    public void onSuccess(GenerateContentResponse result) {
        String resultText = result.getText();
        System.out.println(resultText);
    }

    @Override
    public void onFailure(Throwable t) {
        t.printStackTrace();
    }
}, executor);
```

code is in the ``master`` branch , feel free to use __clone and contribute__ , lets make this basic app to high-end

Don't forget to leave a star on our repository! :star:

***
## Screenshots 

![ss2](https://github.com/pranshusingh/Gemini-AI-diary-app/assets/42331128/cc094df0-ebe4-4462-8299-47611787cf08)  ![ss1](https://github.com/pranshusingh/Gemini-AI-diary-app/assets/42331128/43ab6cb8-2b1b-4722-8e71-ba424f5dc65b)

| Tab 1 | Tab2 |




