ES6 Promises - Javascript
![image](https://github.com/iNtoko/alx-backend-javascript/assets/122923725/55b9d821-0cdb-44f1-b424-faba24d4c24a)


A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.read more

Learning Objectives
Promises (how, why, and what)
How to use the then, resolve, catch methods
How to use every method of the Promise object
Throw / Try
The await operator
How to use an async function
Get a quick idea about the subject matter
Introduction to Javascript Promise
The await keyword in Js
async in Js
Try /Throw in Js
Requirements
All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
Allowed editors: vi, vim, emacs, Visual Studio Code
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the js extension
Your code will be tested using Jest and the command npm run test
Your code will be verified against lint using ESLint
All of your functions must be exported
Installation Breakdown
Machine ubuntu 18.04 LTS To install node on your ubuntu machine
$ sudo apt-get install -y nodejs
NodeJs v12.22.12
npm v6.14.16
insatalling jest, babel, eslint
$ npm install --save-dev eslint jest
$ npm install --save-dev babel-jest @babel/core @babel/preset-env @babel/cli
create a file called package.json then copy-paste the following code
{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
    "eslint": "^6.4.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}
create a file called babel.config.js then copy paste the following code
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
copy paste this into a file utils.js
export function uploadPhoto() {
  return Promise.resolve({
    status: 200,
    body: 'photo-profile-1',
  });
}


export function createUser() {
  return Promise.resolve({
    firstName: 'Guillaume',
    lastName: 'Salva',
  });
}
copy-paste this in a file called .eslintrc.js
