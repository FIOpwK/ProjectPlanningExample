# We are creating an issue logger
https://docs.oracle.com/cd/E14373_01/appdev.32/e13363/issue_track_obj.htm#BABBHFAF

# User Stories
## Manager
-as a manager, I want to add a project_maintainer or contributor to an issue
-as a manager, I want to remove an assignee from an issue

## Viewer
-as a viewer, I want to search for an issue by Id
-as a viewer, I want to search for an issue by Desc
-as a viewer, I want to get notifications on issues I checkbox or like

## User
-as a user, I want to create an issue from my account
-as a user, I want to comment on an issue from my account

## Sys
-as the sys, I must track issues
-as the sys, I must prioritize tasks
-as the sys, I must manage (whatever assigned)


# Permissions
CREATE_ISSUE [create,read,update,close]
EDIT_ISSUE [read,update,close]
ADMIN_ISSUE [create,read,update,close]
VIEW_ISSUE [read]
SEARCH_ISSUE [read]



# Components
    - Issue_Number : to track the issue by Id (unique_int)

    - Issue_Status : to note if issue is open, in_progress, blocked, or done (string)

    - Issue_Desc : to detail what the issue is addressing (string)

    - Issue_Category : to categorize issues by product or issue type (string)

    - Issue_Priority : to prioritize the issue low,medium,high? (filter/string)

    - Issue_Assigned : to clarify ownership of the issue, team member, contributor (string)

    - Issue_By : to clarify who reported the issue, the author (string/email)

    - Issue_Date_Open : to time-frame which day the issue was identified (string/date)

    - Issue_Date_Closed : to help look when issue was resolved (string/date)

    - Issue_Date_Updated : to clarify when issue was last modified (string/date)

    - Issue_Comments : to note important information about the issue (string)


# Supported Languages # Supported Backend/DB
 - Python               Postgresql
 - NodeJS               MongoDB
 - Javascript           Postgresql
 - Java                 Postgresql/ODBC
 - C#                   MYSQL/SQL Server

 
# Choosen Languages (options in order of preference)
- Python (
    [https://www.psycopg.org/docs/install.html#running-the-test-suite],
    ['https://www.psycopg.org/psycopg3/docs/'],
)

    ```python
    conn = psycopg.connect("dbname=IssueTrackr user=postgres  port=5433 password=******")
    ```

- Javascript (***)
- Java (**)
- C# (**)


# Database Setup
here['https://app.dbdesigner.net/designer/schema/new']
 #for this project we will need to create threee db tables
 -Project : tracks all current projects
 -People : information about who can be assigned to handle issues
 -Issue : tracks all information about an issue, including related project, person assigned