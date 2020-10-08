## Morning learning - Eloquent JavaScript

I went through exercises of chapter 7 and I finally understood the logic behind this project. 
I started reading chapter 8, which is about debugging. 

All my notes on codepen.

## Pocket globe app

First I've been refactoring the code, reorganizing folder structure and cleaning the components.
After I finished I've found some nasty memory leak bugs. I'm trying to figure it out since 4 hours with no results so far.

At least I was able to reproduce the error in isolated environment.

https://codesandbox.io/s/polished-moon-91fg2?file=/src/App.js

I think it has something to do with conditionally rendering a component. The error message points at line where I'm conditionally rendering Details component.

<hr>
Total: 7hrs

