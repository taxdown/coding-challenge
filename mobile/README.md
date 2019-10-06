## TaxDown mobile challenge


### About the position 📱

Being a **Mobile Engineer**  means that you know what are the best approaches and solutions to native application implementations in both iOS and Android.
To complete that task, we are going to use **React Native** as our main framework as it lets our app to be hybrid, so we can install them in all kind of devices (yay! 🙌).

So we are going to test that and see how good of a developer you are regarding a mobile application project! 🔥

### Take me to the challenge! 🤟

In this challenge (wont be long, we promise), you'll be using **React Native** to create an app that renders a form given an input in the form a JSON file.

To create the project, you can use **react-native init** for speed! 🏎

*It would be great if the app runs smoothly in iOS, because that's where we are mainly going to test it.

Here's the sample JSON file you can use to complete the exercise:

```
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

Just create it and import in your files, it will appear as an object!

#### First step 🥇

The form should be able to grow in size depending on the new input given in that file (imagine we have an API that provides these values).

After showing the form, let the user fill the fields and submit the answer (a `console.log()` should be enough to show it).

Remember that some fields may have validations in their keys (`maxLength` for the text inputs) and they can increase or change in the future.

PS: Don't forget to give it some style (not too crazy, just make it look nice)!

#### Second step 🥈

We got the form running and submitting our data! So now what?

We are using the latest React APIs in our projects, so you'll have to face **Context and Hooks** in your daily life with us. Did you use class components? Let's make them into functional ones and use hooks to handle the state properly! 💪

PS: **If you don't feel like using hooks** and prefer class components, keep them like that, but remember, write a comment about why it's preferred to keep the class ones and we will talk about that in the next interview we have! It's great to talk and find different solutions to coding challenges!

And now that you have some hooks around, let's store all our submissions into a global state in our application.

```
	// exampleState.js

	const state = {
		submissions: [], // Insert the submissions in this attribute
	}
```

How can I do this? We know this is just a challenge and using **Redux** is overkill for little projects, but as an application grows over time, it's practically necessary to keep a global store with our app state.

That's why it will be really valuable for us to see how you handle yourself when applying **Redux** in this app.

Remember that we are going to keep the submissions made in the store, so why not introduce the form fields in there too? That way our app will have one source of truth for the forms too.

```
	// exampleState.js

	const state = {
		submissions: [], // Insert the submissions in this attribute
		formFields: [], // Insert the form fields received from the JSON file
	}
```

#### Third  step 🥉 (These medals should go from bronce to gold)

Last step and we are done! We are saving our submissions in the state, so let's go and show them in a list of some kind!

You can use **React Navigation** to create a new route with the list, and one with the form we created before.

In the new **List** route, show all submissions by mapping them so we can see the key/value pairs introduced by the user.

```
	Submission 1
		Name: Bruce
		Surname: Wayne
		Age: 26
	Submission 2
		Name: Clark
		Surname: Kent
		Age: 22
```

And last but not least, it would be great if you added one or two **tests** to check for render stability or proper mapping of values ⭐️.

Easy and simple no? **So we are done!** 🚀!

### How can I share my solution?

I guess you used Git all the way here and made a few commits already, so how about creating a private repo and inviting us?

This way, we can review your code and have it at hand for the next step, a personal interview! 👻

Check who you should share it with:

https://github.com/TaxDownAutomation/coding-challenge

Good luck with the challenge! Enjoy it and do your best!
