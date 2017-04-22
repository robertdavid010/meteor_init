# meteor_init

Base application and packages initialization for new [Meteor](https://www.meteor.com/) projects using [BlazeJS](http://blazejs.org/).

### TODO:
1. Review all packages for most current patterns and update, or replace as necessary
	1. Update to SimpleSchema2
	
These steps, and the accompanying configuration files, will set up a base MeteorJS app installation with the default BlazeJS renderer. This is a bare project, an empty app ready to accept boiler plate code.

### Steps to initialize MeteorJS App

**Create new Meteor project**

Navigate in your terminal to the directory where the new Meteor project is to be created and create a new project (examples for bash):

```bash
$ meteor create <project name> --bare
```

**Add .gitignore**

Download the handy Meteor .gitignore into the newly created project directory

```bash
$ cd <project name>
$ wget https://raw.githubusercontent.com/robertdavid010/meteor_init/master/.gitignore
```

**Adding minimum package base**

Add the necessary packages for the base application.

```bash
$ meteor add random check reactive-dict session less accounts-base accounts-password alanning:roles aldeed:collection2 aldeed:simple-schema aldeed:autoform aldeed:autoform-bs-datepicker aldeed:template-extension kadira:flow-router kadira:blaze-layout arillo:flow-router-helpers gwendall:body-events huttonr:bootstrap3 msavin:mongol
```


Packages included are those needed to:

* handle round trip CRUD for the application data model
* handle data validation 
* manage application state
* render views according to the application state
* provide basic UI libraries for views


[See more package details](../master/packages.md)

**Update Meteor**

Bring the project as up to date as possible with latest release of framework and packages.

```bash
$ meteor update
```
> **Note:** Watch for the terminal output/message after the update from Meteor, it may direct you on how to update packages not updated during the global update.
	There may be cetrain interdepencies with prevent every single package from being fully up to date. If after manually entering `meteor udate <package name>` results in an up to date result from the terminal, these packages are as up do date as they can be.

## Security Notice:

Security is of great importance when building software or services for public usage over the Internet. Make sure to be informed of the risks, and necessary measures.

[Meteor Security Checklist](https://meteorjs.club/MeteorSecurityChecklist.pdf?__s=qmhqtnitpz5xzsmztn8g)

The project is now ready for boilerplate code, or to begin coding from scratch.

**Have Fun!**
