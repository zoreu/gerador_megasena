**Gerador da mega-sena 2.0**

Copie o código abaixo e cole no [https://extendsclass.com/python.html](https://www.programiz.com/python-programming/online-compiler/)

não esqueça de remover o codigo já presente na pagina antes
e clique em Run

```python
from random import randint
def megasena():
    mega_sena = []
    #sortear 6 numeros
    for i in range(0,6):        
        #encontrar numero não repetido
        while True:
            n = randint(1, 60); #numero aleatório de 1 a 60
            # sorteia numeros com maior probabilidade e não repetidos
            if not n in mega_sena and not n in range(39,43+1) and not n in range(45,52+1) and not n in range(54,57+1) and not n in range(59,60+1):
                # elimina numeros que nao saem na mega da virada
                if not n in [7, 8, 9, 13, 19, 21, 26, 28, 39, 44, 48, 54, 60]:
                    mega_sena.append(n)                    
                    break
    return mega_sena    

def apostas():
    try:
        n_apostas = int(input("Quantas apostas você vai fazer? Digite um numero:"))
        if n_apostas > 0:
            for i in range(0,n_apostas):
                print(megasena())
            preco = n_apostas*5
            print("\n")
            print("Você irá gastar {} Reais".format(preco))
        else:
            print("número invalido")
    except:
        print('valor invalido, digite um número!')

apostas()
```

Download script [megasena.py](https://raw.githubusercontent.com/zoreu/gerador_megasena/main/megasena.py)
