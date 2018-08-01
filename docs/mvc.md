---
id: mvc
title: Structure your project with MVC
sidebar_label: MVC structure
---
>*We covered a lot of topics with the javascript language until now but we didn't talk about the architecture of your project which is something really important, as a developer you will be most of the time working with others developers and it's really important to define a good structure to your project so that everyone can easily understand what you want a do. For that we will use the famous MVC structure which is (model, view and controller).*

A lot of projects use tools to immediately generate a structure for your app like the `create-react-app` npm package for example, and a lot of them use the MVC structure who consist to create folders and sub-folders to correctly organize your application.

MVC stands for Model, View, Controller and if you search for MVC in google you will probably see a lot of ways to implement this structure but for this section we will simply use a definition of each terms and let you organize your own MVC structure as you want.

Today thank's to ES6 modules it's really easy to implement this kind of structure.

## Model
The Model will be organize by component for example each component of your website will have his own Model, his works is to receive data and send it to the Controller.

## View
The View will also be organize by components for example your header will have his own View file, same for your footer etc..

His works is to display your component with the different data from the Controller, View files doesn't interact directly with Model file this is why we implement a Controller to do the link between them.

## Controller
The Controller will be an `index.js` file who is charged to do the link between the Model and the View.

His works is to receive information's from a Model component and treat this information's to send it to the View component.


## Current errors
This is a list of the main errors that you can meet when you use MVC structure:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.