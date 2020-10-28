## Habit tracker app refactor

I refactored the app so that it is now in one repository.

## How to redirect back from Express to React?

I've been looking for answer to this for so many hours that I've lost count. After authenticating with google I basically wanted to
get back to my react app and I just couldn't do it in a simple way. 

```javascript
router.get(
  '/google/callback',
  passport.authenticate('google', { failureRedirect: '/' }),
  (req, res) => {
  
    // I wanted this to redirect me back to React (localhost:3000), and instead it was
    // redirecting me to the server (localhost:5000)
    res.redirect('/dashboard');
  }
);
```

The solution to this was to remove this line of code in `setupProxy.js`
```javascript
module.exports = function (app) {
  app.use(
    '/auth',
    createProxyMiddleware({
      target: 'http://localhost:5000/',
      
      // Remove line below
      changeOrigin: true,
      // Remove line above
     
    })
  );
};
```

To be honest, I have absolutely no idea if this is the proper way to do all the authentication process, because
I've never done it before. So I'm really curious what I'll have to say about this when I rediscover this post in a year or so :D

It works at the moment, we'll see later how it goes.

<hr>
Total: 9hrs
