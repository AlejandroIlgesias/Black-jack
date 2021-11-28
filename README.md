# Black-jack

Dirección del repositorio:[Black-jack.git](https://github.com/AlejandroIlgesias/).

<br>
<img height="2000" src="https://github.com/AlejandroIlgesias/Black-jack/blob/main/Diagrama%20de%20flujodel%20black%20jack.drawio.png" />
<br>

El programa que aqui se muestra comienza creando una baraja y colocando un dealer (el crupier) y un visitor (el jugador), cuyas clases son todas.
El código del que hablamos se muestra a continuación:

```
from random import choice, sample
 
cartas = {
   chr(0x1f0a1): 11,
   chr(0x1f0a2): 2,
   chr(0x1f0a3): 3,
   chr(0x1f0a4): 4,
   chr(0x1f0a5): 5,
   chr(0x1f0a6): 6,
   chr(0x1f0a7): 7,
   chr(0x1f0a8): 8,
   chr(0x1f0a9): 9,
   chr(0x1f0aa): 10,
   chr(0x1f0ab): 10,
   chr(0x1f0ad): 10,
   chr(0x1f0ae): 10,
}
 
print("cartas: {}".format(" ".join(cartas. keys())))
print("puntos: {}".format(list(cartas.values())))
 
print("1\ Interacción estánar sobre un diccionario")
for carta, valor in cartas.items ():
     print ("la carta {} vale {}" .format(carta, valor))
 
print("2\ interación ordenada sobre un diccionador rio")
for carta in sorted (cartas.keys ()):
   print ("la carta {} vale {}" .format(carta, cartas[carta]))
 
print("3\ Black Jack")
lista_cartas = list (cartas)
 
print("Ha seleccionado:", end= " ")
carta= choice(lista_cartas)
score = cartas [carta]
print(carta, end=" ")
carta = choice (lista_cartas)
score += cartas[carta]
print(carta,end=" ")
print(" >>> su puntuación es de", score)
 
main_banca = sample(lista_cartas, 2)
score_banca = sum(cartas[carta] for carta in main_banca)
print ("La banca tiene: {} {} >> su score es {}".format (main_banca[0],
                                                           main_banca[1],
                                                           score_banca))
```
                               
