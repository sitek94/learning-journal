## Interactive Globe

I made a great progress today. 

First I organized all the code that I was left with yesterday. To be more specific I extracted the logic 
that is responsible for rendering the interactive globe. It's now a separate component that I can easily use 
in any other project.

I've been experimenting a little with different topojson datasets. At first I wanted to have an option to choose from
3 different precisions but in the end I decided to go without 10m because it was definitely too large. 

After that I started to implement fetching data after clicking on each country. First I wanted to use wikipedia api but they 
didn't really had what I wanted or I couldn't find it. Nevertheless I've found really nice REST Countries api and this is what I used
in the project.

Fetching country details is now implemented and extracted to a separated component so it's clean and easy to use.
<hr>
Total: 7.5hrs
