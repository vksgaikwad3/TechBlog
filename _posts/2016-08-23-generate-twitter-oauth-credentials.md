---
title: Generate Twitter OAuth Credentails
author: Vikas Gaikwad
date: 2016-08-23 11:33:00 +0800
categories: [Blogging, OAuth]
tags: [twitter,oauth]
math: true
#image: /assets/img/sample/devices-mockup.png
comments: true
---

<img class="  wp-image-483 aligncenter" src="https://vksgaikwad3.files.wordpress.com/2016/08/twitterblogimg.png" alt="twitterblogimg" width="621" height="339" />

Hello friends,

Its been a long past now I had worked on Twitter API with python for creating an awesome things like controlling things(devices) from physical world using Digital World.

Today we will understand How to access python <strong>Twitter API</strong> and do awesome things with <strong>python,Twitter & Internet.</strong> Well I usually write a <strong>software</strong> for   controlling <strong>Hardware.</strong>

Here I had an interesting  application in mind around <strong>IoT </strong>ohhh yeah !!! but before starting with actual idea we need the <strong>Twitter OAuth</strong> Credentials to access the python Twitter API

so lets get started........
<h3 class="entry-title">How to Generate API Key, Consumer Token, Access Key for Twitter OAuth</h3>
After Twitter has closed the access to  version 1.0 of API, we all are pushed to change the Latest Tweets widget and Twitter Follower counter widget settings in order to make it work with <a href="https://dev.twitter.com/overview/api">Twitter API version 1.1.</a>

To make things straight, you have to create a Twitter application to generate Twitter API Keys, Access Token and secret keys and so on.

<img class="alignnone size-full wp-image-492" src="https://vksgaikwad3.files.wordpress.com/2016/08/create-twitter-api-key.jpg" alt="Create-Twitter-API-Key" width="640" height="402" />

To use Twitter counter widget and other Twitter related widgets, you need OAuth access keys. To get Twitter Access keys, you need to create Twitter Application which is mandatory to access Twitter.
<ul>
	<li>Go to <a title="https://dev.twitter.com/apps/new" href="https://dev.twitter.com/apps/new">https://dev.twitter.com/apps/new</a> and log in, if necessary.</li>
	<li>Enter your Application Name, Description and your website address. You can leave the callback URL empty.</li>
	<li>Accept the TOS, and solve the CAPTCHA.</li>
	<li>Submit the form by clicking the <strong>Create your Twitter Application.</strong></li>
	<li>Copy the consumer key (API key) and consumer secret from the screen into your application.</li>
</ul>
<img class=" size-full wp-image-501 alignleft" src="https://vksgaikwad3.files.wordpress.com/2016/08/twitter-oauth-settings.jpg" alt="Twitter-OAuth-Settings" width="640" height="355" />

After creating your Twitter Application, you have to give the access to your Twitter Account to use this Application. To do this, click the <strong>Create my Access Token.</strong>
<h3>Get the Consumer Key, Consumer Secret, Acess token, Access Token Secret</h3>
<img class="alignnone size-full wp-image-507" src="https://vksgaikwad3.files.wordpress.com/2016/08/twitter-oauth-access-tokens.jpg" alt="Twitter-OAuth-Access-tokens" width="640" height="409" />

In order to access the Twitter, that is to get recent tweets and twitter followers count and more, you need the four keys such as <strong>Consumer Key, Consumer Secret, Acess token, Access Token Secret.</strong>

At this stage you will receive all the above credentials of your <strong>Twitter App.</strong>

<strong>Note: Please don't share your twitter apps credentials with anyone.</strong>

Yes we are now done with our 1st step, in our next session we are going to use these these credentials in our python programs and going to access Twitter API.

Cheerrrrr..........!!!

