## Habit tracking app

I spent all they refactoring app's folder structure, organizing routing and cleaning up the code. I think it should be good to go now.

* updated checkmarks so that they use the data that is already fetched and exposed by `checkmarks-provider`. 
Before each checkmark was fetching its own data.
* completely changed the folder structure - moved away from `features/...` pattern and instead I split 
the code into pages as I thought it's more natural for this project.
* created `layout` and `content` wrappers
* `public-wrapper` - responsible for public routes and appbar
* `dashboard-wrapper` - responsible for authorized routing, appbar and drawer

<hr>
Total: 8.5hrs
