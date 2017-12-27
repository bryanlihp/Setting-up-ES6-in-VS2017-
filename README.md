# Setting-up-ES6-in-VS2017

https://www.slightedgecoder.com/2017/05/22/setting-es6-environment-asp-net-mvc-5/

1. NPM configuration and packages
   GO to project folder and run:
      npm init -y
   This will create package.json in project folder.
2. Install Webpack and Babel
      npm install --save-dev webpack babel-core babel-loader babel-polyfill babel-preset-es2015
3. Add package.json to the project.
    The "devDependencises" section in this file has references to Babel and Webpack. 
4. Create ES6 files for testing
   * person.js
   export default class Person { 
     constructor(name, age) { 
       this.name = name; 
       this.age = age; 
     } 
   
     speak() { 
       console.log(`Hi I'm ${this.name} and ${this.age} years old and I am awesome`); 
     } 
   }
  * main.js
    import Person from './person'; 
    var person = new Person("David", 20); 
    person.speak();
5. Config Webpack
    Create 
