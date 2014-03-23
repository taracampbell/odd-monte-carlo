Odd: Monte Carlo AI
===============

AI for the game [Odd](http://nickbentleygames.wordpress.com/2010/02/11/one-of-my-better-games-odd/), using the Monte Carlo method. See the wiki for an explanation of the game and the AI.

### Compiling

`javac boardgame/*.java odd/*.java`

### Launching the server

Ensure that the directory containing the _boardgame_ and _odd_ directories is your working directory

Use the following command to launch the server:

`java boardgame.Server [-p port] [-ng] [-q] [-t n] [-b class]`
* '-p port' sets the port to listen on. (default=8123)
* '-ng' indicates not to show a GUI.
* '-q' indicates not to dump log to console.
* '-t n' sets the timeout. (default=5000)
* '-b class' determines the game to run. (default=odd.OddBoard)
* '-k' indicates to start a new server once a game is running  

To launch a GUI with the default Odd parameters: `java boardgame.Server -p 8123 -t 5000 -b odd.OddBoard`

### Launching the client

The server waits for two clients to connect. To launch a client:

`java boardgame.Client [PlayerClass [serverName [serverPort]]]`

To launch the random player: `java boardgame.Client odd.OddRandomPlayer localhost 8123`

To launch the Monte Carlo player: `java boardgame.Client odd.FlatMonteCarloPlayer localhost 8123`
