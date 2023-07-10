# Tiago Professional Page

### My professional page to share my skills, projects and professional contact with interested parties.

![alt text for screen readers](/static/readme/responsive_screenshoot.png "Text to show on mouseover")

## Content

1. [Installation](#1-resume) <br/>
2. [Structure](#2-structure) <br/>
3. [Components](#3-components) <br/>
   3.1. [AboutMe.vue](#31-aboutmevue) <br/>
   3.2. [Badge.vue](#32-badgevue) <br/>
   3.3. [Contact.vue](#33-contactvue) <br/>
   3.4. [Dialog.vue](#34-dialogvue) <br/>
   3.5. [Footer.vue](#35-footervue) <br/>
   3.6. [MenuBar.vue](#36-menubarvue) <br/>
   3.7. [Projects.vue](#37-projectsvue) <br/>
   3.8. [Skills.vue](#38-skillsvue) <br/> 
4. [Layouts](#4-layouts) <br/>
   4.1. [defaul.vue](#41-defaultvue) <br/> 
   4.2. [error.vue](#42-errorvue) <br/> 
5. [Pages](#5-pages) <br/>
   5.1. [index.vue](#51-indexvue) <br/> 
6. [Static](#6-static) <br/>
   3.8. [avatar](#61-avatar) <br/> 
   3.8. [contact](#62-contact) <br/> 
   3.8. [projects](#63-projects) <br/> 
   3.8. [readme](#64-readme) <br/> 
7. [Frameworks and Libraries ](#7-technologies-used) <br/>   



## 1. Resume
This page was developed with the aim of briefly highlighting who I am professionally, my experience and skills. The page was basically developed using VueJs and frameworks.

## 2. Structure

├── **assets** <br/>
│ ├── **variables.scss** <br/>
├── **components** <br/>
│ ├── **AboutMe.vue** <br/>
│ ├── **Badge.vue** <br/>
│ ├── **Contact.vue** <br/>
│ ├── **Dialog.vue** <br/>
│ ├── **Footer.vue** <br/>
│ ├── **MenuBar.vue** <br/>
│ ├── **Projects.vue** <br/>
│ ├── **Skills.vue** <br/>
├── **layouts** <br/>
│ ├── **default.vue** <br/>
│ ├── **error.vue** <br/>
├── **pages** <br/>
│ ├── **index.vue** <br/>
├── **static** <br/>
│ ├── **avatar** <br/>
│ │ ├── **avatar2.js** <br/>
│ ├── **contact** <br/>
│ │ ├── **contact.png** <br/>
│ ├── **projects** <br/>
│ │ ├── **logoLuna.svg** <br/>
│ │ ├── **tiago-profile.png** <br/>
│ ├── **readme** <br/>
│ │ ├── **responsive_screenshoot.png** <br/>
│ ├── **mb.ico** <br/>
├── **store** <br/>
│ ├── **README.md** <br/>
├── **.editorconfig** <br/>
├── **.gitignore** <br/>
├── **nuxt.config.js** <br/>
├── **package-lock.json** <br/>
├── **package.json** <br/>
├── **README.md** <br/>
├── **tsconfig.json** <br/>

## 3. Components

### 3.1. AboutMe.vue

Component that makes up the "Home" section in index.vue. It basically contains name, title and a brief professional introduction.

### 3.2. Badge.vue

Component that contains the layout of the buttons used to populate the skills section. This component is used inside the Skills.vue component.

### 3.3. Contact.vue

Component that makes up the "Get in touch" section in index.vue. It basically provides all means of contact.

### 3.4. Dialog.vue

Dialog Component responsible for copying the contact e-mail to the Clip Board and sending an informative message to the user.

### 3.5. Footer.vue

Component that makes up the footer of the page. Invoked in Default.vue

### 3.6. MenuBar.vue

Component that makes up the options menu. It has two modes, one for small and up screens and one for extra small screens.

## 3.7. Projects.vue

Component that makes up the projects section in index.vue. Basically it has all the projects developed and the option to access github and the website.

## 3.8. Skills.vue

Component that makes up the Skills section in index.vue. basically includes all mastered languages, libraries and frameworks.

## 4. Layouts

### 4.1. Default.vue

Contains the default site structure. Here the positions of the menu bar, footer and background are defined.


### 4.2. Error.vue 

Error page layout returned when an error is found in the source code.

## 5. Pages

### 5.1. Index.vue

Root file containing the home page structure. Basically constituted by 4 droughts. Are they:
- Home (or Abour Me)
- Skills
- Projects
- Contact

## 6. Static

### 6.1. Avatar

Photo used in the Avatar component in the home or about me section.

### 6.2. Contact 

Image used in the Get in touch section.

### 6.3. Projects

Illustrative images of the developed projects.

### 6.4. Readme

Image attached in the README used to illustrate how responsive the site is.

## 7. Frameworks and Libraries used

- Nuxt 2
- Vuetify 2
- CSS
- TypeScript


