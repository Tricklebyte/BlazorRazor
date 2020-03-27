# BlazorRazor 
**Reusable Razor pages and views for Blazor Applications**

 ## Blazor Server App support for IdentityServer Hybrid Flow
**This library replaces the LoginIDP and LogoutIDP pages from Kevin Dockx's pluralsight course:**\
<br/>[Authentication and Authorization in Blazor Applications by Kevin Dockx](https://app.pluralsight.com/library/courses/authentication-authorization-blazor-applications)\
<br/> In his Pluralsight course, Kevin demonstrates using the LoginIDP and LogoutIDP pages to support hybrid flow operations between the Blazor Server application and IdentityServer.\
This library allows you to use Kevin's design pattern without needing to create the LoginIDP and LogoutIDP pages for every one of your applications.\
The views do not contain User Interface design content. The users are redirected to IdentityServer to login there.

 ### LoginIDP.cshtml / LogIDP.cs
Invokes HttpContextChallengeAsync(OpenIdConnectDefaults.AuthenticationScheme), triggering the redirect to the IdentityServer login page.
If there is already a User signed in, they are redirected to the application root.

 ### LogoutIDP
Invokes SignOutAsync for both the Cookie and OpenIdConnect authentication schemes. 

### Demo
The [Demo](https://github.com/Tricklebyte/BlazorRazor/tree/master/demo) project is based on Kevin's demo project with several modifications:
* Upgraded project to .NET CORE version 3.1
* Deleted LoginIDP and LogoutIDP pages from project
* Added Reference to BlazorRazor nuget package
