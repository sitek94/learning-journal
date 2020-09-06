## Heat Map

I've finished and posted on the forum 3rd data visualization project - Heat Map.
I've had some problems when displaying the tooltip next to screen edges.
I fixed it by 
  * setting the tooltip `width` instead of `max-width`
  * using `scrollLeft` and `offsetLeft` from the container element
```
  const { scrollLeft, offsetLeft } =  document.body;
  const { pageX, pageY } = d3.event;
  const yOffset = -120;
  const xOffset = scrollLeft + offsetLeft;
   
  tooltip
    .style("left", pageX + xOffset + "px")		
    .style("top", pageY + yOffset + "px");
```

## Functional Programming
For two days I've been going through the article about functional programming and I have to put 
it away now as some concepts are too hard for me to understand at the moment. I understand the core principles 
of functional programming and I'll dive deeper once I have more experience.

I went through the following [article](https://www.freecodecamp.org/news/the-principles-of-functional-programming/)
to the section about Composition and Currying and stopped there.
<hr>
Total: 2.5hrs
