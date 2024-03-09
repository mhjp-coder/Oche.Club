# Oche.Club Darts Design Document

## About the Application

- The software application, Oche.Club, is a comprehensive Dart Management System. It's designed to cater to a wide range of dart players and enthusiasts, from individuals who play casually to organized teams participating in competitive leagues. A player can be an individual or a group of individuals (team) participating in the game. The system is flexible enough to handle various game setups, including single player games, multi-player games, team games, and even complex league tournaments. In a league setup, the system can manage multiple teams playing against each other in different formats, such as round-robin or bracket-style tournaments. This versatility makes the system a one-stop solution for all dart scoring and management needs, regardless of the level of play or complexity of the tournament structure.

- Oche.Club is designed to solve the problem of manual score, statistic, and tournament tracking in dart games, which can be tedious, prone to errors, and disruptive to the flow of the game. By automating these tasks, the application reduces the likelihood of mistakes in score calculation and recording, which can lead to disputes and dissatisfaction among players. It also saves players the effort of keeping track of their scores and statistics, allowing them to focus more on the game itself. Furthermore, the application provides a more streamlined and enjoyable gaming experience by displaying real-time scores and standings, which adds to the excitement and competitive spirit of the game. For tournament play, the application simplifies the management of multiple games and teams, making it easier to organize and run large-scale events. The system can automatically schedule matches, keep track of results, and update tournament standings, reducing the administrative burden on organizers and ensuring a smooth and efficient tournament process.

- Oche.Club will allow users to input their scores for each round, automatically calculate the total score, and display the current standings. This feature is designed to make the scoring process as seamless and intuitive as possible. Users can easily enter their scores using a simple and user-friendly interface, and the application will do the rest. The automatic calculation feature eliminates the need for manual arithmetic, reducing the risk of errors and disputes. The real-time display of current standings adds an element of excitement and competition to the game, as players can see exactly where they stand at any given moment. The application will also display the player order in the case of multiple player teams, ensuring a fair and orderly progression of the game. Additional features like undoing the last score and resetting the game provide flexibility and control to the users, allowing them to easily correct mistakes or start a new game. For future consideration, the application could support different dart game variations, making it adaptable to a wide range of game rules and formats.

- The main concepts involved in the application are the players, rounds, scores, and game rules. Players are the individuals or teams participating in the game. Each player takes turns playing rounds, where they throw their darts and score points based on where the darts land on the dartboard. The application keeps track of these scores for each round and adds them to the players' total scores. The game rules are the set of guidelines that determine how points are scored and how the winner is decided. These rules can vary depending on the specific game variation being played. For example, in a standard game of darts, the objective is to be the first player to reduce a fixed score, commonly 501 or 301, to zero. However, other game variations may have different objectives and scoring methods. The application applies these game rules to calculate the total scores and determine the winner. It also handles special situations defined by the rules, such as 'busts' where a player's score exceeds the remaining total, requiring the player's score to be reset to the previous round's total. By incorporating these concepts into its design, the application provides a comprehensive and authentic dart gaming experience.

## Technical Specification

- What technical details do developers need to know to develop the software or new feature?
- Are there new tables to add to the database? What fields?
- How will the software technically work? Are there particular algorithms or libraries that are important?
- What will be the overall design? Which classes are needed? What design patterns are used to model the concepts and relationships?
- What third-party software is needed to build the software or feature?

**Notes**
You can use UML to draw out the main classes that will be added and how they fit into the rest of the system. When you design your classes and methods, consider design principles such as SOLID. Design principles are the foundation of software design. Going through all of the principles is out of scope for this document, but I have several videos on my YouTube channel where I talk about them, so check those out if you’re not yet comfortable with the principles. On top of the principles are the design patterns, which are standardized solutions to particular software design problems. There are also quite a few videos about those on my channel. This is also a good section to describe specific edge cases that you want the system to handle correctly, for example what should happen in case of a network connection error.

- Developers should have a solid understanding of Python and the Django web framework, as these will be the primary technologies used for backend development. Knowledge of Postgres is also necessary, as it will be used for database management.

- For frontend development, familiarity with HTML is required. Additionally, experience with Tailwind and DaisyUI for styling, and HTMX for handling AJAX requests, is beneficial.

- The backend will be built using Django, which follows the Model-View-Template (MVT) architectural pattern. Django's ORM will be used to interact with the Postgres database.

- The frontend will be built using HTML, enhanced with Tailwind and DaisyUI for responsive and modern design. HTMX will be used to enable AJAX requests, allowing for a dynamic user interface without the need for JavaScript.

- The database will have tables for Players, Teams, Games, and Tournaments. The Players table will have fields like player_id, name, and statistics. The Teams table will have fields like team_id, team_name, and player_ids. The Games table will have fields like game_id, player_ids, team_ids, scores, and game_status. The Tournaments table will have fields like tournament_id, game_ids, team_ids, tournament_status, and winner_id.

- The application will work by taking user inputs for scores, calculating the total scores, and updating the database in real-time. Python's built-in math library will be used for calculations. Django will handle server-side logic and database updates.

- In terms of edge cases, the system should handle situations like a player entering an invalid score, a network connection error during a game, or a user trying to access a game or tournament they're not part of. The system should provide appropriate error messages and recovery options in these cases.

Here are the main classes that will be needed:

- `Player`: This class will represent a player in the game. It will have attributes such as `player_id`, `name`, and `statistics`.

- `Team`: This class will represent a team in the game. It will have attributes such as `team_id`, `team_name`, and `player_ids`.

- `Game`: This class will represent a game. It will have attributes such as `game_id`, `player_ids`, `team_ids`, `scores`, and `game_status`.

- `Tournament`: This class will represent a tournament. It will have attributes such as `tournament_id`, `game_ids`, `team_ids`, `tournament_status`, and `winner_id`.

In terms of design patterns, the application will primarily use the following:

- `Factory Pattern`: This can be used to create objects of `Player`, `Team`, `Game`, and `Tournament` classes based on the user's input.

- `Singleton Pattern`: This can be used for database connection to ensure that only one connection is active throughout the application.

- `Observer Pattern`: This can be used to update the game and tournament standings in real-time whenever a score is updated.

These design patterns will help in structuring the application in a way that is efficient, scalable, and maintainable.
