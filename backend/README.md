# TaxDown backend challenge

## About the position

You will be building the backbone of TaxDown. Working shoulder to shoulder with other developers as well as the product team so we can grow and scale. Our business is tech and we build our core. 🔋

We love getting our hands dirty, we believe that a developer should understand all the code shipping process. You will be expected to write unit tests heavily, as well as own the *DevOps* of your projects. You can't know everything, but we expect you want to learn. 👓

If you love starting from scratch and dream with eradicating repetitive tasks, tag along!

## Take me to the challenge! 🤟

In this challenge (won't be long, we promise), you'll be using **Node.js** to create a service that will offer an API and will act as a gateway for our customers. It will handle calling third party services.

### First step 🌟

This service will allow a GET request on an endpoint of your choice. It will then call the following URL and return that response to the original request. The URL is:

<https://api.exchangeratesapi.io/latest>

The response from that service should have this format:

```json
{
    "rates":
      {
        "CAD":1.4722,
        "HKD":8.6889,
        ...
      },
    "base":"EUR",
    "date":"1852-12-28"
}
```

Feel free to use any modules or frameworks that you usually work with.

### Second step

We got the service running and working as expected! 🚀

Let's deploy it. What's the fun of developing something if no one can access it?

At TaxDown we use the serverless framework <https://serverless.com/>. If you are comfortable with it or want to learn, go for it! Otherwise, use whatever you feel comfortable with, but please remember that we should be able to clone the repo and replicate the environment.

👂 *Psst, remember to include instructions on how to deploy it*

### Third step

Prepare to be asked a lot of questions on your choices 😆

And last but not least, it would be great if you add tests. Easy and simple no? **So we are done!**

## How can I share my solution? 🔥

I guess you used Git all the way here and made a few commits already, so how about creating a private repo and inviting us?

Joaquin Fernandez - [https://github.com/JoaquinFernandez](https://github.com/JoaquinFernandez)  
Cristian Castillo - [https://github.com/Ccastillo06](https://github.com/Ccastillo06)

This way, we can review your code and have it at hand for the next step, a personal interview! 👻

Good luck with the challenge! Enjoy it and do your best!
