# DS5100_Project_CM9QJ

Metadata
- Course Name: DS5100
- Name: Chloe Merriweather
- Net Id: cm9qj
- GitHub Repo: https://github.com/cmerriwe/DS5100_Project_CM9QJ

Synopsis:
- Die: create and roll a dice with weighted faces
- Game: Play a game with mulitple dice and record results
- Analyzer: analyze results of game


from montecarlo import Die, Game, Analyzer

# Create a die
die = Die([1, 2, 3, 4, 5, 6])
die.change_weight(6, 5.0)


# Create and play a game with three dice
game = Game([die, die, die])
game.play(10)
results = game.show('wide')

# Analyze the game results
analyzer = Analyzer(game)
jackpot_count = analyzer.jackpot()
combo_counts = analyzer.combo()
face_counts = analyzer.face_counts_per_roll()

#API Documentation
Die Class
- __init__(faces)
- change_weight(face, weight)
- roll(num_rolls=1)
- show()

Game Class
- __init__(dice)
- play(num_rolls)
- show(form='wide')
- show_die(die_index=0)

Analyzer Class
- __init__(game)
- jackpot()
- combo()
- face_counts_per_roll()

