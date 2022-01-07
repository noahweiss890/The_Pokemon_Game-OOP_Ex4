# OOP_Ex4

The Pokemon Game is our final project in the Object Oriented Programing course, concentrating the algorithms from previous assignments. 

The game is run by the server, while the client (us) constantly send and receive information and updates on the game through passing strings back and forth. 
The game consists of agents and pokemons which are both located on a map. The map is a directed weighted graph consisting of nodes and edges, where the edge weights are the time in seconds it takes to cross from the source node to the destination node. Pokemons, which are weighted by the amount of points they are worth, are located throughout the graph. The agents' collective goal is to collect the most points as possible by capturing pokemons within the time constaint and without surpassing 10 moves (calls to the server) per second on average. A pokeman can only be caught if the agent is sitting on the source node of the edge the pokemon is located on. Each time a pokeman is caught, a new one appears somewhere on the map. There are 16 cases one can play where the size of the graph and number of agents and pokeman vary. 


Our code follows an MVC (Model View Controller) design pattern. Meaning the data, presentation and control information are all seperated into different objects. The graphAlgo class is the model, holding all the algorithms of the program. The GUI is the view, and the main is the control. 


The GUI presents the map, the amount of collective points accumulating throughout the game, a countdown of the time left of the game and the number of moves/calls to the server. 

We used the idea for allocating pokeman to agents and commanding moves from algorithms we wrote in assignments 0 and 1, and used Center, TSP and Shortest Path (Dijkstra) from assignments 2 and 3, changing the aglogrithms slightly to fit the program. 


More information on the different classes we built, alogrithms we used and functions we created is available in the Wiki section of this project. 

How to run: Download the code and run the server with the following command in the terminal of the downloaded folder:

./serverName x 

x will be a number between 0-15 representing which case the user would like to play. 


Then run the following command:

python3 main.py
