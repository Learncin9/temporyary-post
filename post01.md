# MPA vs SPA
## Requirement to read this.
You should know these following things to read and understand this post.

```
1. What is HTML
2. Basic Javascript
```

# What is MPA
MPA is abbreviation of `Multi Page Application`.
In here, you should know is what is `page`.

`page`is just a HTML file.
`Multi Page Application` means "There is many html files in your application."

If you are php developer, whole php application can be a good example.
If you move to another page, your browser wil request another html and render that html.
And you will see a blank page for a very short while.

```
       Request a page
[You] ---------------> [Server]
      <---------------
       Give a HTML
```

But, why we should use this way?
In web application, you most provide recent data.
If a user puts money in the bank, bank server should show a user increased money.

Originally, you can`t talk with server, after HTML/CSS/JS were sent to browser.
So, server should make a HTML with recent data and send it to user.
Not using this way, there is no way to show recent data to user.

They usually fetches data from Databse and make an appropriate HTML for user with Template Engine.
(If you want to use this way, you can use spring(java) or php)

**MPA**
```
Pros
1) You can always send recent data to user.

Cons
1) Users wil be suffered by 'blink time'.
```

# What is SPA
All users don't want to wait.
This is true and will be true forever.

Of course, users don't like 'blink time'.

When developers were making website with 'blink time', A interesting specification was submited.
That specification was `XMLHttpRequest` and it let JS talk with server after it was sent to broswer.

Now, some developer think some **wired** idea.
Basically, If you load html page, you will face 'blink time'. And some tricks, you can trick users that they loaded html without any loading.

This is the trick.
