# Cerebras.AI API Tutorial for JanitorAI
This Guide will walk you through:
+ [Creating a free account on Cerebras.AI](#creating-a-free-account-on-cerebrasai)
+ [Getting your API key](#getting-your-api-key)
+ [Selecting a model](#selecting-a-model)
+ [Using Cerebras.AI endpoint in JanitorAI](#using-cerebrasai-endpoint-in-janitorai)

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
To list the free models that you can click the `≡` button then select `Limits`. You will see a table with all the models you can use for free. At the time of writing this tutorial, the two best models are `llama-3.3-70b` and `qwen-3-32b`, because they have a 65K context window. If this changes over time, make sure to select a model with a high context window as this is the whole purpose of using a proxy.
> **<u>Note:</u>**
> 
> The Limits that **Cerebras.AI** put are generously high, but if you *do* exceed them, you can either wait for the next day or create another account and redo the tutorial (But **I don't recommend it**, if they catch you, they will delete your accounts).

