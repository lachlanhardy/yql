REQUIRED KEY: domain

You must pass the domain key to specify which public JIRA instance you are querying. This can be done by adding the following to your YQL query:

    AND domain="some-url"

eg: To access JAC, use: AND domain="jira.atlassian.com"

Therefore, an example query would be:

    use "http://github.com/lachlanhardy/yql/raw/7fc7b051e9c56fc176bc46597ed7e8d3ed135e17/jac.xml" as jactable; 
    select key.content FROM jactable WHERE pid=10240 AND fixfor=14531 AND domain="jira.atlassian.com"


