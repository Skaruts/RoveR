# RoveR

### <i> Your battery is low and it’s getting dark </i>

RoveR is a roguelike about a planetary rover created using [R](https://en.wikipedia.org/wiki/R_(programming_language)) and the package [Shiny](https://shiny.rstudio.com/). 

This is my entry in the [/r/roguelikedev](https://www.reddit.com/r/roguelikedev/) 2019 summer tutorial. I am not a developer, and this is entirely a hobby project. I’m not aware of any games made with R (perhaps for a good reason)! Let's see if it's possible. You can play my most recent deployment [here](https://foxfields.shinyapps.io/rover/). Press any key to start. Be patient, the demo requires up to 10 seconds to load when hosted. It's almost instant locally, I swear!

Controls: Any key to start; WASD keys to move

<i> Not working?</i> The RoveR app is being hosted for free. If the application is active for more than 25 hours, it will be unavaliable to users. 

### Mission Progress: 

#### Week 3: "Lunokhod 2"

This week's mission objectives included [planet generation](preview/lunokohd_2_map.png) and turn handling. I've decided to forego the field of view tutorial - I can implement later, if necessary - but my decision to have a small field of view might make any field of view mechanic redudant. Planet generation uses a modified random cluster method modified from [Saura and Martínez-Millán, 2000](https://link.springer.com/article/10.1023/A:1008107902848). This will be expanded later with environmental variables like thermal gradients across elevation and lattitude. Performance remains an issue when hosted online but is great locally. Profiling suggests the peformance bottleneck is mapping R objects to javascript (I think) with Plotly.js and not my R script per se. Because this only seems to be an issue with the hosted demo, I will save optimization until the end of the tutoial.

![Lunokhod_2](/preview/lunokhod_2.gif)

#### Week 2: "Apollo Lunar Rover"

This week's mission objectives included tile collision, non-player entities and a temporary 'dungeon' for exploring. Level generation is simple, with a central hall and rooms. Performance is great when run locally, but relatively slow when the shiny app is hosted.

![Apollo Lunear Rover](/preview/apollo_lunar_rover.gif)

#### Week 1: "Lunokhod 1"

Huzzah! By using R along with the package Shiny, I was able to create the basic environment and move the player rover "@" around the screen. 

![Lunokhod 1](/preview/lunokhod_1.gif)
