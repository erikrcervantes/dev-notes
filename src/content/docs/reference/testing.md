---
title: Software Testing
---

# About Unit Testing

please put some notes about what you've learned about testing today here.

* After doing the Coding Kata, I really started to learn about not looking to future requirements and finding the quickest solution to pass the *meanfully* failing test. 
    * I would start to overthink about how to implement the current step I was working on, but when I would think about the analogy of swimming up for air as quick as possible,
    that kept me on track.
* Also was a good lesson for me to be able to keep coming back to it throughout the day while Jeff was showing some ways to refactor it. 

# API Testing with Alba

```csharp

using Alba;

namespace HelpDesk.Tests.Software;
public class GettingSoftware
{
    // Test that we can make an HTTP GET requests to /api/software

    [Fact]
    public async Task CanGetSoftware()
    {
        var host = await AlbaHost.For<Program>();

        await host.Scenario(api =>
        {
            api.Get.Url("/api/software");
            api.StatusCodeShouldBeOk();
        });


    }
}
```

Write what you understand about this code. What is Alba? Where did that come from? What is `Program`?

* Alba is a class number that is used with unit testing tools, to aid in creating integration testing for ASP.NET Core
* The code snippet is from the HelpDesk.Tests project in the HelpDesk solution. 
* `Program` is the applications' entry point. Which I believe in this case is `/api/software`