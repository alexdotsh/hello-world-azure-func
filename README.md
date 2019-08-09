####
Azure pipeline and function demo using Python

| Requirements    | Task          | Current Status | Finished | 
|-----------------|---------------|----------------|----------|
|Create a simple ‘Hello World’ Python app can be Dockerised) that will be run as an Azure Function | Simple Python App | Done | <ul><li>[x]</li></ul>
|During the build phase run one example of code testing or scanning, for example: Secrets scanning: using TruffleHog on the code repo for your Python app OR Quality scanning: create a SonarQube server using this ARM template & scan your code during the build | Setup and configure SonarQube server | Done | <ul><li>[x]</li></ul>
|Demonstrate both pass and fail scenarios in the build history if possible| | Done | <ul><li>[x]</li></ul>
|Create a release pipeline that deploys your Python app as an Azure Function| Setup a Azure function resource and task to deploy | Done | <ul><li>[x]</li></ul>
|This should be a multi-stage (multi-environment) release pipeline with stages that reflect a realistic route-to-live Each environment’s release stage can be very simple and need only perform an Azure Function deployment The pipeline should also, however, aim to demonstrate relevant examples in some, or all, of the following areas. | Multi stage deployments | Done | <ul><li>[x]</li></ul>
|Use of pre- and post-deployment conditions| Add pre- and post-deployment conditions | Done | <ul><li>[x]</li></ul>
|Your deployed Azure function should result in a response from a testable endpoint| See table for results | Done | <ul><li>[x]</li></ul>

Azure Devops project can be founh here:
https://dev.azure.com/alexmirkhaydarov/alex-mirkhaydarov-demo

Main pipeline can be found here:
Deployments
https://dev.azure.com/alexmirkhaydarov/alex-mirkhaydarov-demo/_build?definitionId=9

Relase pipeline can be found here:
https://dev.azure.com/alexmirkhaydarov/alex-mirkhaydarov-demo/_release?view=mine&definitionId=2

PR changes pipeline is mainly used for PR changes as the name indicates.
https://dev.azure.com/alexmirkhaydarov/alex-mirkhaydarov-demo/_build?definitionId=10
https://dev.azure.com/alexmirkhaydarov/alex-mirkhaydarov-demo/_release?view=mine&definitionId=3

Testable endpoints

DEV:  https://dev-hello-world-func.azurewebsites.net/api/HelloWorld?name=World
TEST: https://test-hello-world-func.azurewebsites.net/api/HelloWorld?name=World
RTL:  https://rtl-hello-world-func.azurewebsites.net/api/HelloWorld?name=World
PROD: https://prod-hello-world-func.azurewebsites.net/api/HelloWorld?name=World

SonarQube Analysis report: https://sonarqube-azureappservicee389.azurewebsites.net/dashboard?id=HelloWorldPythonApp
