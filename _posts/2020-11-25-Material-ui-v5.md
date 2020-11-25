# Habit tracking app

## Material-UI v5

So far I've been using `react-date-range` but there was it was not possible to easily implement custom styles and the project seems 
that is no longer maintained so I started looking for something else.

I really liked date pickers from `material-ui` and I'm already using it anyway so it was very easy choice for me. 
The only thing I had to do is to migrate from v4 to v5. Week picker is now implemented.


## Problems

Also, fixed some issues when toggling checkmarks really fast. Because of cancelling the query a `CancelledError`
is thrown and my `error-boundary` was crashing with it so I made some changes to avoid that. Anyway I read that it is not going to be a problem in v3 of `React-Query`.

## Other

disabled future checkmarks in the dashboard

<hr>
Total: 8.5hrs
 
