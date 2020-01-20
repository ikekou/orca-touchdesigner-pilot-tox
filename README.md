# orca-touchdesigner-pilot-tox

I wanted to operate TouchDesigner and Pilot from ORCA.  
This is a tox that links ORCA, TouchDesigner and Pilot.  
It receives UDP from Orca and parses it into CHOPs, and proxy to Pilot.

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

How to run --> https://github.com/hundredrabbits/Orca/blob/master/README.md

### Change UDP Port of Orca

Menu > Communication > Choose UPD Port

Input `49169` .

### Run Pilot

Just run fork version Pilot.

How to run --> https://github.com/ikekou/Pilot/blob/master/README.md

### Run TouchDesigner and open example

Open `example/touchdesigner/touchdesigner-example.toe`

### Done

That's all.

![orca](https://github.com/ikekou/orca-touchdesigner-pilot-tox/blob/master/README/orca.gif?raw=true)
![touchdesigner](https://github.com/ikekou/orca-touchdesigner-pilot-tox/blob/master/README/touchdesigner.gif?raw=true)
![pilot](https://github.com/ikekou/orca-touchdesigner-pilot-tox/blob/master/README/pilot.gif?raw=true)

## Why do I need to change the port?

I wanted to send notes from Orca to Pilot and TouchDesigner at the same time. However, one operator did not know how to send to both.

So I considered sending from Orca to TouchDesigner and then from TouchDesigner to Pilot.

### Flow

```
[ Orca ] == (UDP) ==> (port:49169) [ TouchDesigner ] == (UDP) ==> (port:49161) [ Pilot ]
```

## I think there is another better way.

I'm sure Orca has an easier way, but I didn't know. Please let me know if you know.

https://twitter.com/ikekou