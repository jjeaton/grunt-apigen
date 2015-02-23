# grunt-apigen

> Grunt task for generating Apigen documentation.

This is my very first Grunt plugin, so proceed with caution. For more info about Apigen documentation library, check their website and GitHub repository: 

- http://www.apigen.org/
- https://github.com/apigen/


## Prerequisities

First, install Apigen. [Check Apigen website](http://www.apigen.org) for recommended ways how to do so.

Personally, I've installed Apigen by Composer globally. 

```
$ composer global require apigen/apigen
$ composer update
```

You also need to add path to your global Composer packages to your $PATH variable. 

```
PATH=~/.composer/vendor/bin:$PATH
```

You can check if Apigen is working for you regardless of your setup by:

```
$ apigen --version
```


## Getting started (Grunt)

This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```
$ npm install grunt-test --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```
grunt.loadNpmTasks('grunt-apigen');
```

### Options

For now, plugin supports only 2 options to mimic basic Apigen command:

```
apigen generate --source src --destination api
```

#### options.source
Type: `String`
Default value: `./`

Files to be documented. Current directory by default. Works recursively.

#### options.destination
Type: `String`
Default value: `./apigen-docs`

Destination of Apigen output.

## Release History

##### 0.1.0 

- Initial release.

##### 0.1.1

- Added an actual readme.
- Fixed bug with adding to command (instead of overwriting it).
- Deleted `test` directory.

## ToDo list

- Contact Apigen developers and (at least) fix terminal output, that is normally way nicer.
- Learn concept of unit testing to actually use them here.