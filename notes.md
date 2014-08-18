Process
-------

✓ Server with connection open to Twitter (streaming user?)
- When receives something from Twitter, checks to see if it should do anything
  (e.g. if 1st word is verb 'Play' or 'Use' or something)
- Uses info from database to check whether it needs to send a request to
  PokeAPI
- Simulates another turn in the battle
- Updates database & tweets back with new battle status

- Language = Ruby
- Database = PostgreSQL
- Server not a web server, but can implement web interface for viewing match
  data later

- Simple AI
- Then play against friends
- Easy 'wrapper' bots (e.g. tm_Pikachu)

- Every day, clean inactive (nothing in a week) matches

Twitter parsing
---------------

- Mention can come anywhere in the sentence.
- Verbs:
    - help
    - attack/use/move <move number/name> [player]
        - optional preposition?
        - if [ -z player ], check if user only has 1 match active
            - if y, use on them
            - if n, tell them
    - stats [player]
        - if [ -z player ], stats of user
    - later: in-match checks (re-check moves, stats etc.)
    - later: spectate a match (send another tweet, or mention? mentions may
      make tweet too long)
