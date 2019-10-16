# AngularFundamentals

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.9.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## To Install Node.js and NPM

Node.js - commonly referred to as Node - is a JavaScript runtime that allows you to run JavaScript on your computer without using a browser. This is the technology that enables JavaScript based application servers, including the one used by Angular.

Node also includes a package manager for installing 3rd party modules within their environment called Node Package Manager, or NPM.

### Mac OS X

1. If you do not have XCode installed, install it from the Apple App Store.

2. If you do not already have Homebrew installed, you will need to install it. Homebrew is a package manager specifically for OS X - you can find more about it on the Homebrew Website. To install it you run the following command in your terminal.

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

3. With Homebrew installed, installing Node and NPM is easy. Just run the following:
brew install node

4. Follow the messages in the terminal to install Node.

## Install TypeScript

The last prerequisite needed before installing the Angular CLI.

For Mac and Linux users you need sudo rights to install TypeScript, so type:

`sudo npm install typescript -g`

The -g flag tells NPM to install TypeScript as a global module, instead of to the directory your terminal is currently pointed it. This will enable you to be able to use the tsc command to compile TypeScript directly, and enable the Angular CLI to be able to use it.

Now that we have installed TypeScript, next we will install the Angular CLI.

## Install the Angular CLI

The Angular Command Line Interface is an optional component for Angular development that offers a series of generators and commands to make developing in Angular simpler and faster.

With the Angular CLI, you can create a scaffold for your app, generate components, modules, and also perform build tasks such as linting your code, serving your app locally, preparing your files for production usage, and using Angular's Ahead of Time compilation to optimize the performance of your app in production environments.

Let's go ahead and use NPM to install the Angular CLI on your machine.

For Mac and Linux users you need sudo rights to install the Angular CLI, so type:

`sudo npm install @angular/cli -g`

Now we have everything installed to start creating our Angular app. 


## Generate an Application Scaffold using the Angular CLI

Now that we have the Angular CLI installed, we are going to use it to create a scaffold for our application. The term “Scaffold” refers to the process of generating a generic template of an application based on the standards of how an Angular application should be constructed. A basic folder hierarchy is created following layout and naming best-practices. The folders are then populated with the components necessary to create a basic Angular application. Creating a scaffold sets up the basic files and architecture required for your app to run, and gives you a good pattern to follow. Using the Angular CLI to build your scaffold also gives you a variety of useful tools, including:

* Linting
* Unit testing with Karma
* End to End testing with Protractor
* Ahead of Time Compilation
* A built in local server

Let's go ahead and instantiate a scaffold with the Angular CLI.

1. First we need a name for our application. It needs to be alphanumeric (excepting that it can use dash characters), but the dashes must be immediately succeeded by a letter. For this application we are going to call it angular-fundamentals.

2. Open your command prompt and navigate to the directory you want to generate your app in. Note that the CLI will generate a subdirectory with the name angular-fundamentals within that directory.

3. Type the following to instantiate your application.

`ng new angular-fundamentals`

## To Generate a Module using the Angular CLI


Now that we have our app generated using the Angular CLI, we're going to use the Angular CLI's generator feature to generate a module. Using the built in generator command in the Angular CLI allows you to create components of your application easily without having to worry about properly including the code in your application. The Angular CLI generates the files in the appropriate format and modifies your files to include the newly generated component properly. Some of the different generators that the Angular CLI can run are:

* Modules `ng g module my-module`
* Components `ng g component my-component`
* Directives `ng g directive my-directive`
* Pipes `ng g pipe my-pipe`
* Services `ng g service my-service`
* Classes `ng g class my-class`
* Guards `ng g guard my-guard`
* Interfaces `ng g interface my-interface`
* Enums `ng g enum my-enum`


Open your command prompt or terminal and navigate to your angular-fundamentals directory.

Run the following command:

`ng g module first-module`

Note that `first-module` is the name of the module you are creating.

## To Use the Angular CLI to Run your App Locally

One of the most useful features about using the Angular CLI is the ability to serve your app locally in order to test it in real time. Serving your app compiles your modules for use and runs a server on your computer. You can then access the app via a browser. In addition, the Angular CLI will listen to changes to your files and recompile your app, meaning you can edit code, and then immediately see the changes in your browser.

Let's serve the app we made now.

1. Open your command prompt and navigate to the angular-fundamentals app.

2. Type the following:

`ng serve`

3. Open up a browser and navigate to `http://localhost:4200`. 

## Angular Modules

A module, in Angular, is a class file that helps you to organize all the different “pieces” of your application. it allows you to organize these pieces into blocks.

Angular modules also allow you to extend your application's capabilities through external libraries. Recall, again, the code from Module 1. The two import statements brought in two Angular modules, core and common. Your application is extended by the use of these two modules, which means your application gains the functionality found in those modules, without you needing to write code to implement that same functionality.

You can also export your module for use in other applications. The export class FirstModuleModule {} line in the previous lab code, means that your module is exportable and can be imported into some other Angular application.

Using Angular modules, you can break your application into multiple components, making your application easier to update and maintain.

Every Angular application has at least one module known as the root module. The root module is bootstrapped to load the application. By convention, this root module is called AppModule and you will find it in the file app.module.ts. It is located in the `src/app` folder. Note the export statement at the end. It indicates the module's name, AppModule.

## Module Syntax

Angular modules consist of a discrete set of attributes that you use to describe the module. These are listed here:

* declarations - these are the list of components, directives, and pipes that are a part of the specific module you are creating. Everything in a declaration is visible to application using this module, without requiring any explicit exports.
* imports - using import statements, you can make other modules visible within this module. Importing other modules is not an implicit export of those other modules, meaning simply, if another developer imports your module, they may not be able to see the modules you have imported.
* exports - this is the list or any declarations that you want to be made available (visible) to other modules that may import this module.
* providers - used to list providers for configuring the injector, when this module is imported by other modules.
* entryComponents - constitutes a list of components about which ComponentFactory should be generated. Primarily used for dynamically loading components.


## Using Dependency Injection

In our lab scenario, we will be creating an interface to some data that will come from GitHub. We are building a GitHub search component for the lab. This interface will be used in a service and that service will become an injectable component available for use in other components.

You will inject that service into your application module and use it to access the functionality of the Git search. In this way, our service is a stand-alone, testable, and reusable component but not only that, we don't need to worry about instantiating it in our client code. Angular takes care of this for us automatically. An added benefit is that the service may contain data that becomes shareable among all components that inject it. It is a singleton.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/7da9a2325f95b8b976a5769e860d908e/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/dependency_injection.png)

## HttpClient

When we consider communication between front-end clients and back-end services using the HTTP protocol, we note that modern browsers will use either XMLHttpRequest or the fetch() API. The HttpClient is an asynchronous HTTP library built into Angular, replacing other methods such as XMLHttpRequest, jQuery's $.ajax() or the more modern fetch.

Angular 4.3 and above make use of the HttpClient library as a mechanism to handle http requests in your Angular application. This is the replacement for the Http library that was used in AngularJS. HttpClient is available as an injectable class.

The HttpClient in Angular, provides a simplified mechanism for accessing HTTP functionality in your client applications. It supports testability, strongly typed request and response object, and better error handling.

Before you can use the HttpClient in your Angular application, you have to import the HttpClientModule.

```javascript
import {HttpClientModule} from '@angular/common/http';

@NgModule({
    imports: [
        BrowserModule,
        HttpClientModule,
    ],
})
```

Once you have imported the module, you can make use of it in your own component. Bellow you can see that we are using injection to bring the HttpClient functionality into the service we are creating.

```javascript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';
import 'rxjs/add/operator/toPromise';

@Injectable()
export class GitSearchService {
  cachedValues: Array<{
    [query: string]: GitSearch
  }> = [];
  private http: HttpClient
  constructor(http: HttpClient) {
      this.http = http
  }
```

The important aspects to note are that the HtstpClient is imported at the top of the file and then, within the @Injectable portion, we use the constructor to create an instance of the component for use in our application.

## Introduction to Services

Services are a type of component in Angular that are specifically designed to create reusable logic that can be injected into multiple components. This makes them ideally suited for the task of compartmentalizing API interactions, and so that is their most common use case.

When you use a service to hold your API interactions, you can easily add additional features to your API methods such as caching, and allow your components to subscribe to a single instance of an API call, preventing unnecessary trips to the server.

A common usage scenario for a service in Angular is to fetch data from a data source. This could be a database running on a server somewhere, or it could be any other form of data that you Angular application needs. 

The very first thing you do, after designing your service, is to create one using the Angular CLI. This is accomplished with a simple command:

`ng generate service service_name`

This single command use the Angular CLI, calls the generate command to generate a service and gives it a name of service_name. You should, of course, ensure that you are using descriptive names for your services.

This will generate a file called `service_name.service.ts` in the `src/app` folder of your project.

If you open that folder, you should see the following:

```javascript
import { Injectable } from '@angular/core';

@Injectable()
export class service_nameService {

  constructor() { }

}
```

Notice that our service imports Injectable from `@angular/core`, which allows this service to be injectable into other components. Recall that we want our service to be usable by other components and the Angular pattern recommendations is to make the services injectable so they can be used across components, share data, and be a singleton for instantiation when a component needs their functionality.

## Using Service

Once you have a service created, and it is an injectable component, you can make use of it in your components. One way to do this is to add it to the **providers:** section in your component, as shown here:

```javascript
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [service_name],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Note that this code segment is not complete as we are missing the imports but the it is intended to show where we would place our service so that the Angular framework will inject it into our component.

You will also need to ensure that the service is imported in the app module as well. This will be covered in the tutorial labs where you will create a search service, inject it into your components, and then utilize in the application, to return data from a web site.

## Tutorial Labs

1. *Creating Interfaces*

In this lab, you will learn how to create interfaces in TypeScript to define the output coming from the API in a type-safe fashion. You will then use the interface to define the output coming from the GitHub Search API.

2. *Creating Services*

In this lab, you will generate a Service to encapsulate your API interactions and in a way that Dependency Injection can make the service available through the app. You will also import the interface that was created in the last labs. You will also create a method that uses a simple caching strategy and will form the basis for retrieving data.

3. *Using HttpClient*

In this lab, you will extend the service created in the previous lab to use HttpClient. You will learn how to use promises instead of observables and will retrieve data from the GitHub API.

## To Retrieve Sample Data

Working with APIs is a quintessential part of modern Web application development. In Angular, there is a well-defined workflow for dealing with API interaction that leverages Angular, TypeScript, and your choice of either using Promises or a newer system called Reactive-X, also known as RxJS Observables. With all of these tools, you can communicate with APIs in your application easily and reliably. 

This first lab involves using TypeScript to create an Interface - basically a description of the types of data that an object will contain. In this case, we will be using an Interface to give us a predictable shape for the output of the GitHub Search API. When you use TypeScript in your app, it will allow you to safely identify the parameters of the data object as you are working with it in your application, giving you a firm foundation for building views off of an API call.

Note: You won't always need to create an interface by hand. Many APIs have libraries available that include the type definitions (or interfaces) for the API calls.

In order to do this, first we are going to need to retrieve an example of the data we are trying to call.

1. Open up your web browser.

2. Navigate to the following link in your browser. https://api.github.com/search/repositories?q=topic:angular Note that this is a direct search API call in link form. If you want to learn more about the GitHub Search API, you can visit this link

3. Notice the JSON output in the browser. You're going to want to copy the first entry in the “Items” array, as well as the initial first couple of fields in the output. 

4. Open up Visual Studio Code and paste that into a new file. Then, delete the comma at the end of the last line, and close the array and object with a closing square bracket ] and a closing curly bracket }. When you're finished, you should have this:

```json
{
  "total_count": 5867,
  "incomplete_results": false,
  "items": [
    {
      "id": 12256376,
      "name": "ionic",
      "full_name": "ionic-team/ionic",
      "owner": {
        "login": "ionic-team",
        "id": 3171503,
        "avatar_url": "https://avatars0.githubusercontent.com/u/3171503?v=4",
        "gravatar_id": "",
        "url": "https://api.github.com/users/ionic-team",
        "html_url": "https://github.com/ionic-team",
        "followers_url": "https://api.github.com/users/ionic-team/followers",
        "following_url": "https://api.github.com/users/ionic-team/following{/other_user}",
        "gists_url": "https://api.github.com/users/ionic-team/gists{/gist_id}",
        "starred_url": "https://api.github.com/users/ionic-team/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/ionic-team/subscriptions",
        "organizations_url": "https://api.github.com/users/ionic-team/orgs",
        "repos_url": "https://api.github.com/users/ionic-team/repos",
        "events_url": "https://api.github.com/users/ionic-team/events{/privacy}",
        "received_events_url": "https://api.github.com/users/ionic-team/received_events",
        "type": "Organization",
        "site_admin": false
      },
      "private": false,
      "html_url": "https://github.com/ionic-team/ionic",
      "description": "Build amazing native and progressive web apps with open web technologies. One app running on everything ",
      "fork": false,
      "url": "https://api.github.com/repos/ionic-team/ionic",
      "forks_url": "https://api.github.com/repos/ionic-team/ionic/forks",
      "keys_url": "https://api.github.com/repos/ionic-team/ionic/keys{/key_id}",
      "collaborators_url": "https://api.github.com/repos/ionic-team/ionic/collaborators{/collaborator}",
      "teams_url": "https://api.github.com/repos/ionic-team/ionic/teams",
      "hooks_url": "https://api.github.com/repos/ionic-team/ionic/hooks",
      "issue_events_url": "https://api.github.com/repos/ionic-team/ionic/issues/events{/number}",
      "events_url": "https://api.github.com/repos/ionic-team/ionic/events",
      "assignees_url": "https://api.github.com/repos/ionic-team/ionic/assignees{/user}",
      "branches_url": "https://api.github.com/repos/ionic-team/ionic/branches{/branch}",
      "tags_url": "https://api.github.com/repos/ionic-team/ionic/tags",
      "blobs_url": "https://api.github.com/repos/ionic-team/ionic/git/blobs{/sha}",
      "git_tags_url": "https://api.github.com/repos/ionic-team/ionic/git/tags{/sha}",
      "git_refs_url": "https://api.github.com/repos/ionic-team/ionic/git/refs{/sha}",
      "trees_url": "https://api.github.com/repos/ionic-team/ionic/git/trees{/sha}",
      "statuses_url": "https://api.github.com/repos/ionic-team/ionic/statuses/{sha}",
      "languages_url": "https://api.github.com/repos/ionic-team/ionic/languages",
      "stargazers_url": "https://api.github.com/repos/ionic-team/ionic/stargazers",
      "contributors_url": "https://api.github.com/repos/ionic-team/ionic/contributors",
      "subscribers_url": "https://api.github.com/repos/ionic-team/ionic/subscribers",
      "subscription_url": "https://api.github.com/repos/ionic-team/ionic/subscription",
      "commits_url": "https://api.github.com/repos/ionic-team/ionic/commits{/sha}",
      "git_commits_url": "https://api.github.com/repos/ionic-team/ionic/git/commits{/sha}",
      "comments_url": "https://api.github.com/repos/ionic-team/ionic/comments{/number}",
      "issue_comment_url": "https://api.github.com/repos/ionic-team/ionic/issues/comments{/number}",
      "contents_url": "https://api.github.com/repos/ionic-team/ionic/contents/{+path}",
      "compare_url": "https://api.github.com/repos/ionic-team/ionic/compare/{base}...{head}",
      "merges_url": "https://api.github.com/repos/ionic-team/ionic/merges",
      "archive_url": "https://api.github.com/repos/ionic-team/ionic/{archive_format}{/ref}",
      "downloads_url": "https://api.github.com/repos/ionic-team/ionic/downloads",
      "issues_url": "https://api.github.com/repos/ionic-team/ionic/issues{/number}",
      "pulls_url": "https://api.github.com/repos/ionic-team/ionic/pulls{/number}",
      "milestones_url": "https://api.github.com/repos/ionic-team/ionic/milestones{/number}",
      "notifications_url": "https://api.github.com/repos/ionic-team/ionic/notifications{?since,all,participating}",
      "labels_url": "https://api.github.com/repos/ionic-team/ionic/labels{/name}",
      "releases_url": "https://api.github.com/repos/ionic-team/ionic/releases{/id}",
      "deployments_url": "https://api.github.com/repos/ionic-team/ionic/deployments",
      "created_at": "2013-08-20T23:06:02Z",
      "updated_at": "2017-09-09T16:36:34Z",
      "pushed_at": "2017-09-08T17:43:01Z",
      "git_url": "git://github.com/ionic-team/ionic.git",
      "ssh_url": "git@github.com:ionic-team/ionic.git",
      "clone_url": "https://github.com/ionic-team/ionic.git",
      "svn_url": "https://github.com/ionic-team/ionic",
      "homepage": "https://ionicframework.com/",
      "size": 74842,
      "stargazers_count": 31203,
      "watchers_count": 31203,
      "language": "TypeScript",
      "has_issues": true,
      "has_projects": true,
      "has_downloads": true,
      "has_wiki": false,
      "has_pages": false,
      "forks_count": 8762,
      "mirror_url": null,
      "open_issues_count": 960,
      "forks": 8762,
      "open_issues": 960,
      "watchers": 31203,
      "default_branch": "master",
      "score": 4.7591105
    }
  ]
}
```

4. Save this file as `angular-fundamentals/src/app/git-search.json.`

## To Generate an Interface

Now that we have a bit of example JSON output from the GitHub Search API, we are going to use it to create a TypeScript Interface for our application. TypeScript interfaces describe the shape of a data object, including the types of all of its parameters. This is particularly useful because it gives your application (including the IntelliSense feature in Visual Studio Code) a template for the expected output types of the object to follow, allowing for auto-complete suggestions and code analysis on the object you are expecting to receive from the API.

Let's get our interface set up now.

1. Open up your command prompt or terminal.

2. Navigate to your angular-fundamentals folder.

3. Type the following: `ng generate interface git-search`

4. This will generate the interface file in your `angular-fundamentals/src/app` directory. Navigate to that directory in your file explorer.

5. Open the git-search.ts file in Visual Studio Code. This is a template for a TypeScript interface. You can see that the proper syntax for exporting the interface export interface GitSearch is already in the code. All we need to do now is fill it with the sample data before we can turn it into an actual interface.

6. Open the `git-search.json` file you had saved in the previous lesson.

7. Copy the inner contents of the first pair of curly braces.

8. Paste it in between the curly braces of your `git-search.ts` file. You should now have something that looks like this:

```typescript
export interface GitSearch {
  "total_count": 282772,
  "incomplete_results": false,
  "items": [
    {
      "id": 24195339,
      "name": "angular",
      "full_name": "angular/angular",
      "owner": {
        "login": "angular",
        "id": 139426,
        "avatar_url": "https://avatars3.githubusercontent.com/u/139426?v=4",
        "gravatar_id": "",
        "url": "https://api.github.com/users/angular",
        "html_url": "https://github.com/angular",
        "followers_url": "https://api.github.com/users/angular/followers",
        "following_url": "https://api.github.com/users/angular/following{/other_user}",
        "gists_url": "https://api.github.com/users/angular/gists{/gist_id}",
        "starred_url": "https://api.github.com/users/angular/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/angular/subscriptions",
        "organizations_url": "https://api.github.com/users/angular/orgs",
        "repos_url": "https://api.github.com/users/angular/repos",
        "events_url": "https://api.github.com/users/angular/events{/privacy}",
        "received_events_url": "https://api.github.com/users/angular/received_events",
        "type": "Organization",
        "site_admin": false
      },
      "private": false,
      "html_url": "https://github.com/angular/angular",
      "description": "One framework. Mobile & desktop.",
      "fork": false,
      "url": "https://api.github.com/repos/angular/angular",
      "forks_url": "https://api.github.com/repos/angular/angular/forks",
      "keys_url": "https://api.github.com/repos/angular/angular/keys{/key_id}",
      "collaborators_url": "https://api.github.com/repos/angular/angular/collaborators{/collaborator}",
      "teams_url": "https://api.github.com/repos/angular/angular/teams",
      "hooks_url": "https://api.github.com/repos/angular/angular/hooks",
      "issue_events_url": "https://api.github.com/repos/angular/angular/issues/events{/number}",
      "events_url": "https://api.github.com/repos/angular/angular/events",
      "assignees_url": "https://api.github.com/repos/angular/angular/assignees{/user}",
      "branches_url": "https://api.github.com/repos/angular/angular/branches{/branch}",
      "tags_url": "https://api.github.com/repos/angular/angular/tags",
      "blobs_url": "https://api.github.com/repos/angular/angular/git/blobs{/sha}",
      "git_tags_url": "https://api.github.com/repos/angular/angular/git/tags{/sha}",
      "git_refs_url": "https://api.github.com/repos/angular/angular/git/refs{/sha}",
      "trees_url": "https://api.github.com/repos/angular/angular/git/trees{/sha}",
      "statuses_url": "https://api.github.com/repos/angular/angular/statuses/{sha}",
      "languages_url": "https://api.github.com/repos/angular/angular/languages",
      "stargazers_url": "https://api.github.com/repos/angular/angular/stargazers",
      "contributors_url": "https://api.github.com/repos/angular/angular/contributors",
      "subscribers_url": "https://api.github.com/repos/angular/angular/subscribers",
      "subscription_url": "https://api.github.com/repos/angular/angular/subscription",
      "commits_url": "https://api.github.com/repos/angular/angular/commits{/sha}",
      "git_commits_url": "https://api.github.com/repos/angular/angular/git/commits{/sha}",
      "comments_url": "https://api.github.com/repos/angular/angular/comments{/number}",
      "issue_comment_url": "https://api.github.com/repos/angular/angular/issues/comments{/number}",
      "contents_url": "https://api.github.com/repos/angular/angular/contents/{+path}",
      "compare_url": "https://api.github.com/repos/angular/angular/compare/{base}...{head}",
      "merges_url": "https://api.github.com/repos/angular/angular/merges",
      "archive_url": "https://api.github.com/repos/angular/angular/{archive_format}{/ref}",
      "downloads_url": "https://api.github.com/repos/angular/angular/downloads",
      "issues_url": "https://api.github.com/repos/angular/angular/issues{/number}",
      "pulls_url": "https://api.github.com/repos/angular/angular/pulls{/number}",
      "milestones_url": "https://api.github.com/repos/angular/angular/milestones{/number}",
      "notifications_url": "https://api.github.com/repos/angular/angular/notifications{?since,all,participating}",
      "labels_url": "https://api.github.com/repos/angular/angular/labels{/name}",
      "releases_url": "https://api.github.com/repos/angular/angular/releases{/id}",
      "deployments_url": "https://api.github.com/repos/angular/angular/deployments",
      "created_at": "2014-09-18T16:12:01Z",
      "updated_at": "2017-09-09T05:09:33Z",
      "pushed_at": "2017-09-09T02:05:28Z",
      "git_url": "git://github.com/angular/angular.git",
      "ssh_url": "git@github.com:angular/angular.git",
      "clone_url": "https://github.com/angular/angular.git",
      "svn_url": "https://github.com/angular/angular",
      "homepage": "https://angular.io",
      "size": 66203,
      "stargazers_count": 27612,
      "watchers_count": 27612,
      "language": "TypeScript",
      "has_issues": true,
      "has_projects": true,
      "has_downloads": true,
      "has_wiki": false,
      "has_pages": false,
      "forks_count": 6919,
      "mirror_url": null,
      "open_issues_count": 1922,
      "forks": 6919,
      "open_issues": 1922,
      "watchers": 27612,
      "default_branch": "master",
      "score": 135.76045
    }
  ]
}
```

Now we have our interface generated and our sample data loaded into it - but it's not ready to be used yet. In the next lesson we will be converting each of those values in the sample data into their appropriate types to be used as an Interface.


## To Implement an Interface

Now that we have our interface generated and our sample data loaded into it, we need to convert the sample values listed into their appropriate Types. To do this, we need to go field by field through our object and identify the type of data represented.

1. Open up your `git-search.ts` file.

2. Let's start with the first parameter in the object, `total_count`. As you can see, the total_count parameter in the object has a value that is a number. So we are going to go ahead and replace the value of the parameter with the TypeScript type number.

```typescript
export interface GitSearch {
 "total_count": number,
```

3. The next value `incomplete_results` has a value of `false`. This is a boolean value, so let's go ahead and replace it with the TypeScript type boolean.

```typescript
export interface GitSearch {
  "total_count": number,
  "incomplete_results": boolean,
```

4. Now we have our Array object items. TypeScript not only needs to know that this is an Array, but it needs to have the contents of it typed as well. To do this, we need to label items as the type Array, and then convert the square brackets around its contents [] into tag brackets <>.

```typescript
export interface GitSearch {
  "total_count": number,
  "incomplete_results": boolean,
  "items": Array<
    {
      "id": 24195339,
      "name": "angular",
      "full_name": "angular/angular",
      "owner": {
        "login": "angular",
        "id": 139426,
        "avatar_url": "https://avatars3.githubusercontent.com/u/139426?v=4",
        "gravatar_id": "",
        "url": "https://api.github.com/users/angular",
        "html_url": "https://github.com/angular",
        "followers_url": "https://api.github.com/users/angular/followers",
        "following_url": "https://api.github.com/users/angular/following{/other_user}",
        "gists_url": "https://api.github.com/users/angular/gists{/gist_id}",
        "starred_url": "https://api.github.com/users/angular/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/angular/subscriptions",
        "organizations_url": "https://api.github.com/users/angular/orgs",
        "repos_url": "https://api.github.com/users/angular/repos",
        "events_url": "https://api.github.com/users/angular/events{/privacy}",
        "received_events_url": "https://api.github.com/users/angular/received_events",
        "type": "Organization",
        "site_admin": false
      },
      "private": false,
      "html_url": "https://github.com/angular/angular",
      "description": "One framework. Mobile & desktop.",
      "fork": false,
      "url": "https://api.github.com/repos/angular/angular",
      "forks_url": "https://api.github.com/repos/angular/angular/forks",
      "keys_url": "https://api.github.com/repos/angular/angular/keys{/key_id}",
      "collaborators_url": "https://api.github.com/repos/angular/angular/collaborators{/collaborator}",
      "teams_url": "https://api.github.com/repos/angular/angular/teams",
      "hooks_url": "https://api.github.com/repos/angular/angular/hooks",
      "issue_events_url": "https://api.github.com/repos/angular/angular/issues/events{/number}",
      "events_url": "https://api.github.com/repos/angular/angular/events",
      "assignees_url": "https://api.github.com/repos/angular/angular/assignees{/user}",
      "branches_url": "https://api.github.com/repos/angular/angular/branches{/branch}",
      "tags_url": "https://api.github.com/repos/angular/angular/tags",
      "blobs_url": "https://api.github.com/repos/angular/angular/git/blobs{/sha}",
      "git_tags_url": "https://api.github.com/repos/angular/angular/git/tags{/sha}",
      "git_refs_url": "https://api.github.com/repos/angular/angular/git/refs{/sha}",
      "trees_url": "https://api.github.com/repos/angular/angular/git/trees{/sha}",
      "statuses_url": "https://api.github.com/repos/angular/angular/statuses/{sha}",
      "languages_url": "https://api.github.com/repos/angular/angular/languages",
      "stargazers_url": "https://api.github.com/repos/angular/angular/stargazers",
      "contributors_url": "https://api.github.com/repos/angular/angular/contributors",
      "subscribers_url": "https://api.github.com/repos/angular/angular/subscribers",
      "subscription_url": "https://api.github.com/repos/angular/angular/subscription",
      "commits_url": "https://api.github.com/repos/angular/angular/commits{/sha}",
      "git_commits_url": "https://api.github.com/repos/angular/angular/git/commits{/sha}",
      "comments_url": "https://api.github.com/repos/angular/angular/comments{/number}",
      "issue_comment_url": "https://api.github.com/repos/angular/angular/issues/comments{/number}",
      "contents_url": "https://api.github.com/repos/angular/angular/contents/{+path}",
      "compare_url": "https://api.github.com/repos/angular/angular/compare/{base}...{head}",
      "merges_url": "https://api.github.com/repos/angular/angular/merges",
      "archive_url": "https://api.github.com/repos/angular/angular/{archive_format}{/ref}",
      "downloads_url": "https://api.github.com/repos/angular/angular/downloads",
      "issues_url": "https://api.github.com/repos/angular/angular/issues{/number}",
      "pulls_url": "https://api.github.com/repos/angular/angular/pulls{/number}",
      "milestones_url": "https://api.github.com/repos/angular/angular/milestones{/number}",
      "notifications_url": "https://api.github.com/repos/angular/angular/notifications{?since,all,participating}",
      "labels_url": "https://api.github.com/repos/angular/angular/labels{/name}",
      "releases_url": "https://api.github.com/repos/angular/angular/releases{/id}",
      "deployments_url": "https://api.github.com/repos/angular/angular/deployments",
      "created_at": "2014-09-18T16:12:01Z",
      "updated_at": "2017-09-09T05:09:33Z",
      "pushed_at": "2017-09-09T02:05:28Z",
      "git_url": "git://github.com/angular/angular.git",
      "ssh_url": "git@github.com:angular/angular.git",
      "clone_url": "https://github.com/angular/angular.git",
      "svn_url": "https://github.com/angular/angular",
      "homepage": "https://angular.io",
      "size": 66203,
      "stargazers_count": 27612,
      "watchers_count": 27612,
      "language": "TypeScript",
      "has_issues": true,
      "has_projects": true,
      "has_downloads": true,
      "has_wiki": false,
      "has_pages": false,
      "forks_count": 6919,
      "mirror_url": null,
      "open_issues_count": 1922,
      "forks": 6919,
      "open_issues": 1922,
      "watchers": 27612,
      "default_branch": "master",
      "score": 135.76045
    }
>
}
```

5. Next, we need to go through each parameter of the contents of the items object and replace them with their types. We could do this one at a time, but instead let's use the regular expression match capabilities of Visual Studio Code.

First, we will match all of the string values and replace them with the string type. Open the `Edit... Replace` command and select the `.*` option indicating we are going to use a regular expression to find strings in our source.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/a1e61da2016ded01467d83901edad188/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/replace_regex.png)

Then enter the regular expression `: "[^"]*"` as the find value and enter `: string` as the replace value. Note that there is a space after the `:` character. Your matches should be similar to the image below - go ahead and replace the values.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/9210b0ef21168cbfa4f771c8918ff6c4/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/regex1.png)

**Note:** To give you an idea of how this regular expression works, imagine the following:

* The regular expression `: "[^"]*"` defines the following pattern:
* A `:` followed by a space followed by a `"` followed by zero or more characters that are not `"` followed by a `"`.
* Each line in the file is searched to see if it contains a match for this pattern, if so all of the characters that match are selected.
* The replace operation then replaces all of the selected characters on the line with the replacement value, in this case `: string`.

Next, we will replace the numbers - enter `:(<? )[-0-9.]+` as the find value and `: number` as the replace value. Your matches should be similar to the image below - go ahead and replace the values.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/d2ed27ba2c8ad2d2f80d2c05825f060a/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/regex2.png)

Finally, we will replace the boolean values - enter `:(<? )(true|false)` as the find value and `: boolean` as the replace value. Your matches should be similar to the image below - go ahead and replace the values.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e6229d5f54c7328ca4ce2fe7193d43df/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/regex3.png)

6. When you're finished you should have the following:

```typescript
export interface GitSearch {
  "total_count": number,
  "incomplete_results": boolean,
  "items": Array<
    {
      "id": number,
      "name": string,
      "full_name": string,
      "owner": {
        "login": string,
        "id": number,
        "avatar_url": string,
        "gravatar_id": string,
        "url": string,
        "html_url": string,
        "followers_url": string,
        "following_url": string,
        "gists_url": string,
        "starred_url": string,
        "subscriptions_url": string,
        "organizations_url": string,
        "repos_url": string,
        "events_url": string,
        "received_events_url": string,
        "type": string,
        "site_admin": boolean
      },
      "private": boolean,
      "html_url": string,
      "description": string,
      "fork": boolean,
      "url": string,
      "forks_url": string,
      "keys_url": string,
      "collaborators_url": string,
      "teams_url": string,
      "hooks_url": string,
      "issue_events_url": string,
      "events_url": string,
      "assignees_url": string,
      "branches_url": string,
      "tags_url": string,
      "blobs_url": string,
      "git_tags_url": string,
      "git_refs_url": string,
      "trees_url": string,
      "statuses_url": string,
      "languages_url": string,
      "stargazers_url": string,
      "contributors_url": string,
      "subscribers_url": string,
      "subscription_url": string,
      "commits_url": string,
      "git_commits_url": string,
      "comments_url": string,
      "issue_comment_url": string,
      "contents_url": string,
      "compare_url": string,
      "merges_url": string,
      "archive_url": string,
      "downloads_url": string,
      "issues_url": string,
      "pulls_url": string,
      "milestones_url": string,
      "notifications_url": string,
      "labels_url": string,
      "releases_url": string,
      "deployments_url": string,
      "created_at": string,
      "updated_at": string,
      "pushed_at": string,
      "git_url": string,
      "ssh_url": string,
      "clone_url": string,
      "svn_url": string,
      "homepage": string,
      "size": number,
      "stargazers_count": number,
      "watchers_count": number,
      "language": string,
      "has_issues": boolean,
      "has_projects": boolean,
      "has_downloads": boolean,
      "has_wiki": boolean,
      "has_pages": boolean,
      "forks_count": number,
      "mirror_url": null,
      "open_issues_count": number,
      "forks": number,
      "open_issues": number,
      "watchers": number,
      "default_branch": string,
      "score": number
    }
   >
}
```

Note that the `mirror_url` parameter has a value of null. We won't be able to determine it's type from this sample, but we can probably guess this will be a URL string because it's key is mirror_url. In this case we have two choices, either to mark it as any, or to mark it as a string. Since we generally want to avoid using any in TypeScript because it bypasses type checking, we will assume it is a string and mark it as such. If we couldn't determine the future value as easily though it would be prudent to use any.

```typescript
"forks_count": number,
"mirror_url": string,
"open_issues_count": number,
```

That's it! You now have a complete Interface of the GitHub search API to use with your application.

## To Import an Interface into Your Service

Now that we have our service ready to go, we can import the interface we made in the previous task. When we do this, we can give the Service the shape of the expected output of our API call, and every component that we subsequently inject our Service into will be provided with that information as well. This will especially come in handy later when we are building out the views for our application.

Let's go ahead and import the Interface into our Service.

1. Open up your `git-search.service.ts` file in Visual Studio Code.

2. Go ahead and open up your `git-search.ts` file (the file containing your interface) as well.

3. Take a look at the top line of your `git-search.ts` file. You will see the following:

```typescript
export interface GitSearch {
```

Using the export statement in this fashion creates an export object with GitSearch as a parameter. It will need to be imported using curly braces in an import statement {}. Curly braces allow you to have multiple exports in the same file, and to import them separately on a single import statement.

4. Let's add the import statement to the top line of git-search.service.ts.

```typescript
import { GitSearch } from './git-search'
```

As the git-search.ts file that implements the interface is in the same directory as the `git-search.service.ts` file, you can use the relative directory path `./` to indicate that the file is in the same directory. You also do not need to include the .ts extension on the end of the file as TypeScript assumes this. Note that the name of the interface in the import statement matches the name of the interface in the export statement in git-search.ts. As we are importing types using the curly braces {} syntax, you need to ensure that the names in the import match the names being exported.

5. When you are finished, your service should now look like this:

```typescript
import { Injectable } from '@angular/core';
import { GitSearch} from './git-search'
@Injectable()
export class GitSearchService {

  constructor() { }

}
```

Our interface is now imported into our service and ready to go.

## To Create a Service Method

In the previous task, we created a service and imported our GitSearch Interface. Since we have our service created and our interface imported into it, we are now going to do two things: prepare a method to be used within our service to access the GitHub API, and set up caching within that method. Caching within a service is relatively easy, and allows you to be able to save data to be used later, preventing subsequent API calls and allowing those repeated calls to be delivered much quicker.

Note that at the end of this task we will have our method set up to be used, but it won't be talking to the API just yet. In the next lab we will be taking this method and adding the HttpClient to access the GitHub Search API.

1. Open up your `git-search.service.ts` file.

2. Above our constructor function, let's add an empty array to contain the cached values. This will set up a cache for our service the first time it is injected.

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search'
@Injectable()
export class GitSearchService {
    cachedValues: Array<{
          [query: string]: GitSearch
      }> = [];
  constructor() {}
}
```

You can see we went ahead and described the shape of the objects we are going to be storing inside of the array. In this case the key of each object in the array will be the query passed to the function - so it subsequently has a type of `string` - and the value which will be the actual output from the API - marked with the type of GitSearch, which is using our previously imported interface.

3. Let's go ahead and add our method next.

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search'
@Injectable()
export class GitSearchService {
    cachedValues: Array<{
        [query: string]: GitSearch
    }> = [];
  constructor() {}

  gitSearch = (query: string) => {}
}
```

The `gitSearch `function we have just created is scoped to the this variable of the service, so if we were referencing it from within the service we would reference `this.gitSearch`. Outside of the service, in other components, it would be referenced as `GitSearchService.gitSearch`.

4. Next we are going to create a Promise within our function to get resolved by either the cache value or the API call value.

```typescript
gitSearch = (query: string) => {
    let promise = new Promise((resolve, reject) => {})
    return promise;
  }
```

Note the two parameters of the Promise - resolve and reject. You will call resolve with successful data calls, whereas reject would be used for manual error handling.

5. Inside of our promise, we want to add a check to see if we want to use the cached value instead of querying for the response.

```typescript
gitSearch = (query: string) => {
    let promise = new Promise((resolve, reject) => {
        if (this.cachedValues[query]) {
            resolve(this.cachedValues[query])
        }
    })
    return promise;
}
```

This will check the array that we created earlier for cached values with the same search query as what is being currently searched. This will get returned immediately without querying the API.

6. If a value isn't cached, we will want to return the call from the API. For now, we'll just put a direct resolve call into an else block.

```typescript
gitSearch = (query: string) => {
    let promise = new Promise((resolve, reject) => {
        if (this.cachedValues[query]) {
            resolve(this.cachedValues[query])
        }
        else {
            resolve("Placeholder");
        }
    })
    return promise;
}
```

Note: What we have demonstrated here is a very naive caching method that caches the values for the lifetime of the application instance. For long running applications or APIs where the return values could change frequently (i.e. stock price) this approach would be problematic. However, this approach could be extended - for example - by storing the time the query was last executed. The code could then check to see if the cached data was older than a predefined limit (say 10 minutes). If the cached data had expired, it could then be discarded, a new API call made, and the new data saved in the cache and returned.

7. When you're finished, you should have something that looks like this:

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search'
@Injectable()
export class GitSearchService {
    cachedValues: Array<{
          [query: string]: GitSearch
    }> = [];
    constructor() {}

    gitSearch = (query: string) => {
        let promise = new Promise((resolve, reject) => {
            if (this.cachedValues[query]) {
                resolve(this.cachedValues[query])
            }
            else {
                resolve("Placeholder");
            }
        })
        return promise;
    }
}
```

So now we have a service created, our methods ready, and our interfaces injected.

## To Use HttpClient

Now we are going to be adding the HttpClient to our GitHub Search service so that we can actually call the GitHub API and retrieve a result.

In order to use the HttpClient, we first need to import it into our application.

1. Open up your `app.module.ts` file.

2. Import the `HttpClientModule` into your `app.module`

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { AppComponent } from './app.component';
import { HttpClientModule } from '@angular/common/http';
```

3. Add the `HttpClientModule` to your list of imports in the module.

```typescript
imports: [
    BrowserModule,
    HttpClientModule
],
```

4. When you're finished, your `app.module.ts` should look like this:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { AppComponent } from './app.component';
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Now that we have enabled `HttpClient` in our application, we can import our `HttpClient` into our service and use it.

5. Open up your `git-search.service.ts` file in Visual Studio Code.

6. Add the following line to the import block at the top of your file:

```typescript
import { HttpClient } from '@angular/common/http';
```

This imports the HttpClient into your service.

7. HttpClient will emit RxJS Observables by default. Since we are using Promises in this example, we will import a feature from RxJS will allow us to convert the Observable emitted by the HttpClient into a Promise.

```typescript
import 'rxjs/add/operator/toPromise';
```

**Note:** The import syntax is a little different than before. This particular syntax only adds the toPromise method to the Observable type without adding other methods that you may not need. This can help keep the size of your application as small as possible.

8. Our service also needs to have an instance of the HttpClient type to use for the WebApi calls. To achieve this, we will ask the Angular infrastructure to inject HttpClient via the service constructor. One way to do this would be as follows

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';
import 'rxjs/add/operator/toPromise';

@Injectable()
export class GitSearchService {
  cachedValues: Array<{
    [query: string]: GitSearch
  }> = [];
  private http: HttpClient
  constructor(http: HttpClient) {
      this.http = http
  }
```

Within the constructor, we assign the value of http passed to the constructor to the private http member variable. If we had a large number of constructor parameters, writing this code over and over would be very repetitive. Fortunately the designers of TypeScript realized this and created a nice shorthand syntax:

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';
import 'rxjs/add/operator/toPromise';

@Injectable()
export class GitSearchService {
  cachedValues: Array<{
    [query: string]: GitSearch
  }> = [];
  constructor(private http: HttpClient) {
  }
```

In this version, the http member is declared as private as part of the constructor definition and this is the clue for the TypeScript transpiler to automatically create the `http` member and assign the value. As you can imagine, this saves keystrokes and repetitive code over time.

9. Now, let's go ahead and add the http call to our Promise created earlier.

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';
import 'rxjs/add/operator/toPromise';

@Injectable()
export class GitSearchService {
  cachedValues: Array<{
    [query: string]: GitSearch
  }> = [];
  constructor(private http: HttpClient) {}

  gitSearch = (query) => {
    let promise = new Promise((resolve, reject) => {
        if (this.cachedValues[query]) {
            resolve(this.cachedValues[query])
        }
        else {
            this.http.get('https://api.github.com/search/repositories?q=' + query)
        }
    })
    return promise;
  }
}
```

Note that we have concatenated our query param onto the end of our API call.

10. Next, we're going to chain a call to `.toPromise()` onto the end of the http call, to convert the Observable into a Promise. Remember we can only do this because we imported toPromise earlier.

```typescript
else {
    this.http.get('https://api.github.com/search/repositories?q=' + query)
    .toPromise()
}
```

11. Now we need to chain a `.then()` method to deal with the response from the call.

```typescript
else {
    this.http.get('https://api.github.com/search/repositories?q=' + query)
    .toPromise()
    .then( (response) => {
        resolve(response)
    }, (error) => {
        reject(error);
    })
}
```

Note that we are resolving the original promise we created with the result from the promise generated by the API call. Promises enable you to do that - use other promise resolutions to resolve them. Note that we have also included a second function callback to `.then()` to handle any errors that occur by rejecting the promise with the returned error.

Finally, to correctly identify the response with TypeScript, we need to annotate our method to include the proper types. In this case, our function is taking in a string and it's going to be returning a Promise with a return value that is a GitSearch - `Promise<GitSearch>`. We also need to mark that the response will have the shape of GitSearch by using the type assertion response as `GitSearch`. Update the function to match:

```typescript
gitSearch = (query: string): Promise<GitSearch> => {
    let promise = new Promise<GitSearch>((resolve, reject) => {
        if (this.cachedValues[query]) {
            resolve(this.cachedValues[query])
        }
        else {
            this.http.get('https://api.github.com/search/repositories?q=' + query)
            .toPromise()
            .then( (response) => {
                resolve(response as GitSearch)
            }, (error) => {
                reject(error);
            })
        }
    })
    return promise;
}
```

13. When you are finished, your service should look like this:

```typescript
import { Injectable, Inject } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';
import 'rxjs/add/operator/toPromise';

@Injectable()
export class GitSearchService {
  cachedValues: Array<{
    [query: string]: GitSearch
  }> = [];
  constructor(private http: HttpClient) {
      
  }

  gitSearch = (query: string): Promise<GitSearch> => {
    let promise = new Promise<GitSearch>((resolve, reject) => {
        if (this.cachedValues[query]) {
            resolve(this.cachedValues[query])
        }
        else {
            this.http.get('https://api.github.com/search/repositories?q=' + query)
            .toPromise()
            .then( (response) => {
                resolve(response as GitSearch)
            }, (error) => {
                reject(error);
            })
        }
    })
    return promise;
  }
}
```

Great! We now have a completed service ready to use. In our next task, we're going to call the service, and see the result.