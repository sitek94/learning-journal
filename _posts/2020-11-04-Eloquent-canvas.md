## Morning learning

I've finished exercises from chapter 16 and started reading chapter 17 about the Canvas!

## Habit tracking

I did some refactoring:
* nested routes responsible for managing habits
* created `useFirebase` hook that exposes the api
* Added habits context, it can be used through `useHabits` hook
* it's possible to update the habit in `edit-habit-page`

- [ ] When reloading the page, and user is inside of a route in `HabitsContexts` the habits are not loaded so it throws an error, because 
it cannot destructure a value. I have to figure sth out how to prevent that.

<hr>
Total: 7.5hrs
