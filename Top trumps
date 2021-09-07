import requests
import random
from random import randint

'''Drawing Card from the deck'''
def make_deck():
    deck = []
    for i in range(1,7):
            number = randint(1, 151)
            deck.append(number)
    player1 = []
    player2 = []
    while len(player1) < 3 : #each player has 3 cards
            card = random.choice(deck)
            deck.remove(card) #remove card from deck so it can"t be picked again
            player1.append(card)
            card = random.choice(deck)
            deck.remove(card) #remove card from deck so it can"t be picked again
            player2.append(card)
    # print(deck) #deck is empty because it has been assigned to player 1 and 2
    print(f'Player 1: {player1}')
    print(f'Player 2: {player2}')
make_deck()


def generate_pokemon():
    pokemon_id = input('Player enter stats: ') # this is a string
    pokemon_list = pokemon_id.split(",")  # this function converts the string to list
    pokemon_n = []
    for id in pokemon_list:
        url = f'https://pokeapi.co/api/v2/pokemon/{id}/'
        pokemon = requests.get(url).json()
        pokemon_name = pokemon.get('name')
        pokemon_stats = pokemon.get('stats')
        print(f'stats for pokemon: {pokemon_name}')
        for stat in pokemon_stats:
            stats = {}
            stat_name = stat.get('stat', {}).get('name')
            stat_level = stat.get('base_stat')
            print(f'{stat_name.title()} : {stat_level}')
    return pokemon_n
    
generate_pokemon() # print stats card_1 for both players

'''Pitting cards against each other'''
# choosing which stats to play -- random choice
# choosing stat to use for battle
rand_num = random.randrange(1,6)
print(rand_num)
if rand_num == 1:
        print('Chosen stat: HP')
elif rand_num == 2:
        print("Chosen stat: Attack")
elif rand_num == 3:
        print("Chosen stat: Defense")
elif rand_num == 4:
        print("Chosen stat: Speed")
elif rand_num == 5:
        print("Chosen stat: Special Attack")
elif rand_num == 6:
        print("Chosen stat: Special Defense")
# user input both stats and higher opponent wins
player1 = input("Player 1 enter stat: ")
player2 = input("Player 2 enter stat: ")
# max number wins
if player1 > player2:
    print("Player 1 wins")
else:
    print("Player 2 wins")
