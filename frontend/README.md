## TaxDown frontend challenge


### About the position 💻

Being a **Frontend Engineer** means that you know how to apply the best solutions to the problems that can appear in the client of a Web Application  (don't forget about the communication with backend services!).
So we are going to test that and see how good of a developer you are regarding the frontend part of a project! 🔥

### Take me to the challenge! 🤟

In this challenge (wont be long, we promise), you'll be using **React** to create a SPA that renders a form given an input in the form a JSON file.

To create the project, you can use **create react app** for speed! 🏎

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

And now that you have some hooks around, let's store all our submissions into a global state in our application.

```
	// exampleState.js

	const state = {
		submissions: [], // Insert the submissions in this attribute
	}
```

How can I do this? You have a good variety of options, so go with the one you feel more comfortable with. Here are some examples:

 - **Don't you have much time?** Go with a state in your App component and update that one. Be careful with the **prop drilling**!  (Psst, `useReducer` can be a good approach for this).
 - **Are you familiar with hooks?** How about simulating the Redux pattern using `useContext`? Think about how this could affect our app life cycle.
 - **Did you use Redux before?** Just use Redux so we know how far can you go, or some similar library (MobX, ReactN, easy-peasy...).

Remember to **use the one you feel more comfortable with**, don't waste your time going crazy on this, we just want to see how you are structuring the code and how clean it is!

#### Third  step 🥉 (These medals should go from bronce to gold)

Last step and we are done! We are saving our submissions in the state, so let's go and show them in a list of some kind!

You can use **React Router** to create a new route with the list and one with the form we created before.

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

Joaquín Fernandez - [https://github.com/JoaquinFernandez](https://github.com/JoaquinFernandez)
Cristian Castillo - [https://github.com/Ccastillo06](https://github.com/Ccastillo06)

This way, we can review your code and have it at hand for the next step, a personal interview! 👻

Good luck with the challenge! Enjoy it and do your best! 
