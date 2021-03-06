# UnityWebGL VueJS Boilerplate

This is a boilerplate **Unity WebGL** ++ **VueJS** web app with **VueX && **vue-router** pre-installed.

This project takes advantage of the Unity3d web container wrapper component provided by
@votetake's [vue-unity-webgl](https://github.com/votetake/vue-unity-webgl) Node package.

## Run in Dev

Install deps:
```
npm install
```

Spin up Node dev server:
```
npm run serve
```

## Directory Structure

`./public/Build` && `./public/TemplateData` - the templates/JS functions of a bare Unity3D WebGL project.

## Send a string from VueJS to the Unity Scene

The Unity scene contains only a lean 3D plane and a text object.

Text can be sent to the text object in the Unity game instance via the `@click` method in `./src/views/Home.vue`:

```JavaScript
// $refs.myInstance === <unity ref="myInstance">
this.$refs.myInstance.message('Text', 'SetText', this.textInput)
```

Note: Further configuration is needed to make the text input in `./src/views/Home.vue` editable after the Unity game loads,
since the Unity WebGL instance grabs all keyboard input to the page. There is an example string in the input box for this reason.

[Related Unity forum thread](https://forum.unity.com/threads/disable-enable-keyboard-in-runtime-webgl.286557/#post-1892527)

## Trigger a webpage JavaScript function from Unity Scene

[WIP] 

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
