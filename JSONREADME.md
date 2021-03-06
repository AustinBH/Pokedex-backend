Our Pokedex API

 * This pokedex api was created to serve data that is used for a javascript project.

Database

  * Setup
    - Our database is setup using postgres so if you want to clone this repo down you will need to ren rails db:setup to start
    - Our seed file requires some work if you want to seed your database with all 807 pokemon.
    - Because we are seeding using the PokeAPI and the Poke API V2 Gem you will need to manually change the while loop in our seeds file.
    - The API supports 100 requests per minute so we recommend seeding 50-75 pokemon at one time.

Using the API

  * Routes
    - All of the routes for our API are available to view pokemon specific information.
    - You can also view information about individual pokemon.
    - We do support 3 different filtering options at this time.
      - Pokemon Type
      - Pokemon Name
      - Pokemon Generation (I, II, III, etc.)

  * This API can currently be accessed here
    - https://pokedex-yeet.herokuapp.com

Live Routes

   * Pokemon
     - Example Route
       - https://pokedex-yeet.herokuapp.com/v1/pokemon
     - Filter formatting
       - You will need to prepend the following to the above example route
         - ?name=insertNameHere
         - ?type=insertTypeHere
         - ?generation=insertGenerationHere
     - The name filter will display pokemon with a name that includes the string that you pass in
       - For example, charm will return both charmander and charmeleon
     - The type filter will display pokemon that have a matching type
       - This does include multi type pokemon so a fire and flying type will be displayed if you search fire or flying
     - The Generation filter will display all pokemon from that generation
     - Information
       - Name
       - Pokedex Number
       - Image
  * Specific Pokemon
    - Example Route
      - https://pokedex-yeet.herokuapp.com/v1/pokemon/1
      - This route will return all of the information for the pokemon bulbasaur
    - Information
      - Here we display all of a pokemon's information
        - Name
        - Pokedex Number
        - Description about the pokemon
        - Their type(s)
        - Height
        - Weight
        - Image
        - Generation

Contributors

  * Both the back and frontends of this project were built by Noah Fairbairn and Austin Harlow
    - https://github.com/NFairbairn
    - https://github.com/AustinBH
  * The data that we used for this project is from the PokeApi and The Pokemon Website.
    - https://pokeapi.co/
    - https://www.pokemon.com/us/
