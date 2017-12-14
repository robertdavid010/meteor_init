# meteor_init

This is a base application and packages initialization for new [Meteor](https://www.meteor.com/) projects using [BlazeJS](http://blazejs.org/).

These steps, and the accompanying configuration files, will set up a base MeteorJS app installation with the default BlazeJS renderer. This is a bare project, an empty app ready to accept boiler plate code.

## Steps to initialize MeteorJS App

### Create new Meteor project

Navigate in your terminal to the directory where the new Meteor project is to be created and create a new project (examples for bash):

```bash
meteor create <project name>
```
> Normal project creation is used as a handy way of adding some base npm files etc.

After the project is created, navigate into the new app directory

```bash
cd <project name>
```

### Add NPM packages

Adding some dependencies for meteor packages (listed independently for easy individual install).

```bash
meteor npm install --save bcrypt
meteor npm install --save simpl-schema
meteor npm install --save bootstrap@4.0.0-beta.2
```

### Add Meteor packages

Add the necessary packages for the base application.

```bash
meteor add random check reactive-dict session less accounts-base accounts-password alanning:roles aldeed:collection2-core aldeed:autoform aldeed:autoform-bs-datepicker aldeed:template-extension kadira:flow-router kadira:blaze-layout arillo:flow-router-helpers gwendall:body-events msavin:mongol twbs:bootstrap
```

Packages included are those needed to:

* handle round trip CRUD for the application data model
* handle data validation 
* manage application state
* render views according to the application state
* provide basic UI libraries for views

[See more package details](../master/packages.md)

## Security Notice:

This initialization of a base meteor app directory includes the packages 'insecure' and 'autopublish'. These **MUST** be removed before deploying software live.

Security is of great importance when building software or services for public usage over the Internet. Make sure to be informed of the risks, and necessary measures.

[Meteor Security Checklist](https://meteorjs.club/MeteorSecurityChecklist.pdf?__s=qmhqtnitpz5xzsmztn8g)

The project is now ready for boilerplate code, or to begin coding from scratch.

See the [meteor_boilerplate](https://github.com/robertdavid010/meteor_boilerplate) for a codebase boilerplate specifically developed to be deployed on top of this initialization process.

### Completion

**Have Fun!** Along with maybe a beer :)

**TODO:**
1. Review all packages for most current patterns and update, or replace as necessary
	1. ~~Update to SimpleSchema2~~
	1. ~~Update to support bootstrap 4 npm~~
	1. Add bootstrap/front-end dependencies to custom <head>
	1. Consider remove accounts packages (?)
1. Review package install order
