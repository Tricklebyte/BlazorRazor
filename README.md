# BlazorRazor 
**Reusable Razor pages and views for Blazor Applications**

 ## Blazor Server App support for IdentityServer Hybrid Flow
**This library replaces the LoginIDP and LogoutIDP pages from Kevin Dockx's pluralsight video:**\
[Authentication and Authorization in Blazor Applications](https://app.pluralsight.com/library/courses/authentication-authorization-blazor-applications)\
<br/> The LoginIDP and LogoutIDP views only support hybrid flow operations between the Blazor Server application and IdentityServer. The views do not contain User Interface design content. The users are redirected to IdentityServer to login there.\
This library allows you to use Kevin's design pattern without needing to create LoginIDP and LogoutIDP pages for every individual Blazor server application 

 ### LoginIDP.cshtml / LogIDP.cs
Invokes ChallengeAsync on the HttpContext to trigger the redirect to IdentityServer for User login

 ### LogoutIDP
Invokes SignOutAsync for both the Cookie and OpenIdConnect authentication schemes. 

