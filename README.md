# hangfire-template-netcore
Template Hangfire .NET Core

# IIS Configuration

https://docs.hangfire.io/en/latest/deployment-to-production/making-aspnet-app-always-running.html

https://forums.asp.net/t/1755922.aspx?IProcessHostPreloadClient+An+error+occurred+while+executing+Preload+method+

<pre>

namespace Administration.Presentation
{
    public class StartUp : System.Web.Hosting.IProcessHostPreloadClient
    {
        public void Preload(string[] parameters)
        {
           
        }
    }
}

<serviceAutoStartProviders>
       <add name="AutoStartProvider" type="Administration.Presentation.StartUp, Administration.Presentation" />
</serviceAutoStartProviders>

</pre>
