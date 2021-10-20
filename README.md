# React-Three-MindAR Demo

A simple demo app for natural feature tracking using the excellent [MindAR library](https://github.com/hiukim/mind-ar-js/tree/master/) with ThreeJS.

![Demo video of simple cube scene](/public/ar-demo.gif)

## Description

The main part of the app can be found in the src/components/App.tsx file. In src/mind.d.ts you'll find a global declaration, since this project uses Typescript, to help with accessing the MindAR controller.

## Getting Started

### Installing
After grabbing the code:

```
npm i 

or

yarn i
```

### Running

```
npm start

or 

yarn start
```
The app immediately launches into the webcam and runs the MindAR controller setup. Give it a few seconds to warm up.

## Final Notes

* For the purpose of being simple, this demo doesn't support multi-nft capabilities. However, adding multiple markers shouldn't be much trouble after inspecting the code and referencing the [MindAR docs](https://hiukim.github.io/mind-ar-js-doc/) and the MindAR source. 
* All of the logic is in a single 'App' component. An improvement would be to lift state to multiple smaller components. For example, hook MindAR via a context provider. See [artcom/react-three-arjs](https://github.com/artcom/react-three-arjs) for a comprehensive example of what I mean. This pattern lends itself really well to multi-nft and also integration with the react-three-fiber package.
* I'm using a screenshot of the create-react-app landing-page logo as an image target. Generally, this was a poor decision. Square markers with low contrast and high symmetry act as terrible markers. You'll likely want to test out multiple different target images. You can use the [MindAR Compiler tool](https://hiukim.github.io/mind-ar-js-doc/tools/compile) to help you.