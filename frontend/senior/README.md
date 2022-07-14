
# TaxDown frontend challenge

## About the position 💻

Being a **Frontend Engineer** means that you know how to apply the best solutions to the problems that can appear in the client of a Web Application (don't forget about the communication with backend services!).
So we are going to test that and see how good of a developer you are regarding the frontend part of a project! 🔥

## Take me to the challenge! 🤟

In this challenge (wont be long, we promise), you'll be using **React** to create a SPA.

# What we are looking for

- Structure organization
- Component based Architecture
- Apply SOLID principles
- Abstraction for external libraries
- Store managment
- Route managment
- Code testing

We use webpack like bundler so it's important that the project make use of it, you are free to use another bundler (the use of webpack will be a plus!).

## First step 🥇

First, you have to create a login form that allows a user to access the application.

Once logged in, the application will show a dashboard with a list of active user taxes. The information of these taxes will be obtained from a fake API built with **json-server** or similar.
<https://github.com/typicode/json-server>

``` json
endpoint: /taxes

{
 "taxes":  [
  {
   "id":  "1",
   "name":  "Tax Season 2021",
   "year": "2021",
  },
  {
   "id":  "2",
   "name":  "Tax Season 2020",
   "year": "2020",
  },
 ]
}

```

The information obtained from the API must be stored in the store using **Redux**, the use of middleware such as **Redux Saga** for handling asynchronous side effects will be a plus.

## Second step 🥈

Each tax will contain a button that will allow adding submissions.

When the button is clicked, it will take you to a new screen where a request will be made to the fake API to obtain a list of inputs.

``` json
/taxes/{id}/form
{
 "inputFields":  [
  {
   "id":  "name",
   "label":  "Name",
   "placeholder":  "Your first name",
   "type":  "text",
   "maxLength":  20
  },
  {
   "id":  "surname",
   "label":  "Surname",
   "placeholder":  "Your last name",
   "type":  "text",
   "maxLength":  40
  },
  {
   "id":  "age",
   "label":  "Age",
   "placeholder":  "Your age",
   "type":  "number",
  }
 ]
}
```

Here, a dynamic form should be rendered based on the inputs defined in the JSON response.

Remember that some fields may have validations in their keys (`maxLength` for the text inputs) and they can increase or change in the future.

## Third  step 🥉 (These medals should go from bronce to gold)

When the inputs are completed and the user clicks on submit button a POST request to **/taxes/{id}/form** with the values of the form will be made.

A list of submissions should be created in the store for that specific tax.

**Note**: _It will be submissions lists for the different taxes_.

All submissions by mapping them so we can see the key/value pairs introduced by the user.

Would be a screen where will be showed the taxes submissions and where the user can filter by tax year, name, surname and age

``` yaml
 Tax: 2021
  Submission 1
   Name: Bruce
   Surname: Wayne
   Age: 26
  Submission 2
   Name: Clark
   Surname: Kent
   Age: 22
```

And last but not least, it would be great if you added one or two **tests** to check for render stability or proper mapping of values ⭐️. We use **jest** and **react-testing-library** to testing.

Easy and simple no? **So we are done!** 🚀!

## Optional

Add the option to edit and delete each submission.

## How can I share my solution?

I guess you used Git all the way here and made a few commits already, so how about creating a private repo and inviting us [Fernán Ramos](https://github.com/Fernan-Ramos)

This way, we can review your code and have it at hand for the next step, a personal interview! 👻

Good luck with the challenge! Enjoy it and do your best!
