# ADD FONT AWESOME ICONS TO YOUR ANGULAR PROJECT
These are the steps to implement Font Awesome icons inside an Angular project

## Commands

`ng new myApp --no-standalone` Generate a new angular project

`npm install xxx` Install additional packages to the project

## Process

To start the project, use `ng new myApp --no-standalone` for projects greater than 16 version of Angular

Install fontAwesome dependencies, use `npm i @fortawesome/angular-fontawesome @fortawesome/free-solid-svg-icons @fortawesome/free-regular-svg-icons @fortawesome/free-brands-svg-icons`

Open myApp/src/app/app.module.ts and paste the following code.:

```
import { FontAwesomeModule, FaIconLibrary } from '@fortawesome/angular-fontawesome';
import { fas } from '@fortawesome/free-solid-svg-icons';
import { far } from '@fortawesome/free-regular-svg-icons';
import { fab } from '@fortawesome/free-brands-svg-icons';

```

In the `@NgModule` paste `FontAwesomeModule`

In the `export class AppModule{}` add the following code.: 

```
constructor(library: FaIconLibrary) {
    library.addIconPacks(fas, far, fab);
    }
```

Your icons are ready


