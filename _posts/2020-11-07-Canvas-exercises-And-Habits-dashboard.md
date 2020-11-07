## Morning learning 

I've started to going through the exercises from chapter 17. At first I thought that exercises that involved using `Math.cos` and `Math.sin` will be
really hard but in the end they weren't that bad at all.

## Habit tracking app

* [HabitsPage]: When user has no habits display Empty state page with a link to Add habit page
* [HabitsPage]: Add frequency in habit list. At first I created a custom svg component with circle and text but
  in the end I used `Chip` from Material-ui
* [Router]: Added habit related routes - so that all the routing is handled here
* [Dashboard] in progress :hourglass: a lot of experimenting
* [Database]: added `days` collection.
  
  Each day should look like this
  ```javascript
  let day = {
    // In firebase it is possible to use other doc ref, so I might use that instead of ID
    habitId: string / ref,
    state: "completed / skipped / failed",
    date: timestamp
  }
  ```
<hr>
Total: 7hrs
