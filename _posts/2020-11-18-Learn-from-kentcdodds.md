## Habit tracking app

A lot of refactoring today. I saw the bookshelf app by Kent C. Dodds and I loved the solutions that he implemented there.
Especially splitting the app to authorized and unathorized. It makes things so simple and it's exactly what I was looking for.

Everything that I've done today was more or less inspired by Kent's code. Amazing stuff. Honestly I can't wait to be able to afford
his [Epic React Course](https://epicreact.dev/)... One day though! 

* split `app` to `authorized-app` and `unauthorized-app`
* create app providers 
* create auth context that exposes `user` object and `login`, `logout`, `register` methods
* create `useAsync` hook
* start adding reusable, small components to `components/lib`
* create reusable `form` component
* update `react-router` to `6.0.0`

<hr>
Total: 9hrs

