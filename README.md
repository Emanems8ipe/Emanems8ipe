
import abc
import random


import  pickle
class EventModel():
    def __init__(self):
        self.eventos=[]
    def __iadd__(self, metodo):
        self.eventos.append(metodo)
        return  self
    def __isub__(self, metodo):
        self.eventos.remove(metodo)
        return  self
    def __call__(self, *args, **kwargs):
        for e in self.eventos:
            e(*args,**kwargs)


class IPessoa(abc.ABC):
    @abc.abstractmethod
    def exame(self,exames):
        pass

class Pessoa(IPessoa):
    Total = 0
    def __del__(self):
        pessoa.Total -=1

    def __new__(cls, *args, **kwargs):
        instancia = super(Pessoa, cls).__new__(cls)
        return instancia

    def __init__(self,nome,Turma,exames):
        self.nome = nome
        self.turma=turma
        pessoa.Total+=1
    def __str__(self):
        return f'nome:{self.nome} turma:{self.turma}'
    def __call__(self, *args, **kwargs):
        print(f'                       ({self.nome})                     ')
        for str in args:
            print(str)
        for k,v in kwargs.items():
            print(k,v)
        print(self.__str__())
        print('--------------------------------------------------------------------')




Aluno1 = Pessoa('Joao',0,0)
print(Pessoa.Total)


def __new__(cls, *args, **kwargs):
    instance = super(Pessoa, cls).__new__(cls)
    return instance
