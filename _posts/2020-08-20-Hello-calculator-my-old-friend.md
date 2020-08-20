## Drum Machine up and running

I've had some troubles with DOM Exception error when running the tests in test suite.
I spent half a day looking for possible solutions. 

Only to in the end find out that it has something to do with Chrome because in Firefox
there is no such error. Moreover, the very same error is in the original example.

So I went one step further and catched that error in a promise so at least I'm not getting
nasty console logs in Google Chrome when running tests.

I just have to deploy the project on gh-pages and we're done.
 
## Calculator

Started from scratch, because I didn't like my old approach. I built very basic layout and started to 
implement logic. I almost finished with 15/16 test, there is just a problem with subtract operator 
but I'll solve it tomorrow.

## Morning learning today
* variable hoisting

Total: 8hrs
