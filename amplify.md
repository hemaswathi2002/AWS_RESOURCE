WITHOUT CONFIGURING THE UNDERLYING INFRASTRUCTURE MANYALLY:
  Service used to build, host, deploy, manage web and mobile application 

=> Connect github repository => Configure Build settings => auto build and deploy applicationn if code pushed 


Frontend Hosting
CI/CD - automatically build and deploy code from connected repo
Global Delivery - amp. hosting uses managed delivery infra, including cloudfront 
Backend Integration - Connect to api's

EXAMPLE:

CODE => github => Amplify-build pipeline => managed hosting and cdn(cloudfront) => User

user opens your website.
The browser downloads the frontend files
When the user views products, the frontend sends an API request to your backend
The backend processes the request and queries RDS if necessary.
The API response returns to the browser, where React updates the page


COST ESTIMATION:

1. Build instance size - Standard — 8 GB RAM, 4 vCPUs
2. Number of build minutes
3. Data stored per month
4. Data served per month - each visit transfers * no of users = data of gb served
5. Number of SSR requests(Server-Side Rendering) 
(normal static React application generally does not need SSR; but a dynamically rendered Next.js application)
6. Duration of each request ( only if ssr used)
7. Web Application Firewall

Security: HTTPS, Cognito, IAM permissions, secrets handling, CORS and WAF.


https://github.com/iam-veeramalla/three-tier-architecture-demo/tree/master/web