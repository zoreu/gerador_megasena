**Gerador da mega-sena**

Copie o código abaixo e cole no https://extendsclass.com/python.html
e clique em Run

    from random import randint;
    def megasena():
        mega_sena = []
        #sortear 6 numeros
        for i in range(0,6):        
            #encontrar numero não repetido
            while True:
                n = randint(1, 60); #numero aleatório de 1 a 60
                if not n in mega_sena:            
                    mega_sena.append(n)                    
                    break;
        return mega_sena    
    
    def apostas():
        try:
            n_apostas = int(input("Quantas apostas você vai fazer? Digite um numero:"))
            if n_apostas > 0:
                for i in range(0,n_apostas):
                    print(megasena())
                preco = n_apostas*4.50
                print("\n")
                print("Você irá gastar {} Reais".format(preco))
            else:
                print("número invalido")
        except:
            print('valor invalido, digite um número!')
    
    apostas()  

Download script [megasena.py](https://raw.githubusercontent.com/zoreu/gerador_megasena/main/megasena.py)
