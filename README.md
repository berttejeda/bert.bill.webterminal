# Overview

This is the Webterminal agent to be used with [bert.bill](https://github.com/berttejeda/bert.bill).

This agent allows the app's [xtermjs]((https://github.com/xtermjs/xterm.js/)) Webterminal React component to connect 
to a local bash process on your computer.

You can get this Webterminal agent running either by:

- Install bertdotbill with `pip install bertdotbill` and running `bill -aio`, OR<br />
  Cloning the [bert.bill](https://github.com/berttejeda/bert.bill) project, installing all requirements, and 
  running `python bertdotbill/app.py -aio`<br />
  Doing so will launch a local websocket that forwards keystrokes to a bash process on your system
- Running the pre-built docker image: `docker run -it --name webterminal --rm -p 10001:10001 berttejeda/bill-webterminal`
- Running `docker-compose up -d` from this project

Either of the commands above will start the websocket and bash process on localhost:10001, 
but you can change the port if you like.

Feel free to adjust to your needs.

# Architecture

- Utilizes [spyder-terminal](https://github.com/spyder-ide/spyder-terminal) component

# Features

- You can practice the lesson material with your own OS/system
- Simply **click** on a command, and it will be executed in the underlying shell via web terminal!
- Default shell is bash (for now)