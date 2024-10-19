# Programming Assignment 1 - CIS427 - Pokemon Card Trading Server/Client
### Tools Needed:
+ Python
+ Terminal
+ Visual Studio Code

### Set-Up Instructions:
1. Ensure that the most recent version of Python is downloaded and installed on your computer

### Running the Program
1. Open Terminal and run these commands:

    a. cd into the folder containing the project code

    b. start server: 'python3 server.py' If no 

    c. start client: 'python3 client.py localhost 9037'

    d. All set!

### Command Implementations
1. BUY
     > Format: BUY <cardName> <cardType> <rarity> <price> <count> <ownerID>\n
     > Function Definition: Upon launch of the server, a database with two tables (Users & Cards) will be created.\n\n

     > Users table will have a single user to start and balance will default to $100.\n
     
     > 200 OK if BUY is within parameters and will add the purchased card to Cards table; 403 if message format is incorrect; 404 if not enough balance to purchase.

2. SELL
     > Format: SELL <count> <price> <ownerID>\n
     > Function Definition: Allows user to sell a card listed in their inventory\n\n
     
     > 200 OK if SELL is within parameters and will remove the quantity of sold card(s) from Cards table; 403 if message format is incorrect; 404 if card is not available to be sold.

3. LIST
     > Format: LIST <ownerID>\n
     > Function Definition: Lists all cards that are currently contained in Users inventory.

4. BALANCE
     > Format: BALANCE <ownerID>\n
     > Function Definition: Provides the Users monetary balance.

5. QUIT: Quits the program by closing the client-side.

6. SHUTDOWN: Quits the program entirely by shutting down the server and closing the client-side.

### Known Project Deficiencies
1. Project does not utilize the UMD name servers due to time-constraint. The code works locally. This functionality will be added on for the second portion of the project.
2. User Switching is not currently programmed.
