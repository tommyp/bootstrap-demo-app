# Bootstrap demo app

This app is to demonstrate how to arrange bootstrap with SCSS files for maximum awesomeness

Have a look in application.css and see that I've removed require_tree, as that includes every file in the /stylesheets directory. This __isn't__ what we want, as it means different layouts are bit useless because all of our styles will be included in any different stylesheets. Instead, I require app.scss and inside that, collect all the different scss files in it.

You'll see that I've included a file for variables and for overrides in app.scss. This allows us to call any variable in any of the included SCSS files. Sprockets will pull the files into app.scss as SCSS, so all the variables can be called in any file before it's compiled to CSS and handed over to application.css. The same applies to functions and mixins.