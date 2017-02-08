# Intro to Reactive Programming Presentation

This is a [reveal.js](http://lab.hakim.se/reveal-js) slide presentation on the introduction to Reactive Programming.

[View the presentation online](http://marinels.github.io/presentations/rx-intro)

### How to Add a Slide

Slides can be added using yeoman commands. The simplest method of adding a slide is the following:

`yo reveal:slide "Slide Title" --notes --markdown`

Slide content is stored in the `slides` directory using a *one file per slide* convention. Image and other similar content are placed in the `resources` directory. The `list.json` file describes the structure and configuration of the presentation. Generic global and section level configuration can be applied to the respective files in the `templates` directory.

### How to Test

Testing locally requires installing the node and bower packages, then serving the files locally using grunt.

`npm install && npm run bower install && npm start`

### How to deploy

Reveal needs to scan the presentation configuration (`list.json`) and generate the entry point (`index.html`). Running the following command will generate the `index.html` file.

`npm run grunt buildIndex`
