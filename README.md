# Summary
- [Modularity](#modularity)

# Modularity
You can add dependency injection modularity in your projects using the following class conception :

```cs
using Versonium.Core.DependencyInjection;

public sealed class MyModule : IModule
{
    public void ConfigureServices(IServiceCollection services)
    {
        // TODO
    }
}
```

When you got some dependencies that's must be added just a single time, it's recommended to add them using those extensions :

```cs
services.AddScopedOnes<>();
services.AddTransientOnes<>();
services.AddSingletonOnes<>();
```