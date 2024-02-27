# Gemini AI Notes app 

This was my old notes app using `sql-lite` build that is now gets Upgraded

__Gemini ai apikey__ 
using free `api` and implementing that to get the results 
this just gives the implementation of __text to text__ feature and get responses 
try the app from given app link below
> [App](https://drive.google.com/file/d/1VRBzX4uQj4vxgTZeTSuc1ZZxUvoFDBdm/view?usp=sharing) 

``system prompt: answer concisely about ``

![ss1](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/a271be18-dcfb-43b0-9c0a-07d5cabb9035)
![ss2](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/8cd3b078-d17e-4c72-9724-fcdfffe56340)
![ss3](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/3867021c-bb44-485a-894c-cc031665f63b)
![ss4](https://github.com/pranshusample765/Gemini-AI-diary-app/assets/58212835/6592681b-1655-4e5c-8a48-0104b4dd0a1d)
![12](https://github.com/PranshuBuilds/Gemini-AI-diary-app/assets/58212835/5b3b8a17-bcd7-48cd-b584-e2bf932a4b9d)
![11](https://github.com/PranshuBuilds/Gemini-AI-diary-app/assets/58212835/2b5b2653-7109-441c-90f9-b1ed888717d2)


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

- [x]  Markdown support
- [x]  Add save botton
- [x]  Speech-to-text
- [ ]  Image analysis
- [x]  Task list
- [x]  Enhancing Task list
- [ ]  Text-to-speech
- [ ]  Chat system
  




