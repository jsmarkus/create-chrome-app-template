This web project has the following setup:

* www/ - the web assets for the project
    * index.html - the entry point into the app.
    * js/
        * app.js - the top-level config script used by index.html
        * app/ - the directory to store project-specific scripts.
        * lib/ - the directory to hold third party scripts.
* tools/ - the build tools to optimize the project.

To optimize, run:

    volo build

This will run the "build" command in the volofile that is in this directory.

That build command creates an optimized version of the project in a
**www-built** directory. The js/app.js file will be optimized to include
all of its dependencies.

To build google chrome's `.crx` file, run:

    volo crx

This will. run "crx" command in volofile and create file `application.crx`. Also `application.pem` will be created first time, and used then.

*NOTE: In Chrome 24 you can only install crx-extension by dragging it onto chrome://extension page from your desktop.*


For more information on the optimizer:
http://requirejs.org/docs/optimization.html

For more information on using requirejs:
http://requirejs.org/docs/api.html
