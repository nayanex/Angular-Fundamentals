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

*OBS:* for styles choose `.css`

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

8. Our service also needs to have an instance of the HttpClient type to use for the WebApi calls. To achieve this, we will ask the Angular infrastructure to inject HttpClient via the service constructor. One way to do this would be as follows

```typescript
import { Injectable } from '@angular/core';
import { GitSearch } from './git-search';
import { HttpClient } from '@angular/common/http';

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

10. Next, we're going to chain a call to `.toPromise()` onto the end of the http call, to convert the Observable into a Promise.

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

## To Consume Services

Since we have a completed service ready to use, now we are going to consume that service in our front-end application, call the API, and display a result.

1. First let's add our service to our application. To do this, open up your `app.module.ts` file and import your service into it.

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { AppComponent } from './app.component';
import { GitSearchService } from './git-search.service';
```

2. Next, inside the providers array we will add our service. When you're done, your `app.module.ts` should look like this.

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { AppComponent } from './app.component';
import { GitSearchService } from './git-search.service';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [GitSearchService],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

By adding `GitSearchService` to the providers array, we are telling Angular that it is a dependency. This makes `GitSearchService` available to be injected into other components as needed.

3. Open up the `app.component.t`s file in your `angular-fundamentals/app/src` directory. It should look like this:

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'GitHub Browser';
}
```

4. We need to import our service to it. Add the following line to the import block at the top of the file:

```typescript
import { GitSearchService } from './git-search.service';
```

5. We also need to add a new import to our Angular Core imports, `OnInit`. This provides what is called a Lifecycle Hook, to execute code when the component is first rendered. Add `OnInit` to your Angular Core import like so:

```typescript
import { Component, OnInit } from '@angular/core';
import { GitSearchService } from './git-search.service';
```

6. In order to use the `OnInit` lifecycle hook, you need to add an implements statement in your class statement, and add a method for `ngOnInit()`

```typescript
export class AppComponent implements OnInit {
  ngOnInit() {
    
  }
  title = 'GitHub Browser';
}
```

The `implements` keyword extends a class with another one - in this case adding OnInit to your component class.

7. We need to add a constructor function that allows our `GitSearchService` to be passed into the class. We declare it as a private member so it will be available via the this property.

Note that adding `GitSearchService` to the constructor declares it as a dependency that the Angular infrastructure needs to satisfy. As we added GitSearchService to the providers array earlier, Angular will automatically pass an instance of the `GitSearchService` to our component.

```typescript
export class AppComponent implements OnInit {
  constructor(private GitSearchService: GitSearchService) {

  }

  ngOnInit() {

  }
  title = 'GitHub Browser';
}
```

8. Next, we are going to add our call to our service inside the ngOnInit hook.

```typescript
ngOnInit() {
    this.GitSearchService.gitSearch('angular').then( (response) => {
      alert("Total Libraries Found:" + response.total_count);
    }, (error) => {
      alert("Error: " + error.statusText)
    })
}
```

We are passing the search term `angular` into the `gitSearch` function that is part of `GitSearchService`. As this function returns a promise we can use a `.then()` method to respond to the promise's resolution, in this case displaying an alert that tells us the total count of results available. We have also added an error handler function afterwards to display an alert of the text description of the HTTP status if the HTTP call fails.

Your `app.component.ts` file should look something like this:

```typescript
import { Component, OnInit } from '@angular/core';
import { GitSearchService } from './git-search.service';
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css'],
  providers: [GitSearchService]
})
export class AppComponent implements OnInit {
  constructor (private GitSearchService : GitSearchService) {

  }
  ngOnInit() {
    this.GitSearchService.gitSearch('angular').then( (response) => {
      alert("Total Libraries Found:" + response.total_count);
    }, (error) => {
      alert("Error: " + error.statusText);
    })
  }
  title = 'app is functional!';
}
```

9. Save all files, and open up a command prompt or terminal.

10. Navigate to your `angular-fundamentals` folder.

11. Type `ng serve`.

12. Once the app has compiled and started, open up your browser and navigate to l`ocalhost:4200`. You should see the following:

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/def1c0fc6234eaa5380a3850d126e29a/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/M2L08result.png)

13. Now that you've seen a successful call, let's demonstrate an error. Change your gitSearch parameter to the following and save your file.

```typescript
this.GitSearchService.gitSearch('&&&&&').then( (response) => {
  alert("Total Libraries Found:" + response.total_count);
}, (error) => {
  alert("Error: " + error.statusText);
})
```

14. When the app has compiled and started, navigate to localhost:4200 and you should see this instead:

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/fdd7637a971578f0cb4cd8b9c59c2f04/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/error.png)

And there you have it! You have successfully used the HttpClient module to access data from an API in your Angular app. You have seen how to handle both the success and failure of such a call using a promise. 


# Generate git-users Interface

1. Create a new interface for searching users in GitHub called [git-users](https://developer.github.com/v3/search/#search-users). [Sample Call](https://api.github.com/search/users?q=tom)

`ng generate interface git-users`

2. Create a new method in your existing service to search for users.

```typescript
gitUsers = (query: String): Promise<GitUsers> => {
    let promise = new Promise<GitUsers>((resolve, reject) => {
      this.http.get('https://api.github.com/search/users?q=' + query)
      .toPromise()
      .then( (response) => {
        resolve(response as GitUsers)
      }, (error) => {
        reject(error);
      })
    })
    return promise;
}
```

3. Consume that new method in your application.

We found a why to call this service method in our `app.componennt.ts`

```typescript
this.GitSearchService.gitUsers('tom').then( (response) => {
      alert("Total Users Found:" + response.total_count);
    }, (error) => {
      alert("Error: " + error.statusText)
    })
}
```

# Components

A component is responsible for controlling a view, or a part of the screen. You create a class to hold the application logic that forms part of the component.

Angular follows the MVC architecture which stands for Model-View-Controller. The Model portion contains application data. The View is the user interface (UI) or the web page that a user interacts with. The Controller handles the interaction and communication between the View and the Model. In Angular, your component will interact with the view through an application programming interface (API). The APIs consist of properties and methods to act on those properties, or provide some functionality.

One of the most noteworthy and useful features of the Angular architecture is the usage of reusable components to display data. By using an Angular Component, you can couple data display logic, styles, and HTML into one container that's easily portable throughout your application.

An Angular component consists of a template, that is the view or “a” view layout for a portion of your web application. The template consists of HTML for the layout and is used to define the rendered content on the page.

The Angular code that you will add to this HTML is responsible for setting the bindings to data and the directives within the HTML that provides the dynamic aspects of an angular component.

Angular also makes use of a class file to contain code that supports the view in the template. Typically this class file will be created in TypeScript and will contain the properties and methods that will be used by your application.

You will also find metadata in the component, which is used to provide additional information about your component to Angular. Metadata is defined using decorators. You will find out how to use these aspects in this module.

## Generate Components

You'll typically have a top-level component in your Angular application. In the tutorial labs, you will work on building a top-level component called `git-search`. The Angular CLI command is `ng generate` component which is followed by the component name you want to use such as `ng generate component git-search`.

This will result in a new folder structure being created in your Angular app's root folder. The folder structure will be `/src/app/git-search` in this instance. Within this folder, a number of files will be created:

1. a typescript file with the `.ts` extension to contain the logic for the component
2. a CSS file that is injected into the component for specifying styling using CSS for the component
3. an HTML file that will contain the view template
4. a Karma test file with the .spec.ts extension, in the event you want to implement Karma testing
When you open the `.ts` file, you will find these common aspects as a part of the component:

```typescript
import { Component } from @angular/core
```

Import statements are used to access functionality in other code such as libraries and other classes. This line is responsible for importing the Component Object from the `@angular/core` library. This is one of the main libraries used in Angular.

```typescript
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css'],
  title: string = 'Page Title';
}) 
```

This is segment where you define your component. The `@` is a TypeScript symbol that helps us describe an Angular directive. In this case, `@Component` is a directive that tells Angular we wish to create a new component.

`@Component` is also known as a decorator. A decorate in Angular is prefixed with an `@` symbol and is considered a mechanism to add metadata to a class, to the members of a class, or to method arguments of a class. You place the decorator before your class name, ie before the export statement. Angular has several built-in decorators and you will get a change to use some of them in this course.

Within the `@Component` body, we see a `selector`, `templateUrl`, and `styleUrl` entries with some values assigned. Let's cover each of these so you understand their purpose.

* `selector` - this specifies the name of an HTML tag that will contain this component when the application is running. In the HTML, you will find `<app-root></app-root>` tags for this component
* `templateUrl` - using this option allows you to specify a template that will contain the HTML for this component. You could also opt to use the template: option and specify “inline” HTML right in the body of the component.
* `styleUrls` - this links to an external CSS style sheet that will be applied to the component's HTML rendering

There are other options available for the component and you can browse the Angular documentation for additional options and instructions on using them.

Everything found within the `@Component` section is considered to be metadata and template information for this component. Obviously the template information consists of the HTML elements that may be found within the component. In this instance, we are using a URL to define the template rather than placing the HTML inline in the component.

Next we set up an export statement like this:

```typescript
export class AppComponent implements OnInit
```

The `export` keyword is what allows your component to be available to be imported into other files in the project. The `class` keyword identifies this as a class file so if you are familiar with object-oriented programming, then you will understand that class is a keyword used to identify a file that contains the “blueprint” information for a reusable component.

The AppComponent identifier is the class name. It will be the name you use within an import statement in other areas of your application and offers a clear identifer for this class.

The last keyword, `implements`, will not always be present on all components. In this case, it indicates that our `AppComponent` class will also implement functionality that is specified in another component or interface, known as `OnInit`. We won't talk about interfaces here but again, it is an object-oriented programming concept that is used to specify behavior of a class file based on behaviors defined in another file.

Also, this is where we define any variables or functions that the component will consist of. We can see an example here:

```typescript
constructor (private GitSearchService : GitSearchService) {
    
  }
  ngOnInit() {
    this.GitSearchService.gitSearch('angular').then( (response) => {
      alert("Total Libraries Found:" + response.total_count);
    }, (error) => {
      alert("Error: " + error.statusText)
    })
  }
  title = 'GitHub Browser';
```

Here we setup a constructor, implement the `ngOnInit()` method, and set a title for the component.

## Binding Data

Binding is the term used to describe how the data for our application is “connected” to the user interface. If we step back and review the MVC architecture again, we noted that the Model was defined as the data, the View as the UI, and the Controller as the application logic but also as the communicator between the data and the UI.

So, binding is responsible for the communication between our data and our UI. Our data can reside in a back-end database running on a server or it could be as simple as a flat file, such as a JSON file, that contains the data we want to use in our application.

Binding allows us to pass the data into the UI through the use of properties, in the class that defines our Model, and the use of directives, which make use of a concept known as interpolation. Interpolation is the mechanism used to represent a placeholder, in your template, for the data that will be displayed.

So, in summary, binding is the mechanism used to tie the data to the UI for display.

In order to bind data to a template in Angular, you need to have that data available. For now, we will focus on using data that is part of an Angular component. That is, we will make use of the properties of our Angular component and bind them to UI elements in our template.

See bellow an example of a component with properties:

```typescript
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css'],
  title: string = 'Page Title';
})
```

`selector:`, `templateUrl:`, `styleUrls:`, and `title:` are examples of properties for this component. The one that we will be most concerned with for this binding is the `title:` property. It is one that has a type specified (string) and a value after the `=` sign (‘Page Title’).

There are four types of binding that we can do in Angular:

* interpolation binding
* property binding
* event binding
* two-way binding.

### Interpolation Binding 

Interpolation binding is accomplished using the interpolation syntax, also known as the moustache, where we place the data property into the HTML by using the double curly braces, `{{title}}`.

`<h1>{{title}}</h1>`

### Property Binding 

Here is an example of doing the same thing with property binding. Note the syntax is a bit different than you might be used to when dealing with HTML attributes. We use square brackets to surround the HTML attribute, then use the data property in single quotes after the `=` sign.

```html
<h1 [innerHTML] = 'title'></h1>
```

### Event Binding

Event binding is accomplished when we associate an event with a method in our class. For example, we might want to take a specific action in our class when the user clicks a button. In this case, we would use the syntax of"

```html
<button (click) = 'toggleFlag()'>
```

In the above code, we surround the click event attribute of the button element in parentheses and supply the method name in our class, that will handle the event, in single quotes.

### Two-way Binding

Two-way binding allows us to create interactivity or to update our data when the user takes an action with the UI. An example might be a list of products displayed from the data source and then using an input element to allow the user to filter the data displayed based on the value in the input. Sample code here shows using mgModel to achieve two-way binding.

```html
<input [(ngModel)] = 'filter'>
```

These are just simple examples of binding properties or methods from our class to an element in the HTML template. We can also make use of various Angular directives and logic to bind multiple values, such as those that might exist in a database, and create tables on the fly to display these values. Angular binding offers an efficient way to display the data in your application. In the lab for this module, you will use simple binding.

## Pipes

A pipe allows you to use data, as an input to the pipe, and transform it to a more desirable output. As we think about our Angular applications, perhaps the most common reason for creating the application is to access and display data in our web applications. However, the data may be somewhat cryptic or not necessarily “user friendly” as in a data format.

Often times a date may come to in the form:

`Sat Jun 20 2017 04:00:00 GMT -0800 (Pacific Standard Time)`

While it is readable to a certain degree, not every user cares about the time, or the offset. Perhaps you want to display this in a different format that expands the month rather than using an abbreviation, or perhaps, you want to switch the day and month around to support a different locale. Pipes help you accomplish this.

Angular actually has a collection of built-in pipes for common tasks such as DatePipe, UpperCasePipe, LowerCasePipe, and CurrencyPipe. You can find out more about these in the API documentation for Angular. You will make use of the DatePipe and UpperCasePipe in the tutorial labs for this module.

## Using Pipes

Pipes are a concept in Angular that takes data and applies a transformation to it before sending it to the template to be rendered. This can be particularly useful for formatting purposes where consistent data transformations need to be applied to your data.

If you are familiar with command-line or shell environments in operating systems, you may also be familiar with the pipe symbol `|`. In the command-line environments, this pipe symbol is used to send the output from one command to another command. Likewise, in Angular, we are going to use the pipe symbol to transform the data in our template, by passing it through a pipe to a transformation.

In this code sample, taken from the labs, we will demonstrate applying the built-in date pipe to an Angular binding. The way we accomplish this is to add the pipe or | character after the Angular binding, followed by the built-in pipe command. The command we use here is `date:'fullDate'` to indicate a format of full date. See the code sample below:

```html
<div *ngIf="searchResults; else elseBlock">
  ... 
      <p class="description"> {{result.description}}</p> 
      <p> Created On: {{result.created_at | date:'fullDate'}} </p>
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

## Directives

Angular directives are responsible for providing functionality in an Angular application and help transform the Document Object Model (DOM).

When you implement directives in your Angular application, you will use one of two types, structural directives or attribute directives.

Structural directives are what you use to modify the layout of the page by manipulating the DOM. An attribute directive will merely alter the behavior or appearance of an existing DOM element.

### Structural Directives

As we noted in the introduction to directives topic, structural directives manipulate the HTML layout through the DOM. The manipulation comes in the form of either adding, removing, or changing an element. You know you are using a structural directive if the name is preceded by an asterisk such as `*ngIf`.

The `*ngIf` directive is a built-in directive that comes “out-of-the=box” with Angular. So what do we use it for?

Well, the keyword “if” that is contained in the directive should give you some idea. This directive will evaluate a boolean expression and based on the result, it either shows or hides an HTML element, as in the following example.

```html
<p *ngIf="true">
   If the expression is true and ngIf is true, this content is displayed in the DOM.
</p>
<p *ngIf="false">
    If the expression is false and ngIf is false, this content will NOT be displayed in the DOM.
</p>
```

### Attribute Directives

Recall from the introductory topic, attribute directives are responsible for changing the appearance of the element they are attached to rather than creating or removing elements like the structural directives do.

Angular also has some built-in attribute directives that you can use, if you prefer to not create custom attribute directives. Perhaps one of the most commonly used is the ngClass attribute directive.

The ngClass directive is designed to allow you to dynamically apply CSS to an element. The directive uses an expression to evaluate the CSS to apply. An example will illustrate this better.

```html
<p ng-class="{strike: deletedText, bold: important, 'has-error': highlight}">Sample Text</p>
<label>
   <input type="checkbox" ng-model="deletedText">
   Strike Through for Deleted Text (apply the "strike" class)
</label><br>
<label>
   <input type="checkbox" ng-model="important">
   Important Text (apply the "bold" class)
</label><br>
<label>
   <input type="checkbox" ng-model="error">
   Show Where an Error Is (apply the "has-error" class)
</label>
```

In the above example, we have applied the `ng-class` attribute directive to an element with some text in the element.

Using a series of check boxes, we check the expression in the check box against the ng-model directive and apply the CSS styling specified in that class.

NOTE: We don't show the CSS file here as this is merely for illustrative purposes. You will apply the use of directives in your labs.

## Angular Lifecycle

Components in Angular have a lifecycle. Angular follows a lifecycle similar in sequence to:

* Create the component
* Render the component
* Create/Render any children
* Process changes in the component (ongoing)
* Destroy the component

As you can tell from the above list of “lifecycle events”, an Angular application will behave or allow you to interact, at certain times in the lifecycle of the application.

There are some common events, or methods, that you will use to interact your Angular components while your application is bootstrapping, running, and shutting down. You may also see these referred to as lifecycle hooks or component lifecycle hooks.

The three most common methods you will work with are:

* `OnInit` - used to perform initialization of the component(s) or perhaps retrieve data for the application as it loads.

* `OnChanges` - used to perform an action after a change of input properties

* `OnDestroy` - used to clean up the component and resources as the component is being destroyed

## Tutorial Labs

The purpose of these labs is to teach you how to bind dynamic data to a template and manipulate its display. You will learn how to create reusable components to display your data, inject services into them, and render them using Angular's variety of built in tools - including built in pipes and structural directives. We will be taking the service we built in the last module, inject it into a view component, and use it to generate GitHub search results that will be displayed within the component. At the end of the labs, you should be able to construct views and bind them to dynamic data retrieved from a server. 

1. **Creating Components**

In this lab, you will learn how to generate Components using the Angular CLI, and inject and use the service from our previous module. You will then instantiate the component in your main application view.

2. **Creating Templates**

In this lab, you will create a template for your component, bind data from your service to it, and use structural directives to manipulate the display of the data. You will also create and use a component method to make your GitHub search query dynamic.

3. **Using Built-in Pipes and Directives**

In this lab, you will further transform the data using built in Pipes and the ngStyle directive.


## To Generate A Component

In this lab, we are going to create a component to display the data obtained from our GitSearch service.

To do so, the first step is to generate a component using the Angular CLI.

1. Open up your terminal or command prompt.

2. Navigate to your angular-fundamentals folder.

3. Type the following command `ng generate component git-search`.

As you can see the generator created a `/src/app/git-search` folder, as well as a `.css`, `.ts`, `.html`, and `.spec.ts` file for `git-search.component`. These files all have their own purpose.

* The `.ts` file contains the TypeScript logic for the component, and is where you would put methods, service integration, and other logic.
* The `.css` file is automatically injected into your component. You are able to write CSS that is scoped specifically to your component automatically by Angular, without the need to worry about reusing classes.
* The `.html` file is where you will write your view template.
* The `.spec.ts` file is where you would potentially write any Karma tests for the component. We won't be covering testing in this course.

In addition, the command also updates the `app.module.ts` file to ensure the `GitSearchComponent` is available for use. Note that it is imported and added to the declarations array:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { AppComponent } from './app.component';
import { GitSearchService } from './git-search.service';
import { GitSearchComponent } from './git-search/git-search.component';

@NgModule({
  declarations: [
    AppComponent,
    GitSearchComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [GitSearchService],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

And that's it! You now have a component ready to be used.

## To Use a Service

Now that we have our component generated, we are going to inject the service that we created into our component. This will be very similar to what you did when you were working with the `app.component`, except we are going to include an additional method that we will be using later to change the search query dynamically.

1. Open up your `src/app/git-search/git-search.component.ts` file in Visual Studio Code.

2. Import the service into your component by adding an import statement to the top block of code. We also need to import the interface for `GitSearch` that we made in the previous module.

```typescript
import { GitSearchService } from '../git-search.service'
import { GitSearch } from '../git-search'
```

3. Then, go ahead and inject the service in the constructor function.

```typescript
constructor(private GitSearchService: GitSearchService) { }
```

4. Let's go ahead and make a variable to hold the search results to convey to the view. To do so, we'll create a type declaration above the constructor for a `searchResults `variable with the type of `GitSearch`.

```typescript
export class GitSearchComponent implements OnInit {
  searchResults: GitSearch;
  constructor(private GitSearchService: GitSearchService) { }
```

When you declare variable types above a constructor, TypeScript automatically creates a variable scoped to `this`.

5. You'll notice that the `ngOnInit()` lifecycle method has already been created for you. Let's go ahead and add the same code that we had in the `app.component.ts` in the previous module that used the service to display an alert. Open up your app.component.ts and copy the contents of the `ngOnInit()` function, then paste that into the `ngOnInit()` method of `git-search.component.ts`.

```typescript
ngOnInit() {
  this.GitSearchService.gitSearch('angular').then((response) => {
    alert("Total Libraries Found:" + response.total_count);
  }, (error) => {
    alert("Error: " + error.statusText)
  })
}
```

Go ahead and empty the `ngOnInit` function in `app.component.ts` like so:

`ngOnInit() { }`

6. Now, let's modify the inner function of `.then()` to store the search response in the `this.searchResults` variable.

```typescript
ngOnInit() {
  this.GitSearchService.gitSearch('angular').then((response) => {
    this.searchResults = results;
  }, (error) => {
    alert("Error: " + error.statusText)
  })
}
```

7. Next we are going to make a second method that we can call with a search parameter to send a different query string to the server.

```typescript
ngOnInit() {
  this.GitSearchService.gitSearch('angular').then((response) => {
    this.searchResults = results;
  }, (error) => {
    alert("Error: " + error.statusText)
  })
}

gitSearch = (query: string) => {

}
```

8. Let's copy the method from the `ngOnInit()` function, and change `'angular'` to query.

```typescript
ngOnInit() {
  this.GitSearchService.gitSearch('angular').then((response) => {
    this.searchResults = results;
  }, (error) => {
    alert("Error: " + error.statusText)
  })
}

gitSearch = (query: string) => {
  this.GitSearchService.gitSearch(query).then((response) => {
    this.searchResults = results;
  }, (error) => {
    alert("Error: " + error.statusText)
  })
}
```

Now we have a function that we can call to search for whatever keyword we want in GitHub.

9. When you're finished, your `git-search.component.ts` should look like this:

```typescript
import { Component, OnInit } from '@angular/core';
import { GitSearchService } from '../git-search.service'
import { GitSearch } from '../git-search'
@Component({
  selector: 'app-git-search',
  templateUrl: './git-search.component.html',
  styleUrls: ['./git-search.component.css']
})
export class GitSearchComponent implements OnInit {
  searchResults: GitSearch;
  constructor(private GitSearchService: GitSearchService) { }

  ngOnInit() {
    this.GitSearchService.gitSearch('angular').then( (response) => {
      this.searchResults = response;
    }, (error) => {
      alert("Error: " + error.statusText)
    })
  }

  gitSearch = (query) => {
    this.GitSearchService.gitSearch(query).then( (response) => {
      this.searchResults = response;
    }, (error) => {
      alert("Error: " + error.statusText)
    })
  }

}
```

So to recap, we have modified this component so that the `GitSearchService` is injected using dependency injection. We modified `ngInit` so that it executes a search for `‘angular’` when the component is initialized, and we have added a function called `gitSearch` that will take an arbitrary query string and perform a search using that value. In our next task we are going to instantiate our new `GitSearchComponent` in our main view component - `app.component.ts`.

# To Instantiate a Component

Now that we have our component created and hooked up to our service, we need to instantiate it in our main view, contained within `app.component.ts`. Components can be used throughout a module without having to import them into other components.

1. First, let's open up your `app.module.ts` file in Visual Studio Code.

2. Your `app.module.ts` file should look like this:

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { AppComponent } from './app.component';
import { GitSearchService } from './git-search.service';
import { GitSearchComponent } from './git-search/git-search.component';

@NgModule({
  declarations: [
    AppComponent,
    GitSearchComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule
  ],
  providers: [GitSearchService],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

You can see that `GitSearchComponent` is imported at the top, and has been added to the declarations array. Every component must be imported into one (and only one) `@NgModule` and the declarations array contains the list of all components available within that module. As this module represents the application, this ensure the `AppComponent` and `GitSearchComponent` components are available throughout the application. There's nothing more to do in this file, we are just verifying that the component has been properly configured by the Angular CLI.

3. Next, let's go back to our `git-search/git-search.component.ts` file. At the top of the file, you will notice this section.

```typescript
@Component({
  selector: 'app-git-search',
  templateUrl: './git-search.component.html',
  styleUrls: ['./git-search.component.css']
})
```

This is the component declaration. It has three properties, `selector`, `templateUrl` and `styleUrls`. There are more options available, but these are the most commonly used options for `@Component`. The templateUrl and styleUrls properties point to external files where the template and its respective CSS content are stored. You will note that the `styleUrls` is an array, meaning you can reference more than one stylesheet.

It is also worth noting that you can elect to include `HTML` and `CSS` directly within the `git-search.component.ts` file by using the template and styles properties instead. You should only do this if your HTML and CSS is trivial and, even then, separate files are a best practice. This is what inline HTML and CSS would look like (don't update your source - this is just for your reference):

```typescript
@Component({
  selector: 'app-git-search',
  template: `
    <p>
      git-search works!
    </p>`,
  styles: ['p { background: red; }']
})
```

The selector field is what we are interested in right now, as it contains the tag name (or element name) that identifies the component when used in a template. As you can see, `app-git-search` is the `selector` for the `GitSearchComponent`. Whenever Angular sees `<app-git-search></app-git-search>` in a template, it will replace that with the `GitSearchComponent` template. Let's remember that, we'll need it in a moment.

4. Open up your `app.component.html` file. Go ahead and delete all of the html and replace it with:

```html
<div style="text-align:center">
</div>
```

5. Remember the selector attribute from the `@Component` declaration? We're going to use that as though it were an HTML tag name to instantiate the component.

```html
<div style="text-align:center">
  <app-git-search>
  </app-git-search>
</div>
```

Note that we included a closing tag. Angular components can't be self-closed like an `<img />` tag or `<input />` tag. They must include both.

Go ahead and open a command prompt or terminal, and navigate to your angular-fundamentals directory.

Use the command `ng serve`.

Open your browser and point it to `localhost:4200` and you should see the following.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/3639090caed873ae2c421bdaa96c02f9/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/M3L7result.png)

You have now created and instantiated your first Angular component. 

## To Bind Data to Templates

Now we are going to create the template to drive the display of our `GitSearch` data. An Angular Template is essentially an HTML file, but through Angular we are able to bind data from our component logic directly to the HTML, and use other features such as pipes, directives, and other components.

In this lab, we are going to create a template for our component that holds the display results from our `GitSearchService`.

1. Open up the `src/app/git-search/git-search.component.html` file in Visual Studio Code. It will look like this:

```html
<p>
  git-search works!
</p>
```

2. First we are going to bind a simple value to our application, so we are going to use the total number of repositories returned from the search. Go ahead and open your `src/app/git-search.ts` file to take a look at the interface so you can remember what the shape of the output is going to look like.

```typescript
export interface GitSearch {
  "total_count": number,
  "incomplete_results": boolean,
  "items": Array<
{
```

Notice that the first few values include the one we are looking for: `total_count`. Let's remember that key for now.

3. In the previous lab, we created a value in our `git-search.component.ts` file to store the search results when they come back from the server. If you don't recall, go ahead and open up your `git-search.component.ts` file and take a look.

```typescript
export class GitSearchComponent implements OnInit {
  searchResults: GitSearch;
  constructor(private GitSearchService: GitSearchService) { }

  ngOnInit() {
    this.GitSearchService.gitSearch('angular').then( (response) => {
      console.log(response)
      this.searchResults = response;
    }, (error) => {
      alert("Error: " + error.statusText)
    })
}
```

As you can see, we made the `this.searchResults` variable to hold the search results. Variables scoped to this in your component logic are made available for your templates to consume. In order to do this, we use the double-curly-braces syntax. So to access this.searchResults we would use `{{searchResults}}` in our template. So you will use interpolation to directly insert the value of a variable into text or as the value for an attribute.

4. Since we are wanting to display the total number of results that the search returned, we are going to use the property we referenced from the interface - `total_count` - in our `searchResults` variable. Let's also throw in a label to identify what the piece of data being displayed:

```html
<h3>Total Results: {{searchResults.total_count}}</h3>
<p>
  git-search works!
</p>
```

5. We don't need the `<p>` tag indicating that the component works anymore, so let's get rid of it.

```html
<h3>Total Results: {{searchResults.total_count}}</h3>
```

6. Open up a browser and navigate to `l`ocalhost:4200`. You should see the following:

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/4f27d842caf444205763f04f030f1ea4/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/result1.png)

As you can see, we've successfully bound a value from our `searchResults` to our HTML display. 

## To Use Structural Directives ngIf and ngForOf

Directives are basically commands issued to Angular to run specific processes on data or template displays. Structural directives are directives that change the structure of your template. The two most commonly used structural directives are `ngIf` and `ngFor`. `ngIf` allows you to conditionally render a portion of your template based upon the truthiness of a specific value in your component logic. `ngFor` is a repeater directive that allows you to execute a portion of your template in a repeated fashion for each item in an array, and provides the context of the specific index in the array to the instance of the repeater. These two tools are the most useful and fundamental pieces for constructing a web application view.

In this task, we are going to use ngFor to iterate over each result in our `searchResults` variable, and display some information from it. Then we are going to use our ngIf directive to only render our results when the results have become available, and to display an indicator that the results are loading otherwise.

1. First we need to ascertain some relevant data to display from our search results. Let's take a look at our interface again. If you don't still have it open, open up your `src/app/git-search.ts` file.

You will see there is a property items that is an array. The Angular way to display this data is we are going to want to repeat the same chunk of HTML for each item in the items array and we are going to use Angular data binding to show the data that is contained in each item. The `GitSearch` interface defines a lot of properties, but to make things easier we're going to pick a couple of keys to display, in this case `name`, `description`, `html_url`, `owner.login`, and `owner.avatar_url`.

2. If you don't still have it open, open up your `git-search.component.html` file in Visual Studio Code.

3. Before we use our structural directive, let's make the template item that we're going to repeat. We are going to use the HTML unordered list element `<ul>` to start our list of items. Each of our items will then be represented within a list item element `<li>`. As we are going to be using binding we need to think about the variable names we are going to use. When we initiate the repeater, we are going to be setting an instance variable name that will represent each item in the array. In this case we are going to use result, so we are going to use that as the basis for each of our bindings.

```html
<h3>Total Results: {{searchResults.total_count}}</h3>
<ul>
  <li>
    <a [href]="result.html_url">
      <img [src]="result.owner.avatar_url" /> 
      <h4>{{result.name}} 
        <small> by {{result.owner.login}}</small> 
      </h4>
    </a> 
    <p> {{result.description}}</p> 
  </li>
</ul>
```

There are a few things to note here:

* An example of a variable we are binding to is `result.owner.avatar_url` - this will work as we will be assigning an item to result. If you refer back to the `GitSearch` interface, you will see that each item in the `items` array has an `owner` property and each `owner` has an `avatar_url`.
* There are some unusual looking attributes in the HTML: `[src]` in the image link and the `[href]` in the `<a>` tag. In fact Angular uses the `[src]` directive instead of the regular src attribute in HTML when using a value instead of a static string, likewise with the `[href]` attribute in the case of links.
* Not all of the bindings are using the interpolation syntax `{{}}` - we don't use interpolation when we are binding in a directive.

4. Now that we have our basic template for our repeater rigged up, let's go ahead and instantiate the `ngFor` directive on our `<li>` element.

```html
<h3>Total Results: {{searchResults.total_count}}</h3>
<ul>
  <li *ngFor="let result of searchResults.items" >
    <a [href]="result.html_url">
      <img [src]="result.owner.avatar_url" /> 
      <h4>{{result.name}} 
        <small> by {{result.owner.login}}</small> 
      </h4>
    </a> 
    <p> {{result.description}}</p> 
  </li>
</ul>
```

Note that we have instantiated this for the items property of `searchResults`. The `ngFor` directive can only be used on iterable collections such as arrays, it cannot be used on objects directly. The syntax essentially reads as "for every item in `searchResults.items` assign the value to result and then repeat the `<li><\li>` element and it's children using the value of result in the bindings. I think you will agree, it is more succinct to type `<li *ngFor=“let result of searchResults.items” >`.

5. Save your file. If you don't have your app running already, go ahead and open a command prompt or terminal, navigate to your angular-fundamentals folder, and type ng serve. Otherwise, just proceed directly to the next step.

6. Open up your browser and point it to `localhost:4200` and you should see something like this after a moment:

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e2e530425915e6a073dfdcafb6abe52e/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/result2.png)

As you can see, results are now populating on your screen.

7. If you use the developer tools for your particular browser and open up the JavaScript console, you'll notice there are some errors with what's happening right now.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/79abf64f082e426fbe18ca44a56ecae6/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/errors.png)

This is occurring because Angular is trying to read from the items array when there is no response currently present. In order to solve for this problem, we are going to use the ngIf directive to only show this entire template when the `searchResults` data is available.

8. Let's wrap the entirety of our current template, including the header with the total count of results, in a `<div>` and apply the `ngIf` directive to it.

```html
<div *ngIf="searchResults;">
  <h3>Total Results: {{searchResults.total_count}}</h3>
  <ul>
    <li *ngFor="let result of searchResults.items">
      <a [href]="result.html_url">
        <img [src]="result.owner.avatar_url" /> 
        <h4>{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p> {{result.description}}</p> 
    </li>
  </ul>
</div>
```

This will make the whole block only render once `searchResults` is available, eliminating the error we saw previously.

9. One of the features of ngIf is the ability to include a template to be used in the inverse condition of the `ngIf`, essentially an else to ngIf. In order to do this, add an else statement with a hashed ID after the first statement in `ngIf`, then apply that hashed ID to an `ng-template` tag after your initial block.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3>Total Results: {{searchResults.total_count}}</h3>
  <ul>
    <li *ngFor="let result of searchResults.items">
      <a [href]="result.html_url">
        <img [src]="result.owner.avatar_url" /> 
        <h4>{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p> {{result.description}}</p> 
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

You can nest any HTML you'd like within the else block, we are just using the text "Loading…".

**Note:** some connections may be too quick to see the “loading…” string before the data is displayed.

That's it! You've successfully used Structural Directives to shape the way your template is built. 

## To Use CSS and ngStyle

Now that we have our template created and displaying data, it's time for us to add a bit of style to it. To do this we are going to use two different tools: the scoped CSS file linked to our template and the ngStyle built in directive.

1. First we need to apply some css classes to the HTML in our template. Go ahead and open up the `git-search.component.html` file in Visual Studio Code. 

2. Let's add a **total** class to the `<h3>` tag, a **list** class to the `<ul>` tag, a **list_item** class to the `<li>` tag, an **avatar** class to the `<img>` tag, a **title** class to the `<h4>` tag, and finally a description class to the `<p>` tag.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li class="list_item" *ngFor="let result of searchResults.items">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p> 
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

We will use these classes to apply styles to the HTML elements.

3. Now let's open up our `git-search.component.css` file. You can see that it is currently empty. CSS that we add into this file will automatically be injected into our component, and will also be specifically scoped to it - which means that even if you use similar classes or element rules across multiple component CSS files, they will not overlap.

4. Let's add some styles to this file. Go ahead and copy the CSS below and paste it into your file.

```css
.total {
    font-size:24px;
}
.list {
    list-style-type: none;
}
.list_item {
    border:1px solid black;
    height: 165px;
    margin-top: 20px;
    padding-top: 10px;
    padding-left: 10px;
}
.avatar {
    width:150px;
    height:150px;
    float:left;
}
.title {
    font-size:20px;
}
.description {
    font-size:18px;
}
```

5. Next we're going to use `ngStyle` to apply a style to your template conditionally. First we want to add the index property to our `ngFor` so we can use the `index` in our `ngStyle`. To do that, add an i`ndex as i;` statement after your `let result of searchResults.items;` statement. The outcome of this statement is that the variable `i` will be set to `0` the first time through the loop, then incremented to `1` and so on.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li class="list_item" *ngFor="let result of searchResults.items; index as i;">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p> 
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

Note the semicolons separating the statements. This is important when using multiple statements in the same directive such as `ngFor`.

6. Now that we have the `index`, let's apply a style that will vary the background color based on if the row is even or odd. To do this, we add an object to the `ngStyle `directive on our `<li>` tag.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li [ngStyle]="{'background-color' : (i % 2 === 0) ? 'silver' : 'white'}" class="list_item" *ngFor="let result of searchResults.items; index as i;">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p> 
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

Note that there's a ternary expression for the value of `background-color`. Values set in `ngStyle` can be in the form of a JavaScript expression, and the ternary is a good way to set up a quick two-way switch based on a variable, in this case switching on whether the modulus of the index of the repeated element when divided by 2 is 0 (indicating an even number).

5. Save the file, and then, if your app is not already running: open up your terminal or command prompt, navigate to your `angular-fundamentals` folder, and use `ng serve` to start your app.

Open up a browser and navigate to `localhost:4200` and you should see the following.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/89a91c812767cf4ce07e5f7fe5aeb5c4/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/result3.png)

And there you have it! You have successfully applied styles using the scoped component CSS and the built-in directive ngStyle.

## To Use Built In Pipes

In this lab, we are going to do two things: apply built-in Pipes to our Angular template to further transform the data output, and use the `ngModel` built-in directive to create a search input for our application to be able to send custom queries.

We are going to work with a couple of built-in Pipes in Angular: the `date` pipe and the `uppercase` pipe.

1. Open up your `src/app/git-search/git-search.component.html` file in Visual Studio Code. 

2. Next we are going to add an additional field from the `GitSearch` output, `created_at`, below the description.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li [ngStyle]="{'background-color' : (i % 2 === 0) ? 'silver' : 'white'}" class="list_item" *ngFor="let result of searchResults.items; index as i;">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p>
      <p> Created On: {{result.created_at}} </p>
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

3. Now we are going to apply a `date` pipe to our `result.created_at` binding. To do so, you add the pipe or `|` character after your binding, followed by the pipe command, which in this case will be `date:'fullDate'` to indicate that we want to format this as a full date.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li [ngStyle]="{'background-color' : (i % 2 === 0) ? 'silver' : 'white'}" class="list_item" *ngFor="let result of searchResults.items; index as i;">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p> 
      <p> Created On: {{result.created_at | date:'fullDate'}} </p>
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

4. Now let's add an uppercase pipe to our repository owner's names in the same fashion, by adding a `|` followed by `uppercase` after the template binding.

```html
<div *ngIf="searchResults; else elseBlock">
  <h3 class="total">Total Results: {{searchResults.total_count}}</h3>
  <ul class="list">
    <li [ngStyle]="{'background-color' : (i % 2 === 0) ? 'silver' : 'white'}" class="list_item" *ngFor="let result of searchResults.items; index as i;">
      <a [href]="result.html_url">
        <img class="avatar" [src]="result.owner.avatar_url" /> 
        <h4 class="title">{{result.name}} 
          <small> by {{result.owner.login | uppercase}}</small> 
        </h4>
      </a> 
      <p class="description"> {{result.description}}</p> 
      <p> Created On: {{result.created_at | date:'fullDate'}} </p>
    </li>
  </ul>
</div>
<ng-template #elseBlock>Loading...</ng-template>
```

5. Save the file, and then, if your app is not already running: open up your terminal or command prompt, navigate to your angular-fundamentals folder, and use `ng serve` to start your app.

6. Open up a browser and navigate to `localhost:4200` and you should see the following.

![alt text](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/e0b559bd8f0cf593a7c8f40816e27b13/asset-v1:Microsoft+DEV314x+1T2019a+type@asset+block/M3L9result1.png)

Congratulations! You have implemented Pipes in your templates. You can see that the date is now formatted properly, and that the user's name is capitalized.

