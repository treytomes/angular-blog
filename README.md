# `angular-blog` — Angular Blog Framework

## Synopsis

I am expanding my portfolio to include Angular.  The logical place for me to start is to create a blog.  In the real world, if I were wanting to setup a blog site for my company, I would install a WordPress server.  I'd probably use prepackaged 3rd-party components to link up the WordPress security with corporate security.  This is not the real world though; this is a place for me to show off that I actually know how to use this framework.

Here goes.

## User Features

* I should be able to create, read, update, and delete blog entries.
* I should be the only one allowed to make new blog entries.
* I'd like to be able to add and remove tags from blog entries.
* Anyone should be allowed to post comments to a blog entry.
* I should be able to delete comments as I see fit.
* There should be a text search that includes the titles, contents, and comments from all blog entries.
* I want to be able to filter blog entries based on one or more tags.
* Blog entries should be parsed in Markdown formet.

## Technical Features

I will be attempting to implement the MEAN stack.  It seems to be the most popular in AngularJS land:
* MongoDB
* ExpressJS
* Angular
* NodeJS

The data will be retrieved with a REST API created using Loopback.

The component hierarchy will probably look like this:
* blog-app
  * side-bar
    * security
    * search
      * Text entry that can be used to filter blog-entry-list.
    * category-list
      * List of categories that can be clicked to filter blog-entry-list.
  * blog-entry-list
    * create-blog
      * Only available if logged in.
    * blog-post
      * blog-header
        * blog-title
        * blog-author
        * blog-created-date
        * blog-updated-date
      * blog-contents
        * Markdown-formatted text.
      * blog-comment-list
        * blog-comment
          * comment-author
          * comment-date
          * comment-contents
          * Delete button, if logged in.
        * add-comment-form

## How to run

### Prerequisites

* You need git to clone this repository. You can get git from [http://git-scm.com/](http://git-scm.com/).
* We also use a number of node.js tools to initialize and test angular-seed. You must have node.js and its package manager (npm) installed.  You can get them from [http://nodejs.org/](http://nodejs.org/).

### Command-line

* ```git clone https://github.com/treytomes/angular-blog```
* ```cd angular-blog```
* ```npm start```

### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

Then open a browser to http://localhost:8000

## References

I used these to learn AngularJS:
* https://devcenter.heroku.com/articles/mean-apps-restful-api
* https://angular-templates.io/tutorials/about/learn-how-to-build-a-mean-stack-application
* https://docs.angularjs.org/tutorial
