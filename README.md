# Postman API Automation Integration with Github Actions #

This respository is a demonstration for POC for integrating postman tests with github actions. The tests are writtern in postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger project execution on every push to main branch. You can also execute project manually using workflow_dispatch. The project runs on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from thr github page: https://sayalilm.github.io/Phoenix-Inwaaranty-Flow/

The latest report is mailed to the team members using GMAIL SMTP.


#Test Coverage#
1. Happy flow testing
2. Negative testing and edge case testing
3. Token testing
4. Data driven testing with csv
5. Schema Validation
6. Secrets management with Github Secrets


#  Tech Stack#
1. Postman
2. Node.js v22
3. Newman
4. Newman-Reporter-Hrmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner

# Github Pages#
You can directly view the latest report of the postman test at the Github Page Link:  https://sayalilm.github.io/Phoenix-Inwaaranty-Flow/


# HTML Report #
The report will be created in the newman folder
![Postman Report](https://github.com/Sayalilm/Phoenix-Inwaaranty-Flow/blob/static-content/newman-report-screenshot.png)

# Project Structure #


```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json   #Collection File
└─ QA.postman_environment.json  #Environment File

```


```
# How to run the project? #
You can run the project manually on your local system for that:
1. Clone the project on local system: https://github.com/Sayalilm/Phoenix-Inwaaranty-Flow.git
2. Install Nodejs and NPM: https://nodejs.org/en/download
3. Install Newman using npm install -g newman
4. Install Newman-Reporter-Htmlextra using command npm install -g newman-reporter-htmlextra
5. Run the newman command:

                 newman run 'Inwarranty-flow Collection.postman_collection.json' \
                -e 'QA.postman_environment.json' \
                -r cli,htmlextra \
                --reporter-htmlextra-export ./newman/index.html






