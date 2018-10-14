Debounce example

## Installation
`npm i debounce-example@1.0.0`

## Usage
`import debounce from 'debounce-example';`

## Parameters

### debounce(fn, time)

| Parameter name  | Value | required |
| ------------- | ------------- | ------------- |
| fn - `function` | Contains function to be executed  | yes |
| time - `Number` | Indicates time to executed the function | yes |

## About
The debounce function helps to manage time of execution your scripts. You can use this function to disabled multiple execution of some function. For example:
 - When you use a form to sent some data, and you need to prevent multiple call to the endpoint registration.

 ```js
 import debounce from 'debounce-example';
 // Some function
 const myAwesomeRegistrationLogin = () => {
   fetch('http://my.api/user/registration', {
     method: 'POST',
     data: {name, email}
   }).then(() => someNotification('Success registration'));
 };

document.getElementById('registration--button').on('click', () => {
   debounce(myAwesomeRegistrationLogin, 5000);
});

```
