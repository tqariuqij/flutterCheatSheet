# Flutter Cheat Sheet

**This is a guide to the basics of flutter**

## Installation guide

[The flutter Docs](https://flutter.dev/)

Also DartPad allows you to edit and run flutter code on the browser.

## Getting started.

Once installed you can run `flutter create myfirstapp` on the terminal to spin up a new app.

If using vscode make sure you have installed the dart and flutter extensions to make your life easier.

Next choose the emulator and then run `flutter run` to start the app.

## Understanding Flutter

The basic principle that flutter is build upon takes inspiration from react. For UI the building blocks are [widgets](https://docs.flutter.dev/ui/widgets). The widget has a description of what needs to be rendered and the state, when this change the framework makes a differentiation from what it had previously and what it has now in order to make as few changes as possible thereby making this fast.

## Keyboard shortcuts

**In terminal**

r => hot reload
R => hot reload of entire build

**In code**

## Creating your first app

**The main function**

This is the starting point of any flutter app.

```
void main(){
    runApp(MyApp() );
}
```

Takes a single widget as an argument and inflates it to any device that the project is running on

## MaterialApp

The `import 'package:flutter/material.dart'` gives you access to hundreds of pre-built widgets. You use this to combine them to a tree like structure that will be your UI.

## StatelessWidget

This is a widget with no dynamic data. That is a dum widget.

It has a build method which takes in some build context as an argument. This method is called any time flutter needs to rebuild the UI. It returns some widget.

## Scaffold

This allows us to build screens with common ui elements like a appBar, texts, buttons etc.

Every pre-built widget has a bunch of named parameters where you can customize its appearance. Hit ctrl + space while cursor in widget brackets to see them.

## Container.

The layout, or the way you will arrange widgets in a screen, is commonly done using a Container as the base widget. This is equivalent to a div in HTML.

This takes ONE child widget as an parameter, and css-like properties to customise how it will look i.e

```
//...we are in widget

body: Container(
    child: const Text('I love flutter'),
    margin: const EdgeInsets.all(100),
    padding: const EdgeInsets.all(10),
    color: Colors.blue,
    height: 100,
    width: 100
)
```

### BoxDecoration property.

A more thorough way of styling a container is using a BoxDecoration property.
