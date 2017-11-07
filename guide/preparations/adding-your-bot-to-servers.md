## Adding your bot to your own (and other) servers

If you've been diligently following the previous pages of the guide, you should have a bot application set up. However, it's not in any servers yet. So how does that work?

Before you're actually able to see your bot in your own (or other) servers, it needs to be added using a special invite link that can be created using your bot application's client ID.

### Bot invite links

The basic version of one such link looks like this:

```
https://discordapp.com/oauth2/authorize?client_id=123456789012345678&scope=bot
```

The structure of the url is quite simple:

* The first part is just Discord's standard structure for authorizing an OAuth2 application (such as your bot application) for entry to a Discord server.
* The second part that says `client_id=...` is to specify _which_ application you want to authorize. You'll need to replace this part with your client's ID in order to create a valid invite link. 
* Lastly, the third part which says `scope=bot` specifies that you want to add this application as a Discord bot.

<p class="tip">A `permissions` parameter also exists to restrict or guarantee the permission your bot will have on the server you add it to. For ease of use, it is recommended to use [this](https://discordapi.com/permissions.html) website.</p>

<p class="warning">If you get an error message saying "Bot requires a code grant", then head over into your application's settings and disable the "Require OAuth2 Code Grant" option. You usually shouldn't enable this checkbox unless you know why you need to.</p>

### Creating and using your own invite link

As mentioned above, you'll need to replace the `client_id` parameter with your client's ID in order to generate your invite link. To find your app's ID, head back to the [My Apps](https://discordapp.com/developers/applications/me) page under the "Applications" section once again and click on your bot application.

Insert your app's ID into the link template and then access it in your browser. You should see something like this (with your bot's username and avatar):

![Bot Authorization field](assets/img/A8l70bj.png)

Choose the server you want to add it to and click "Authorize". Do note that you'll need the "Manage Server" permission on a server in order to be able to add your bot there. This should then present you a nice confirmation message:

![Bot authorized](assets/img/BAUsjyg.png)

Congratulations! You've successfully added your bot to your Discord server. It should show up in your server's member list somewhat like this:

![Bot in server's user list](assets/img/6qTlDW0.png)