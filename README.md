box-yeoman
=========

A box for building yeoman based projects. (includes: grunt, bower, phantomjs, karma)

In order to use the box you need to:

Add the next wercker.yml to your yeoman project:

    box: olger/box-yeoman
    build:
        steps:
            - wercker/npm-install
            - plasticine/bower-install
            - wercker/grunt:
                tasks: build

for a simple build.
