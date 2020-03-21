# BlazorRazor 
**Reusable Razor pages and views for Blazor Applications**

 ## Blazor Server App support for IdentityServer Hybrid Flow
**This library replaces the LoginIDP and LogoutIDP pages from Kevin Dockx's pluralsight course:**\
[Authentication and Authorization in Blazor Applications](https://app.pluralsight.com/library/courses/authentication-authorization-blazor-applications)\
<br/> The LoginIDP and LogoutIDP views are used to support hybrid flow operations between the Blazor Server application and IdentityServer. The views do not contain User Interface design content. The users are redirected to IdentityServer to login there.\
This library allows you to use Kevin's design pattern without needing to create the LoginIDP and LogoutIDP pages for every one of your applications.

 ### LoginIDP.cshtml / LogIDP.cs
Invokes ChallengeAsync on the HttpContext to trigger the redirect to IdentityServer for User login

 ### LogoutIDP
Invokes SignOutAsync for both the Cookie and OpenIdConnect authentication schemes. 

### Demo
The [Demo](https://github.com/Tricklebyte/BlazorRazor/tree/master/demo) project is taken directly from Kevin's pluralsight course, with two changes:\
* Removed LoginIDP and LogoutIDP pages from the project
* Added Reference to BlazorRazor
