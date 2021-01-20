# Setup containers for Development Server by hosting a bunch of services

Setup containers for the following

I took my development server, which previously hosted a bunch of services as native apps, and containerized everything. So, I wound up with containers for:
-Jira
-Confluence
-MySQL
-Tomcat
-Gitlab
-Nexus
-Jenkins
-Redis
-Mongo
-Apache
-Nginx

I have everything volume-mapped, and then those data directories get sync'd hourly to my main file server where I have a backup mechanism set up. 
That way, if the dev server ever goes down hard, I can rebuild quickly and easily
I built scripts as I did the work so it's a simple matter of running the scripts on a bare server if/when the time comes.

Next steps: Set up Jenkins job to occasionally grab latest OS minor version, run your scripts, and make sure everything restores correctly from backups
