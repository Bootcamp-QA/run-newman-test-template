# API Automated Testing with Postman CLI

This repository contains automated tests for for the JIRA API using Postman CLI. The tests are executed automatically every week.

### Test Results

The latest test results can be found in the latest GitHub Actions run. Click the link above to view the most recent execution and download the HTML report from the "Artifacts" section.


[Latest Run](https://github.com/bootcamp-qa/postman-run/actions)


### Test Scenarios
The tests cover the following API operations:

- **GET**: Retrieve comments associated with a specific issue.
- **POST**: Add new comments to an issue.
- **PUT**: Update existing comments.
- **DELETE**: Remove comments from an issue.

The tests verify both positive scenarios and error handling, including:

- **Positive Cases**: 
  - Successfully retrieving, adding, updating, and deleting comments.
- **Error Handling**: 
  - Testing responses for invalid inputs and verifying appropriate error codes.
- **Authentication**: 
  - Validating authentication mechanisms and checking responses for unauthorized access.
 
### Local Execution Steps

To run the tests locally using Postman, follow these steps:

1. **Import the Postman Collection**:
   - Download the Postman collection from the latest GitHub Actions run artifacts.
   - Open Postman and go to **File > Import**.
   - Select the downloaded `collection.json` file and import it.
   

2. **Create Environment Variables**:
  - Make sure you have a JIRA account and create a ticket with at least one comment.
   - **JIRA_URL**: Your JIRA instance URL (e.g., `https://your-jira-instance.atlassian.net`).
   - **JIRA_ISSUEID**: The ID of the JIRA ticket you created.
   - **JIRA_COMMENTID**: The ID of the comment you added to the JIRA ticket.
   - **USER**: Your JIRA username (email).
   - **TOKEN**: Your JIRA API token.


3. **Run the Collection**:
   - In Postman, select the imported collection and click on the **Run** button to execute the tests.


