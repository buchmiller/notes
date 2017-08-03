# Angular 2 with Firebase

1. Initialize a new project using [Angular CLI](https://cli.angular.io/)

1. Create a new firebase project
    - Click "Add Firebase to your web app" and note down the config values. These will be used in the next step.

1. Follow the instructions for angularfire2 [installation and setup](https://github.com/angular/angularfire2/blob/master/docs/1-install-and-setup.md)
    - Not all of the steps seem to be required
    - It's probably better to create a service to communicate with firebase instead of using the primary app module.
