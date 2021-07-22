## TaxDown mobile challenge


### About the position 📱

Being a **Mobile Engineer**  means that you know what are the best approaches and solutions to native application implementations in both iOS and Android.
To complete that task, we are going to use **React Native** as our main framework as it lets our app to be hybrid, so we can install them in all kind of devices (yay! 🙌).

So we are going to test that and see how good of a developer you are regarding a mobile application project! 🔥

### Take me to the challenge! 🤟

In this challenge you'll be using **React Native** to create an app.

## What we are looking for 🤓

- App organization
- Apply SOLID principles
- Abstraction for external libraries
- Code testing
- Route managment
- Store and side effects managment


#### First step 🥇

The first step is to create a simple login form, something basic but functional. It will use the logo.svg that is located in the assets folder of this repository.

It would be great if we can persist the user's session so that when we re-enter the app, we won't log in again.

#### Second step 🥈

Once logged in, we will enter the dashboard, it will be a screen that shows a list with the results of a call to an endpoint with the following structure:

(This API could be a fake API created for example with ***json-server*** or similars)

```
/taxes

{
	"taxes":  [
		{
			"id": "1",
			"name": "Tax season 2020",
			"year": "2020",
			"active": true,
		},
		{
			"id": "2",
			"name": "Tax season 2019",
			"year": "2019",
			"active": false,
		},
		{
			"id":  "3",
			"name": "Tax season 2018",
			"year": "2018",
			"active": false,
		},
	]
}
```

In this screen we will have the results in two **tabs** one tab will show us the active taxes and another the inactive ones.

*In the dashboard we will have a share button my app to show everyone how cool our application is 💯 (this share will be the native of the phone, both for android and ios)*


#### Third step 🥉

Each element of the list will contain a button that will allow us to add submissions to that tax.

If we click on this button, it will take us to another screen where we have to request an api by id of the selected tax and it will return a structure like this:

```
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
		{
			"id":  "picture",
			"label":  "Picture",
			"type":  "picture",
		}
	]
}
```

We can have a * picture * field that will render a button that if we press it will open the phone's camera and allow us to save the path of the image we capture.

On this screen, a dynamic form should be rendered based on the inputs defined in the JSON response.

When we complete the inputs and give in submit, we will make a POST request to */tax/{id}/form* with the values ​​of the form.

We will also create a list of submissions in our store for that specific tax.

Note: We may have submissions lists for the different taxes.

#### Four step 🏆

Finally, we will have a screen where we can view all our tax submissions and we can filter both by tax year, and by name, surname and age.

*Optional: On the list screen we can delete each of the submissions.*

Easy and simple no? **So we are done!** 🚀!

### How can I share my solution?

I guess you used Git all the way here and made a few commits already, so how about creating a private repo and inviting us?

This way, we can review your code and have it at hand for the next step, a personal interview! 👻

Check who you should share it with:

https://github.com/TaxDownAutomation/coding-challenge

Good luck with the challenge! Enjoy it and do your best!
