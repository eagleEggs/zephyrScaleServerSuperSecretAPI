# Undocumented Internal API for Zephyr Scale Server

Use at your own risk. They're unsupported/undocumented internal API's which the web interface and backend use for operations.


**GET** Additional Test details: ```/jira/rest/tests/1.0/testcase/TestCaseID```


**GET** Find all tests across all projects: ```**/jira/rest/tests/1.0/testcase/search?**```

**POST** Archive a Test: ```/jira/rest/tests/1.0/testcase/bulk/unarchive``` (raw JSON with test ID within body ex. [100])

**POST** Create a Folder within a Run/Cycle: ```/jira/rest/tests/1.0/folder/testrun``` (raw JSON within body, ex: {"index":1,"name":"secretAPIfolder","projectId":100}

**DELETE** Delete an Archived Test: ```/jira/rest/tests/1.0/testcasedelete``` (raw JSON with test ID within body ex. [100])

**GET** Search Users: ```/jira/rest/api/2/user?key=JIRAUSER20000``` (Or by username)
