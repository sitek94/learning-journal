## Habit tracking app

Most of the day I spent on testing habits related components. I started from the smallest ones and once they were 100% covered I was moving on.
I learned some new stuff about mocking as well.

I still have to find out how to test custom hooks, for example, I have `useHabits` hook that fetches data from the database. I'd like to test 
if everything is okay there. I've seen some interesting article from K. C. Dodds so I'll probably go through it tomorrow and try to implement the ideas 
in my code.

By the end of the day I started adding sorting option to the dashboard list. Well now that I think of it, it rather should be called Dashboard Table because it 
actually has table structure. I might change it in the future. Anyway, back to sorting. When new habit is created it gets a position equal to habits length. 
Habits will be sorted initially by their position so that the highest position number goes first. This way the newly created habit will be first in the list.

<hr>
Total: 8.5hrs
