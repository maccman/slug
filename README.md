#Introduction

Slug is a project for compiling CommonJS modules. 

#Commands

* `slug new`    - generate new slug
* `slug server` - host slug server (for development)
* `slug static` - host static slug server (for production)
* `slug build`  - build slug in ./build dir, minimize

Slug would be in charge of collecting all third-party dependencies (listed in slug.json) and injecting them as CommonJS modules / CSS / assets.

When it comes to deployment you'd do:

    slug build
    git add ./build
    git commit -m 'version x'
    git push heroku master

Or if you were building a PhoneGap application:

    slug build
    phonegap --ios ./build