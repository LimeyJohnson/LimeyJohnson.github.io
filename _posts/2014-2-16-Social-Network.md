---
title: Social Network
layout: post
comments: false
category: socialnetwork
---
[Social Network](http://SocialNetwork.LimeyJohnson.net) is a way to visualize your social network. --INSERT SCREEN SHOT--. Initially it start out as a project to learn some cool new technologies like [Script#](http://scriptsharp.com), [D3.js](http://d3js.org) and the [FB Api](http://developer.facebook.com) but now it has grown to a full blown project. 
<!-- more -->
The magic of the project is how quickly it can create the graph of your friends, with all of the connections, and serve that graph to you. 

That magic comes from the following SQL statement
{% highlight SQL %}
 friendsLimit: SELECT uid1, uid2 from friend WHERE uid1 = USERID ORDER BY uid2 ;
 friendsAll: SELECT uid1, uid2 from friend WHERE uid1 = USERID;
 SELECT uid1, uid2 FROM friend WHERE uid1 IN (SELECT uid2 from #friendsLimit) 
	AND uid2 IN (SELECT uid2 from #friendsAll) AND uid1 < uid2;
{% endhighlight %}

TODO:
Screen Shot
Remove code
Explain the reason for doing the project
What is a network and why is is useful

