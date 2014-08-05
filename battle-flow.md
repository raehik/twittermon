while this.active == 1:
    promptForInput(this.currentTurn)
    if otherPokemon.HP == 0:
        database.set(this.active, 0)
        this.active = 0
