# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects runs on a scheduled time with the help of the Cron Job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with they can view the report directly from the github page : https://abhishekhunachagi.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi My Name is Abhishek Hunachagi. I have 5 years of experience in Automation Testing and Devops. My Skillset Include UI Automation with Selenium Webdriver, Cypress, 
Playwright and API Testing I use Rest Assured and Postman. You can connect with me over : [Linked In](https://www.linkedin.com/in/abhishek-hunachagi-a760a921b/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node.Js 22v
3. Newman
4. Newman- Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. CSV for Data Driven Testing
8. AWS-EC2 instances for Self Hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github Page Link : https://abhishekhunachagi.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://raw.githubusercontent.com/abhishekhunachagi/Phoenix-Inwarranty-Flow/static-content/Newman-Report.png)

## Project Structure ##
```
Phoenix Inwarranty flow
├─ Inwarranty-flow Collection.postman_collection.json
├─ QA.postman_environment.json
└─ testdata.csv
```
## How to run the Project ##
You can run the project on your local system for that:
1. Clone the project on Local System : ``` https://github.com/abhishekhunachagi/Phoenix-Inwarranty-Flow.git ```
2. Install Nodejs and NPM from ``` https://nodejs.org/en ```
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman Command:
 ```
                 newman run 'Inwarranty-flow Collection.postman_collection.json' \
              -e QA.postman_environment.json \
              -d testdata.csv \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
```

