# meteor_init

Base app and packages initialization for new [Meteor](https://www.meteor.com/) projects using [BlazeJS](http://blazejs.org/).

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

**Add packages config**

Go to the Meteor application framework hidden directory. Replace the existing packages file with the meteor_init packages. This will install all the base packages minimally necessary to build a fully functioning prototype with production capability.

```bash
$ cd .meteor
$ rm packages
$ wget https://raw.githubusercontent.com/robertdavid010/meteor_init/master/packages
```

Packages included are those needed to:

* handle round trip CRUD for the application data model
* handle data validation 
* manage application state
* render views according to the application state
* provide basic UI libraries for views

**Update Meteor**

Bring the project as up to date as possible with latest release of framework and packages.

```bash
$ cd ../
$ meteor update
```

## Security Notice:

Security is of great importance when building software or services for public usage over the Internet. Make sure to be informed of the risks, and necessary measures.

[Meteor Security Checklist](https://meteorjs.club/MeteorSecurityChecklist.pdf?__s=qmhqtnitpz5xzsmztn8g)

The project is now ready for boilerplate code, or to begin coding from scratch.

**Have Fun!**
