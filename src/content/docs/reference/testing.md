---
title: Software Testing
---

# About Unit Testing

Please put some notes about what you've learned about testing today here.


# API Testing with Alba

```
using Alba;

namespace HelpDesk.tests.Software;
public class GettingSoftware
{
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

