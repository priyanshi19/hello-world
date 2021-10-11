### Requirement
Production validation is a daily process which needs to be performed just after batch cycle run gets completed. This daily health check process for each application was to be performed manually by the Production Support team which required manual effort and was time consuming.

### Scope and Impact
The Application Health-Check tool validates the online applications under BHF such as WMA, PPLUS, NBA and E-APP. This tool is a fully automated version of manual validation and report generation. It is fully automated, more efficient, less time consuming and effortless. 

### Approach
The Application Health-Check tool is built in using secure technologies, considering the privacy in check, and can be scheduled at a specific time to execute and generate the automated application health report. This tool is deployed and versioned on GITHUB and has been integrated via Jenkins.

### Solution
This application is designed to validate database connectivity, application login validation, CICS connectivity validation, contract search and screens navigation on a scheduled time. This automated Health-Check tool generates the consolidated reports for each application after the overall validation and distributed over email to the predefined configurable distribution list. This utility can also be triggered manually any time.

### Key Benefits

* 	 No manual intervention in performing HealthCheck of each application
* 	Generates consolidated reports of each application
* 	Can be Scheduled at a specific time
* 	Can be utilized spontaneously to check the Health of the application after any hotfixes or any new promotion
* 	Easy to configure and run
* 	Can also be run manually after the server patching or production deployment to make sure the applications are up and running.
* 	Any error that occurred while running the application can be identified in the consolidated report.

### Challenges
Initially we have used IE webdriver during the development phase but it was not supported when we deployed this application on the modal office server. So we have used phantomjs webdriver which executes in the background during the validation.
