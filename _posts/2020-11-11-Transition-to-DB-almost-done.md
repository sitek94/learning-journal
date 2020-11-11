## Habit Tracking App

I've been working on transition from Firestore to Realtime Database and it's nearly done. I think the only thing that's left are 
`Checkmarks` but these already work too, they just need cleaning up and testing. 

Also, I replaced some hardcoded data, like days of the week and database formats*

\*database formats - in the database I store habit completion state as numbers: `1` - completed, `2` - skipped, etc.
I created an object where I store all theses values, so it's easy to access and change them eventually.

I've been looking for some ways to test the components that are fetching data from database but couldn't find anything that would help me.

<hr>
Total: 8hrs
