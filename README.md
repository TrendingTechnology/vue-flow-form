# Vue Flow Form

Create conversational conditional-logic forms with Vue.js.

<p align="center">
  <img src="https://www.ditdot.hr/demo/vff/visuals/v-form-green-full-rotate-02.png" alt="v-form screenshots">
</p>

## Demo

* [Questionnaire example](https://www.ditdot.hr/demo/vff/questionnaire/)
* [Quiz example](https://www.ditdot.hr/demo/vff/quiz/)

## Example Project

Requirements:

* [Node.js](https://nodejs.org/en/) version 8.9 or above (8.11.0+ recommended)
* [npm](https://www.npmjs.com/get-npm) version 3+ (or [yarn](https://yarnpkg.com/lang/en/docs/install/) version 1.16+)
* [Git](https://git-scm.com/)

After checking the prerequisites, follow these simple steps to install and use Vue Form:

```shell
# clone the repo
$ git clone https://github.com/ditdot-dev/vue-flow-form.git myproject

# go into app's directory and install dependencies:
$ cd myproject
```

If you use npm:

```shell
$ npm install

# serve with hot reload at localhost:8080 by default.
$ npm run serve

# build for production
$ npm run build
```

If you use yarn:

```shell
$ yarn install

# serve with hot reload at localhost:8080 by default.
$ yarn serve

# build for production
$ yarn build
```

Made with [Vue.js](https://vuejs.org/)

## Usage as npm package

If you don't already have an existing Vue project, the easiest way to create one is to use [Vue CLI](https://cli.vuejs.org/):

```shell
$ npm install -g @vue/cli
# OR
$ yarn global add @vue/cli
```

And then create a project:

```shell
$ vue create my-project
$ cd my-project
```

To add Vue Flow Form as a dependency to your Vue project, use the following:

```shell
npm install @ditdot-dev/vue-flow-form --save
```

And then in your App.vue file:

```html
<template>
  <flow-form v-bind:questions="questions" />
</template>

<script>
  // Import necessary components and classes
  import FlowForm, { QuestionModel, QuestionType, ChoiceOption } from '@ditdot-dev/vue-flow-form'

  export default {
    name: 'example',
    components: {
      FlowForm
    },
    data() {
      return {
        questions: [
          // QuestioModel array
          new QuestionModel({
            question: '...',
            type: QuestionType.MultipleChoice,
            options: [
              new ChoiceOption({
                label: '...'
              })
            ]
          })
        ]
      }
    }
  }
</script>

<style>
  /* Import Vue Flow Form base CSS */
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.css';
  /* Import Vue Flow Form theme CSS (optional) */
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.theme.css';
</style>
```

## JavaScript via CDN

HTML:

```html
<html>
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.2.6/vue.min.js"></script>
    <!-- Flow Form -->
    <script src="https://unpkg.com/@ditdot-dev/vue-flow-form"></script>
    <!-- Flow Form base CSS -->
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form/dist/vue-flow-form.min.css">
    <!-- Optional theme.css -->
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form/dist/vue-flow-form.theme.css">
  </head>
  <body>
    <div id="app">
      <flow-form v-bind:questions="questions" />
    </div>
  </body>
</html>
```

JavaScript:

```js
var app = new Vue({
  el: '#app',
  data: function() {
    return {
      questions: [
        new FlowForm.QuestionModel({
          question: '...',
          type: FlowForm.QuestionType.MultipleChoice,
          options: [
            new FlowForm.ChoiceOption({
              label: '...'
            })
          ]
        })
      ]
    }
  }
});
```
## Browser Support

Modern browsers and IE11.

## Project Documentation

[Guide](https://www.ditdot.hr/en/docs/vue-flow-form-guide)

## License

[MIT](https://github.com/ditdot-dev/vue-flow-form/blob/master/LICENSE) license.
