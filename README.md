box-yeoman
=========

A box for building yeoman based projects. (includes: grunt, bower, phantomjs, karma)

In order to use the box you need to:

Add bower to your package.json

      "devDependencies": {
    "grunt": "~0.4.2",
    "bower": "~1.3.1" 
    ......

And add the next wercker.yml to your yeoman project:

    box: olger/box-yeoman
    build:
        steps:
            - wercker/npm-install
            - plasticine/bower-install
            - wercker/grunt:
                tasks: build
