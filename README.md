# Undocumented Internal API for Zephyr Scale Server

Use at your own risk. They're unsupported/undocumented internal API's which the web interface and backend use for operations.


**GET** Additional Test details: ```/jira/rest/tests/1.0/testcase/TestCaseKey```

**GET** Find all tests across all projects: ```/jira/rest/tests/1.0/testcase/search?```

**GET** Get any fields from a JSON response in test query: ```/jira/rest/tests/1.0/testcase/TESTKEY?fields=fieldDesired``` (ex. precondition, id, archived, objective, etc...) 

**GET** Search Test Cases with granularity: ```/jira/rest/tests/1.0/testcase/search?archived=false&fields=id,key,projectId,name,averageTime,estimatedTime,labels,folderId,componentId,statusId,priorityId,lastTestResultStatus(name,i18nKey,color),majorVersion,createdOn,createdBy,updatedOn,updatedBy,customFieldValues,owner&maxResults=40&query=testCase.projectId IN (PROJID) AND testCase.folderTreeId IN (FOLDERID) ORDER BY testCase.version DESC&sort=version:desc&startAt=0```

**GET** Project Details ```/jira/rest/tests/1.0/project```

**GET** JSON Report Output: ```/jira/rest/tests/1.0/reports/testresults/summary/testrun?displayUnit=COUNT&epicJQL=&jql=&period=MONTH&projectId=12300&scorecardOption=EXECUTION_RESULTS&tql=testResult.projectId IN (PROJECTID) AND testResult.executionDate >= '2022-04-20' AND testResult.executionDate <= '2022-04-20' AND testCase.onlyLastTestResult IS true&traceabilityCustomTreeDisplayOption=CONDENSED&traceabilityMatrixOption=COVERAGE_TEST_CASES&traceabilityReportOption=COVERAGE_TEST_CASES&traceabilityTreeOption=COVERAGE_TEST_CASES```

**POST** Create a Folder within a Run/Cycle: ```/jira/rest/tests/1.0/folder/testrun``` (raw JSON within body, ex: {"index":1,"name":"secretAPIfolder","projectId":100}

**POST** Archive a Test: ```/jira/rest/tests/1.0/testcase/bulk/unarchive``` (raw JSON with test ID within body ex. [100])

**DELETE** Delete an Archived Test: ```/jira/rest/tests/1.0/testcasedelete``` (raw JSON with test ID within body ex. [100])

**POST** Create Attachment: ```	/jira/rest/tests/1.0/testresult/TESTID/attachment```

**DELETE** Delete an attachment: ```/jira/rest/tests/1.0/attachment/ATTACHMENTID```
