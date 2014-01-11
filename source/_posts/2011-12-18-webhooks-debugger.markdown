---
layout: post
title: "WebHooks Debugger"
date: 2011-12-18 00:00:00 -0600
comments: true
categories: 
---

[PostBin]: http://www.postbin.org/
[WebHooks]: http://www.webhooks.org/

I’ve been reading a lot about [WebHooks] lately and I’m very intrigued.  It’s a simple idea, basically just an event call over http.  It’s a push model.  You register a url with another application, and when something happens in that application, it does an HTTP post with the information.  So, the idea is simple to grasp but it can do some powerful things.  For example, this WordPress blog has a way to register url’s to call when a new post is added.  I can create a page for it to post to, and then have an e-mail sent to me, post notifications to my favorite social network, or whatever you can dream up.  We aren’t limited to notification either, we can also create composite calls that act on the data sent to it, same idea as XML-RPC.

I came across [PostBin] which is a WebHook debugger.  You can create a bin and have you application do an HTTP POST to it, and it will store the headers and body data for you.  It has it’s limitations, like being throttled by Google Apps for both data size and bandwidth, it only worked for me about half the time.  I decided to create a [PostBin] type application for my own purposes.  The functionality is the same as [PostBin] but instead of having to manually create the bins, mine are automatically created by posting to the url.  Since it’s not a full fledge application, it doesn’t have the security or data limitations.  I’ll put that in for later versions if it gets overused and abused.

Sample application is available at [http://apps.iamggreen.com/postbin](http://apps.iamggreen.com/postbin)

Source code is available at [https://github.com/iamggreen/PostBinDebugger](https://github.com/iamggreen/PostBinDebugger)
