# pinlarge: a Pinterest feed proxy [![wercker status](https://app.wercker.com/status/936de8db69098d99f2fa909e6c5c38a2/s/master "wercker status")](https://app.wercker.com/project/bykey/936de8db69098d99f2fa909e6c5c38a2)

A simple Heroku application that acts as a proxy to Pinterest feeds. It parses
each item in the feed and updates the embedded image by changing the thumbinail
to the original size image.

This is useful together with [IFTTT][1] or other automation tools when
generating content (e.g.  tweets) based on a Pinterest feed. You can auto-post
the original size images from Pinterest as Twitter images.

## How to deploy?

Click the button below to deploy this application to Heroku. Heroku will host
it for you for free, as long as you don't use it more than 18 hours a day (this
is a soft limit). If you want to use it in 24/7, it'll cost you $7/month.

Recently I was getting _a lot_ of traffic, so I'd kindly ask everyone to deploy
this app for themselves. I will shut down my app soon.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## How to use?

The API is simple (replace _pinlarge_ with your Heroku app name):

* Use `https://pinlarge.herokuapp.com/sapnwnewbie` to get the feed for user
  `sapnwnewbie`. This will use `https://www.pinterest.com/sapnwnewbie/feed.rss`
  as the source.
* Use `https://pinlarge.herokuapp.com/sapnwnewbie/for-the-home` to get the feed
  for the specific pin board. This will use
  `https://www.pinterest.com/sapnwnewbie/for-the-home.rss` as the source.
* The trailing `.rss` is optional. `https://pinlarge.herokuapp.com/user.rss` is
  the same as `https://pinlarge.herokuapp.com/user`.

[1]: https://ifttt.com
