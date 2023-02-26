import random
x = ""
lst = [" " for i in range(9)]
for i in range(3):
  x += "{} | {} | {}\n"
  if i<2 : x+= "----------\n"

print(x.format(lst[0],lst[1],lst[2],lst[3],lst[4],lst[5],lst[6],lst[7],lst[8]))

while True:
  if lst[0]==lst[1]==lst[2]=="x" or lst[3]==lst[4]==lst[5]=="x" or lst[6]==lst[7]==lst[8]=="x" or lst[0]==lst[3]==lst[6]=="x" or lst[1]==lst[4]==lst[7]=="x" or lst[2]==lst[5]==lst[8]=="x" or lst[0]==lst[4]==lst[8]=="x" or lst[2]==lst[4]==lst[6]=="x":
    print("computer won the game")
    break
  elif lst[0]==lst[1]==lst[2]=="o" or lst[3]==lst[4]==lst[5]=="o" or lst[6]==lst[7]==lst[8]=="o" or lst[0]==lst[3]==lst[6]=="o" or lst[1]==lst[4]==lst[7]=="o" or lst[2]==lst[5]==lst[8]=="o" or lst[0]==lst[4]==lst[8]=="o" or lst[2]==lst[4]==lst[6]=="o":
    print("User won the game")
    break
  elif " " not in lst:
    print("Draw match")
    break
  while True:
    p = random.randrange(0,9)
    if lst[p] != " ":
      continue
    elif " " not in lst:
      break
    else:
      lst[p] = "x"
      print(x.format(lst[0],lst[1],lst[2],lst[3],lst[4],lst[5],lst[6],lst[7],lst[8]))
      break
  if " " not in lst:
    continue
  while True:
    inp = int(input("Enter your choice between 1 to 9 :")) - 1
    if lst[inp] != " ":
      continue
    elif " " not in lst:
      break
    else:
      lst[inp] = "o"
      print(x.format(lst[0],lst[1],lst[2],lst[3],lst[4],lst[5],lst[6],lst[7],lst[8]))
      break