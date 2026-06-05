06/05/2026
## The Target
The application is shopify. An e-commerce platform where developers sell or create apps.The app secion seems to be a subdomain of the applicaiton where developers manage their apps.
The reporter finds the bug in url of photo preview.

## My Recon Approach
what I'd do first is click everything and familiarize the platform. Then i would open an app or my account details while examining weather the id appears in the URL so if then i can try to change it to access someone else's.

## The Vulnerability Class
Broken access control

## My Testing Steps
1.Create two shopify accounts one for testing another as victim
2.Add a private image 
3.See if an id parameter appears in URL
4.Change it into victim's image's id
5.View the photo and observe that IDOR vulnerability as been exposed

## Why I Would Have Caught It
This is basic IDOR and many hunters tend to think that most program applications have authorization checks but most do not.

## What I Learned for My Hunting
It is possible to find valid bugs because most of platforms and even popular ones like shopify can miss these basic bugs. 
I will always seek to change the value of id once i see one
