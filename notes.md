- Server with connections open to Twitter & PokeAPI
- When receives something from Twitter, checks to see if it should do anything
  (e.g. if 1st word is verb 'Play' or 'Use' or something)
- Uses info from database to check whether it needs to send a request to
  PokeAPI
- Simulates another turn in the battle
- Updates database & tweets back with new battle status

- Language = Ruby
- Database = PostgreSQL
- Server not a web server, but can implement web interface for seeing match
  data later

- Simple AI
- Then play against friends
- Easy 'wrapper' bots (e.g. tm_Pikachu)

- Every day, clean inactive (nothing in a week) matches
