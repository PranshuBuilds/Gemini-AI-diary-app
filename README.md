# Gemini AI Notes app 

This was my old notes app using `sql-lite` build that is now gets Upgraded

__Gemini ai apikey__ 
using free `api` and implementing that to get the results 
this just gives the implementation of __text to text__ feature and get responses 
try the app from given app link below
> [App](https://drive.google.com/file/d/1VRBzX4uQj4vxgTZeTSuc1ZZxUvoFDBdm/view?usp=sharing) 

``system prompt: write in minimum words about ``


![ss2](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/ee5ad281-4fc3-4281-8b51-5ffa8c6520aa) ![ss3](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/996c0f45-cc11-4905-a868-ae99617449be)  ![ss5](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/66c7a9f3-c037-49c1-9db1-946e98f7cc54)
 ![ss4](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/b7feb341-80d3-414b-8ae7-9644826e6d9d)

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

## TODO list

- [ ]  Markdown support
- [ ]  Add save botton
- [ ]  Image analysis
- [ ]  Speech-to-text
- [ ]  Text-to-speech
- [ ]  Chat system
  




