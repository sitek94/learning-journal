## Fixing calculator

I've been fixing calculator for some time. There were some issues with square root,
dividing by zero. 

Also, I added key binding, which was easier than I thought but then I've been struggling for 
some time with `enter`. It seems that by default `enter` was remembering last action/event.
So when I clicked on `clear` and then used numpad, every time I hit `enter` instead triggering
`equals` it triggered last action - in this case clear.

Fixed it by adding `event.preventDefaults();` in the event handler.

## Portfolio

Finally I've got a file structure that I like and feel comfortable with. Step by step I'm going forward.
Header is almost finished, there might be some small things to fix / adjust but I like it already.

Going forward to About section.

## Morning learning
* Why semantic html is important?
<hr>
Total: 8hrs
