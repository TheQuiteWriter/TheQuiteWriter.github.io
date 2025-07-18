# Cerebras.AI API Tutorial for JanitorAI

This Tutorial will walk you through:
+ **Step 1**: [Creating a free account on Cerebras.AI](#creating-a-free-account-on-cerebrasai)
+ **Step 2**: [Getting your API key](#getting-your-api-key)
+ **Step 3**: [Selecting a model](#selecting-a-model)
+ **Step 4**: [Using Cerebras.AI endpoint in JanitorAI](#using-cerebrasai-endpoint-in-janitorai)

I also made a [Troubleshooting Guide](#troubleshooting):
+ [How to know if a bot supports proxies?](#how-to-know-if-a-bot-supports-proxies)
+ [Why am I getting errors?](#why-am-i-getting-errors)

Just **read the tutorial carefully** before doing anything, I have made sure that this is the easiest way to get it working on JanitorAI quickly.

## About Cerebras.AI
**Cerebras Systems Inc.** is an **American artificial intelligence company** with offices in Sunnyvale, San Diego, Toronto, and Bangalore, India. Cerebras builds computer systems for complex AI deep learning applications. Of course, you're not here to read all this stuff, here's **the important part:** `It has extremely fast inference time`!

## Creating a free account on Cerebras.AI
> **<u>Note:</u>**
> 
> You can skip this step if you are already signed in.

First, head to [Cerebras.AI Sign In Page](https://cloud.cerebras.ai/). Once there, you can sign in using Google or GitHub, but if you don't want to, you can create an account with your email directly. If it's your first time there, it will ask you for `Your name` and `What best describes your case`. This data will not be shared publicly, so don't worry.

## Getting your API key

### First time login
On signing up for the first time, it will show you a dialog box titled `🚀 Make your first API call!`. In this box, you will see your API key, to copy it, just click the `⧉` button. When you are done, you can click the `×` button on the top right or the blue `Continue` button on the  bottom right.
> **<u>Important Notes:</u>**
> 
> **Save this key** somewhere so you can find it easily.
> 
> Also, **don't share it with anyone**, think of it like a _password_. Of course, you can create another key if the default one got leaked, but it's safer this way.

### Logging in again
If this is not your first time to login to your **Cerebras.AI** account, you can click the `≡` button on the top right and select `API Keys`. You can then see a list of your API keys, there's only one by default. To copy your API key again, just click the `⧉` button next to it in the list.

## Selecting a model
To list the free models that you can click the `≡` button then select `Limits`. You will see a table with all the models you can use for free. At the time of writing this tutorial, the two best models are `llama-3.3-70b` and `qwen-3-32b`, because they have a `65536` context window. If this changes over time, make sure to select a model with a high context window as this is the whole purpose of using a proxy. After determining which models you want to use, copy its name and context window size as we will need them in the next step.
> **<u>Note:</u>**
> 
> The Limits that **Cerebras.AI** put are generously high, but if you *do* exceed them, you can either wait for the next day or create another account and redo the tutorial (But **I don't recommend it**, if they catch you, they will delete your accounts).

## Using Cerebras.AI endpoint in JanitorAI
Before we start, make sure you have the following:
+ Your Cerebras.AI API key
+ The ID of the model (its name, eg. `llama-3.3-70b`)
+ The context window size of the model (eg. `65536`)
+ A new Jailbreak prompt (this is optional, you can use JanitorAI default Jailbreak prompt)

To start, head to [JanitorAI Login Page](https://janitorai.com/login) (or [Sign Up](https://janitorai.com/register)) and login to your account, then, select a bot that supports proxies ([How to know if a bot supports proxies?](#how-to-know-if-a-bot-supports-proxies)). Then, click `Chat with [BOT]` or `Continue latest chat`.

After that, once you're in the chat page, click the `≡` button on the top right and select `API settings`. You will see lots of stuff, I know, I know, just don't let it freak you out, it's really simple. Here's what you need to do:
+ Under the label `Model` choose `Custom` then enter the ID of the model in the input.
+ Under the label `Other API/proxy URL` enter `https://api.cerebras.ai/v1/chat/completions`
+ Ignore the `Check API key/model` button
+ Under the label `API Key` enter your Cerebras.AI API key
+ Optionally change the Jailbreak prompt if you have a different one (You can also select one of the predefined prompts provided by JanitorAI for different purposes)
+ Click the `Save` button

Now, you are almost done, just need to change a few more parameters to make it use the new context window. Click the `≡` button again, but this time select `Generation Settings`. After this, do the following:
+ Ignore the `Temperature` and don't change it, it can mess things up. (if you accidentally changed it, set it to `0.9`)
+ Set the `Max tokens` to `0`
+ Set the `Context Size` to the context window size of the model you chose (eg. 65536) and make sure you use the number input box instead of the slider because the number must be accurate.

And Congratulations!! 🎉🎉🎉 you now have a much better model that can actually remember names and events and not mix things up!


# Troubleshooting

## How to know if a bot supports proxies?
To know if a bot supports proxies, click on it to view its page, then scroll down.
If there is `Proxy allowed` **under the bot's tags**, then that's what we want, but in some bots, won't see it under the tags which means that this bot doesn't allow proxies.
Another way to guarantee a bot has proxies allowed is that its definition **isn't hidden**, so if you see a bot with its definition shown that means it allows proxies. About **90%** of all bots on JanitorAI are proxy-compatible.
I personally keep all my bots proxy-compatible for the best experience (I make bots that are huge, so it needs a good LLM to run on).

## Why am I getting errors?
There are several reasons why you may get an error and that depends on the type of the error.
