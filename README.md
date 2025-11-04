**Establish Deployment-Pipeline for production mautic**

Steps: 

- Install gitlab runners to mautic b2b production and mautic b2c production

- Register each runner in gitlab (as shell executor) and use appropriate tags (mautic-production-b2b and mautic-production-b2c respectively)

- Create a .gitlab folder 

- Create separate yml configs for staging and production

- In the last step create production branch from master


Install gitlab runners to mautic b2b production and mautic b2c production  

`curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | bash`  

`apt-get install -y gitlab-runner`    

Register each runner in gitlab (as shell executor) and use appropriate tags (mautic-production-b2b and mautic-production-b2c respectively)  

Project mautic-base > Admin > Settings > CI/CD > Runners > Create project runner: mautic-production-b2b and mautic-production-b2c  

`gitlab-runner verify`  
`gitlab-runner list`

Create a .gitlab folder:  
`cd /var/www/mautic`  

`git fetch origin`  

`git checkout --no-track -b APPS-6817_Establish_Deployment-Pipeline_for_production_mautic origin/master`  

`mkdir -p /var/www/mautic/.gitlab` 

`git add -f .gitlab`  

