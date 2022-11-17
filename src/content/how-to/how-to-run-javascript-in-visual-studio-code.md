---
title: "How to run Javascript in Visual Studio Code?"
subtitle: "You can run Javascript in the Visual Studio Code through the terminal if you have node installed (node filename.js)."
date: "2022-09-08T16:36:30+00:00"
tags: ["javascript", "visual studio code"]
status: "draft"

---


To be able to run javascript in Visual Studio, we need to have installed NodeJs on our system and have a javascript file created with some content.

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_11.png)

Before being able to run javascript on Visual Code, we need to install Visual Studio Code and NodeJs. Visual Studio Code is the IDE (Integrated Development Environment) we will be using throughout the article and NodeJs is the engine that allows javascript to run locally.

## Installing Visual Studio Code

- Go to https://code.visualstudio.com/
- Download installer
- Run the installer
- Accept terms and conditions and next, next, next...

Visual Studio Code is ready to be used, but we still need NodeJs to run javascript locally

## Check if NodeJs is installed already and the version

- Open command prompt 
	- Start menu 
	- Write `cmd`
	- Open
- Type on the command windows `node -v `

If NodeJs is present in the system, you´ll see something like `v16.51.1` being that the installed version of Node.

## Installing NodeJs

- Go to https://nodejs.org
- Download the recommended version
- Run the installer
- Accept terms and conditions and next, next, next....

Now that we have NodeJs installed on our system, we can run javascript locally and Visual Studio as our IDE, but how to run javascript on Visual Studio?

## Let´s set up our Javascript project

- Start Visual Studio Code

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_1.png)

- Open a new `Terminal`

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_2.png)

- Write on the terminal `npm init -y`

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_3.png)

`npm` stands for `Node Package Manager`
`init` is the keyword for NodeJs to create a new project 
`-y` is to pass as a default all values

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_4.png)

- If successful, a `package.json` file will be created on your project folder

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_6.png)

- Right click on the file explorer (where the `package.json` is displayed) and select new file.
- We are naming it `app.js` (js is a javascript extension)

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_7.png)

- Now let´s write some javascript code on our `app.js` file.

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_8.png)

- Go on, write on the terminal: 
```bash
$node app
```
Remember to take out  the "$" 

And you´ll see on the terminal the `console.log()` message displayed. 

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_12.png)


Still, I prefer to do it another way, since it allows for a more robust and personalized way to run our `app.js` file.

Remember the `package.json` we created with `npm init -y`? Well, we are editing now. We will make that, every time we type `npm run start` on the Visual Studio terminal, it´ll execute our `app.js` file.

- Select `package.json` to edit it
- Add 
```json 
	"start" : "node app.js"
```
![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_9.png)

Careful! We added a `,` at the end of line 7, if the `,` is missing, the JSON format is not correct and will throw errors / won´t work.

Now, we can run our javascript project like this:

```bash 
	npm run start
	```

![How to run javascript on Visual Studio](../../assets/images/how_to_run_javascript_on_visual_11.png)