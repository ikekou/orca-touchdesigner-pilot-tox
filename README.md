# orca-touchdesigner-pilot-tox

A tox that links ORCA, TouchDesigner and Pilot.  
Receives UDP from Orca and parses it into CHOPs. And proxy to Pilot.

## Dependencies

hundredrabbits/Orca: Esoteric Programming Language  
https://github.com/hundredrabbits/Orca

hundredrabbits/Pilot: Orca's best friend.  
https://github.com/hundredrabbits/Pilot

Derivative  
https://derivative.ca/


## Install & Run

### Install ORCA 

Please download it.

https://github.com/hundredrabbits/Orca

### Install Pilot

Needed a little remodeling. So download this fork version.

https://github.com/ikekou/Pilot

### Install TouchDesigner

Please download it.

https://derivative.ca/download

### Run Orca and open example

Run Orca, and open example/orca/orca-example.orca .

### Run Pilot

Just run fork version Pilot.

### Change UDP Port of Orca

Menu > Communication > Choose UPD Port

Input `49169` .

### Done

That's all.

### Run TouchDesigner and open example

Open `example/touchdesigner/touchdesigner-example.toe`

## Why do I need to change the port?

I wanted to send notes from Orca to Pilot and TouchDesigner at the same time. However, one operator did not know how to send to both.

So I considered sending from Orca to TouchDesigner and then from TouchDesigner to Pilot.

### Flow

```
[ Orca ] == (UDP) ==> (port:49169) [ TouchDesigner ] == (UDP) ==> (port:49161) [ Pilot ]
```

## Known issues

In Pilot, the case changes depending on the case. However, this tox treats the same. 

But it may not be too much trouble in visual expression. And it seems that Orca's OSC itself has such a specification.

## I think there is another better way.

I'm sure Orca has an easier way, but I didn't know. Please let me know if you know.

https://twitter.com/ikekou