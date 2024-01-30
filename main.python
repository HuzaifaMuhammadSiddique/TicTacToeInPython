def game_board(board):
  for i in range(3):
    print("|", board[i*3], "|", board[i*3 + 1], "|", board[i*3 + 2], "|")

def check_winner(board):
  if board[0] == board[4] == board[8]:
    return True,board[0]
  elif board[0] == board[1] == board[2]:
    return True,board[0]
  elif board[3] == board[4] == board[5]:
    return True,board[3]    
  elif board[6] == board[7] == board[8]:
    return True,board[6]   
  elif board[0] == board[3] == board[6]:
    return True,board[0]
  elif board[1] == board[4] == board[7]:
    return True,board[1]  
  elif board[2] == board[5] == board[8]:
    return True,board[2] 
  elif board[2] == board[4] == board[6]:
    return True,board[2]
  else:
    return (None,None)

def game_play():
  turn_number = 0
  game = [".", ".", ".", ".", ".", ".", ".", ".", "."]
  initial_game = ["1", "2", "3", "4", "5", "6", "7", "8", "9"]
  game_board(initial_game)
  moves = []

  for i in range(9):   


    result = input("Enter a new location: ")
    if result == "E" or result == "e":
      statement = "The game has been exitted!"
      return statement
    result = int(result)    

    while result in moves or (result > 9 or result < 1):
      if (result > 9 or result < 1):
        print("Please enter a location number between 1 and 9 inclusive!")
      elif result in moves:
        print("Already occupied!")
      result = input("Enter a new location: ")
      if result == "E" or result == "e":
        statement = "The game has been exitted!"
        return statement
      result = int(result)

    moves.append(result)
    print(moves)
    result = result - 1
    turn_number += 1
    initial_game[result] = "P"

    if turn_number % 2 == 0:
        game[result] = "X"
    else:
        game[result] = "O"

    print("ORIGINAL BOARD")
    game_board(game)
    print("\n")

    winner = check_winner(game)
    if winner[0] == True and winner[1] != ".":
      print(winner[1], "has won the game!" )
      end = "Thank you for playing!"
      return end
    
    print("GUIDE")
    game_board(initial_game)
    print("\n Press E to Exit!")
    
  return "Tough Match! The game was a Tie! Thank you for playing!"


def game_intro():
  print("Welcome to TicTacToe.")
  print("To start the game, enter a number (between 1 and 9 inclusive).")
  print("\'O\' starts first.")   
  print("\'X\' starts second.")
  print("P means that a location is occupied. In the start, no location is marked with P")
  print("Following is the board with location numbers.")
  print("YOU MAY PRESS \"E\" TO EXIT!")
  print("\n")

game_intro()   
game_play()
