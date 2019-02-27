import random
SP={1:'DDfFa',2:'AAA',3:'Rrrae',4:'rtrfe'} # наш словарь
n=random.randint(1,len(SP)) # рандомное слово
SP_Word=list(SP[n]) # выборо слова и асписывание по буквам
SP_cop=['*']*len(SP_Word) # дублер *
SP_povt=[] # заводим дополнительный словарь  для исключения повторяющихся букв
print(*SP_Word )
print ('hi, guess the word I made, you have 5 tries.')
i=1
while i<=5:
    print('Guess a letter:')
    X = input()
    if X.upper() in SP_povt:
        print('this letter is already guessed')
        continue
    SP_povt+=X.upper()
    if X.upper() in SP_Word or X.lower() in SP_Word  :
        for j in range(len(SP_Word)):
            if X.upper()==SP_Word[j]or X.lower()==SP_Word[j]:
                SP_cop[j]=SP_Word[j]
        print(*SP_cop,)   
        if SP_cop==SP_Word:
            print('You won!')
            break
        continue
    else:  
        print( 'Missed, mistake ',i,' out of 5')
        print(*SP_cop,) 
    i+=1
if i>5:
  print('You lost!')
