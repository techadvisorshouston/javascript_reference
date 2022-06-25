# Javascript Form Validation
**Example of client side form validation using Javascript. Should be used in conjunction with Server side validation to ensure the form and it's input values are secure.**

<br>

## Set the Form inputs to variables
**Makes referring to each element easier in the script**

````javascript
let username = document.forms["FORM_ID"]["USERNAME"];
let email = document.forms["FORM_ID"]["EMAIL"];
let mobile = document.forms["FORM_ID"]["MOBILE"];
let pass = document.forms["FORM_ID"]["PASSWORD"];
let confirm = document.forms["FORM_ID"]["CONFIRM_PASS"];
```` 

## Check for empty values. 
**If any of the fields are empty, show an alertbox and focus on the element. Also returns false to keep the form from being submitted.**

````javascript
if (username.value == "") {
  alert("Please enter a Username.");
  username.focus();
  return false;
}
if (email.value == "") {
  alert("Please enter your Email Address.");
  email.focus();
  return false;
}
if (mobile.value == "") {
  alert("Please enter your Mobile Number.");
  mobile.focus();
  return false;
}
if (pass.value == "") {
  alert("Please enter a Password.");
  pass.focus();
  return false;
}
if (confirm.value == "") {
  alert("You must confirm your password.");
  confirm.focus();
  return false;
}
if (confirm != pass){
  alert("Passwords do not match!");
  confirm.focus();
  return false;
}
  return true;
}
````

<br>

# Full Script
**validation.js**
````javascript
let username = document.forms["FORM_ID"]["USERNAME"];
let email = document.forms["FORM_ID"]["EMAIL"];
let mobile = document.forms["FORM_ID"]["MOBILE"];
let pass = document.forms["FORM_ID"]["PASSWORD"];
let confirm = document.forms["FORM_ID"]["CONFIRM_PASS"];

if (username.value == "") {
  alert("Please enter a Username.");
  username.focus();
  return false;
}
if (email.value == "") {
  alert("Please enter your Email Address.");
  email.focus();
  return false;
}
if (mobile.value == "") {
  alert("Please enter your Mobile Number.");
  mobile.focus();
  return false;
}
if (pass.value == "") {
  alert("Please enter a Password.");
  pass.focus();
  return false;
}
if (confirm.value == "") {
  alert("You must confirm your password.");
  confirm.focus();
  return false;
}
if (confirm != pass){
  alert("Passwords do not match!");
  confirm.focus();
  return false;
}
  return true;
}
````

# Reference
**The code used in this script was inspired by a tutorial on W3docs.**
Here is a link to the original tutorial <a href="https://www.w3docs.com/snippets/javascript/form-validation-using-javascript.html">Form Validation using Javascript</a>
