## D3 Heat map

It's been a really long day with d3 heat map. I couldn't find some tutorials on how to create 
a heat map so I've experimenting, looking at other examples, studying the docs, etc.

But finally it looks quite ok, I've started to implement the tooltip and should finish it tomorrow.
Also, I noticed that in the example from fcc they use `d3.tip()`

```
var tip = d3.tip()
        .attr("class", "d3-tip")
        .attr("id", "tooltip")
        .html(function(d){
          return d;
        })
        .direction("n")
        .offset([-10,0]);
```

I'll have to check it out because it looks like it would be better than a simple `div` that I've been using so far.

### Scale Threshold
I've been struggling a lot with setting up this scale today. While I still don't understand exactly how this works, this post
helped me to figure some things out:
https://stackoverflow.com/questions/48161257/understanding-invertextent-in-a-threshold-scale

## Morning learning
Continue to read the post on fcc about Functional Programming
  * Data, Calculations, and Actions
  * What is mapping
  * Immutability
  * Exercises set 1
  
<hr>
Total: 7.5hrs
  

