
Because the Octopus application itself is built entirely on the API, C# programs using the API can do anything that could be done by a user of the application itself.

```C#
using Microsoft.AspNet.Builder;
using Microsoft.AspNet.Routing;
using Microsoft.Framework.DependencyInjection;

namespace HelloMvc
{
    public class Startup
    {
        public void Configure(IApplicationBuilder app)
        {
            app.UseErrorPage();

            app.UseServices(services =>
            {
                services.AddMvc();
            });

            app.UseMvc();

            app.UseWelcomePage();
        }       
    }
}
