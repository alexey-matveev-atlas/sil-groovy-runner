sil-groovy-runner

This is a plugin for Atlassian Jira Server.
It must be used with the SIL Engine installed.
The plugin executes groovy scripts within the SIL engine.
To use this plugin you should go to SIL manager, create a sil script and add the executeGroovyScript routine to your sil script.
Here is an example of a script:

logPrint("ERROR", executeGroovyScript("return 1"));

You can access the issue variable within your groovy script. The issue variable contains the reference to the issue, under which the script executes. 
To try the issue variable, go to the SIL manager, create a new sil script. Provide the context for the script to a Jira issue and run your script.
Here is an example of such a script:

logPrint("ERROR", executeGroovyScript("return issue.getKey()"));
