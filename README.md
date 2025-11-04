**Establish Deployment-Pipeline for production mautic**

Steps: 

Install gitlab runners to mautic b2b production and mautic b2c production
Register each runner in gitlab (as shell executor) and use appropriate tags (mautic-production-b2b and mautic-production-b2c respectively)
Create a .gitlab folder 
Create separate yml configs for staging and production
In the last step create production branch from master
