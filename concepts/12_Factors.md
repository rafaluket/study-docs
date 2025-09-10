# Introduction
It's a methodology for building SAAS apps that:
- Use declarative formats for setup automation;
- Have a clean contract with the underlying operating system;
- Are suitable for deployment cloud platforms;
- Minimize divergence between dev and prod; 
- Scale up without big(significant) changes;

This methodology can be applied to any programming language.

# The Twelve Factors
1. Codebase\
One codebase tracked in revision control, many deploys from many users (the development environment is your own machine, most time)

2. Dependencies\
Explicitly declare and isolate dependencies. In java we use maven (pom.xml) or gradle (build.gradle) files _(and never forget to add the "node_modules" or other dependencies folder to your .gitignore, this affects the users of the first item of this list)_

3. Config\
Store config in the environment _(also add the .env file to .gitignore please...)_. ATT: the configs in code, like used in spring code modules connection, doesn't count.

4. Backing services\
Treat backing services as attached resources like S3, MYSQL database, Metric apps, or google maps. Just with a simple link for independent configuration outside your code.

5. Build, release, run\
Strictly separate build and run stages, in the twelve factors a code never can be changed in the execution time and every version need to be unique

6. Processes
Execute the app as one or more stateless processes, just use the datastore cache with Redis or Memcached, but never persisted.

7. Port binding\
Export services via port binding (dont depend the web server to run your app, he need to be self-sufficient)

8. Concurrency\
Scale out via the process model

9. Disposability\
Maximize robustness with fast startup and graceful shutdown (your startup need to be a single line of code, or less...)

10. Dev/prod parity\
Keep development, staging, and production as smiliar as possible

11. Logs\
Treat logs as event streams

12. Admin processes\
Run admin/management tasks as one-off processes



