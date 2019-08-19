# A Generic Tic-Tac-Toe Game

a node.js client serving a react interface and a python flask server which implements the game api.

To run the web app, the original instructions are largely the same.

```
docker build -t tictactoe-session .
docker run --volume "$(pwd)":/tictactoe-session --interactive --tty --publish 8000:8000 tictactoe-session
```

Note the Dockerfile has instructions to install plenty of node modules, the build process will take a couple minutes.

Once in bash, the run.sh contains the commands to start both servers as well as a redis instance.

```
chmod +x run.sh
./run.sh
```

The Dockerfile is monstrous, the flask server, redis server and node client deserve their own containers (potential for orchestration).

