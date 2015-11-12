# impress.js Demo Presentation

This is an [impress.js](http://impress.github.io/impress.js) slide presentation demo

[View the presentation online](http://marinels.github.io/presentations/impress-test)

### About

This presentation was created using the [impress yeoman generator](https://github.com/slara/generator-impress).

`npm install -g yo generator-impress grunt`

### How to Add a Slide

Slides can be added using yeoman commands. The simplest method of adding a slide is the following:

`yo reveal:step "Slide Title"`

Slide content is stored in the `steps` directory using a *one file per slide* convention. The `steps/list.json` file describes the structure and configuration of the presentation.

### How to Test

Testing locally requires installing the node and bower packages, then serving the files locally using grunt.

`npm install && bower install && grunt server`
