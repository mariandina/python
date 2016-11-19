=============
PYTHON BAISCS
=============

__________________________________________________________________________________________________________________________
**BASICS**

print('''My name is "Gigel \n Frana"''')      ---   Tiparire cu ghilimele si trecere pe randul urmator.

camera = 123
print ("Stau in camera ",camera,".",sep="")   ---   Tiparire estetica cu semn de punctuatie. 

prenume = "Vasile"
nume = "Popescu"
print (prenume, nume)                         ---   Tiparire stringuri

print ("Aceasta este o pula " + "de 19")       ---   Concatenare

Tipuri  de  date. 
1. int -­‐‐    întregi  ---   45
2. float  -­‐‐  în  virgulă  mobilă   ---  45.0 sau 3.1416   
3. string (str)  -­‐‐  șiruri  --- "Marcel"
4. boolean  ---  True,  False  

#Ia numele, varsta si venitul financiar al userului
nume = input("Care e numele tau? ")
varsta = int(input("Cati ani ai? "))
venit = float(input("Care e venitul tau? "))
#Afiseaza datele
print("Iata datele pe care le-ai introdus: ")
print("Nume", nume)
print("Varsta", varsta)
print("Venit", venit)

Operatori: +  -  *  /  //(extrage catul impartirii)  %(extrage restul impartirii) **(ridicare la putere)
Precedența  operatorilor  matematici  
1. Ridicarea  la  putere  se  execută  prima  (**)  
2. Înmulțirea,  împartirea  și  restul  (*  /    //  %)  al  doilea  
3. Adunarea  și  scăderea  ultimele  

*FORMATAREA NUMERELOR*

x = format (12345.6789, ‘.2f’)
print(x) --- 12345.68
Primul argument, care este un număr în virgulă mobilă (12345.6789), este numărul pe care vrem să-­l formatăm.
Al doilea argument este un șir – ‘.2f’ – și reprezintă specificatorul de format.
.2 specifică precizia; el arată că vrem să rotunjim numărul la două zecimale.  
f vine de la float și specifică faptul că numărul pe care-­l formatăm este în virgulă mobilă  
(pentru formatarea întregilor, cum vom vedea, nu se folosește litera f ci d).  
În aceste condiții, funcția format returnează un șir care conține numărul formatat.
Numărul este rotunjit la două zecimale, in sus.

Inserarea separatorului virgulă  
print(format(123456789.456, ‘,.2f’)
123,456,789.46

#Acest program demonstreaza formatarea
#numerelor mari
plata_lunara = 5000.0
plata_anuala = plata_lunara * 12
print("Plata ta anuala este $",\
format(plata_anuala, ",.2f"), \
sep="")

Specificarea unei lățimi minime de spațiu  
Următorul exemplu afișează un număr în câmpul care este de lațime 12:  
>>> print(‘Numarul este’, format(12345.6789, ’12,.2f’))
Numarul este
12,345.68

Folosim simbolul procentului (%) ca să formatăm un număr ca procent:  
>>> print(format(0.5, %))
50.000%
Și  încă  un  exemplu  care  are  0  ca  precizie:  
>>> print(format(0.5, ‘.0%’))
50%

Formatarea întregilor  
Diferențele la formatarea întregilor față de numerele reale (în virgulă mobilă) sunt:  
- folosești  d  în loc de f  
- NU poți specifica precizia  
Ex:  
>>> print(format(123456, ‘d’))
123456
Acuma, același exemplu dar cu separatorul virgulă:  
>>> print(format(123456, ‘,d’))
123,456

*Formatarea șirurilor*

Formatarea sirurilor se face cu acolade ca în exemplul următor: 

nume=input("Enter your name: ")
salut="Salut{}!".format(nume)
print(salut)
 
Șirurile și alte obiecte au o sintaxă specială pentru funcții numită metodă, asociată unui tip particular de obiect. Obiectele de tipul și (str) au o metodă numita format. Sintaxa pentru această metodă conține obiectul urmat de punct urmat de numele metodei și următorii parametri dintre paranteze: 

obiect.nume_metoda(parametri)

În exemplul de mai sus obiectul este șirul ‘Salut {}’ iar metoda este format. Parametrul este nume. După cum se observă la ieșire, acoladele sunt înlocuite  de valoarea preluată din lista parametrilor metodei format. Deoarece acoladele au un înțeles special în formatarea șirurilor, este nevoie de o regulă specială dacă vrem ca ele să fie incluse în formatarea finală a șirurilor. Regula este dublarea acoladelor: ‘{{‘  și  ‘}}’  

a=2
b=3
formatSir="Setul este {{{}, {}}}."
setSir=formatSir.format(a,b)
print(setSir)  
__________________________________________________________________________________________________________________________________________________________________________________ 

**FUNCTII**

*EX.*

def mesaj():
print("Sunt Gigel,")
print("si incerc sa invat Python!")
.
.
.
mesaj()

------------------------------------------------------------------------------------------------------------------------------

def main():
    pula()
    pizda()

def pula():
    x=int(input("x="))
    y=int(input("y="))
    z=x+y
    print("Rezultatul adunarii lui y la x este: ",z)

def pizda():
    nume=input("Enter nume: ")
    prenume=input("Enter prenume: ")
    print("Numele infractorului este: ",nume,prenume)

main()

------------------------------------------------------------------------------------------------------------------------------
Un *argument* este o porțiune de date care este trecută într‐o funcție atunci când funcția este invocată.
Un *parametru* este o variabilă care primește un argument ce este trecut într‐o funcție.

def dublu(nr):
    rez=nr*2
    print(rez)

dublu(5)
-------------------------------------------------------------------------------------------------------------------------------
*Program pentru dublarea unei valori. Cu functii.*

def main():
    v=int(input("Introduceti valoarea: "))
    arata_dublu(v)
def arata_dublu(nr):
    rezultat=nr*2
    print("Rezultatul dublarii numarului este: ",rezultat)
main()

*Mai multe argumente:*

def main():
    a=int(input("Enter number 1: "))
    b=int(input("Enter number 2: "))
    print("Suma lui a cu b este:")
    arata_suma(a, b)
def arata_suma(x, y):
    rezultat = x + y
    print(rezultat)

main()
_______________________________________________________________________________________________________________________________________________________________________

* **IF**

Operatori de comparatie: < ; > ; <= ; >= ; == ; != . Operatori logici: and ; or ; not.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
def numePrenume():
    a=input("introduceti cuvantul1: ")
    b=input("introduceti cuvantul2: ")
    if a==b:
        print ("cuvintele sunt aceleasi")
    else:
        print ("cuvintele difera")

numePrenume()
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
def calcultemp():
    temp = int(input("Enter temperature: "))
    if temp<=0:
        print("freezing")
    elif temp > 0 and temp <= 10:
        print("cold")
    elif temp > 10 and temp <= 15:
        print ("good")
    elif temp > 15 and temp <= 25:
        print("perfect")
    elif temp > 25 and temp <= 30:
        print ("hot")
    elif temp > 30:
        print ("very hot")

calcultemp()
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
def calificImprumut():
    minsal=2000
    minani=3
    sal=eval(input("Introduceti salariul: "))
    if sal < minsal:
        print ("Nu poti lua imprumut din cauza ca ai salariul mai mic de",minsal,"RON.")
    else:
        ani=int(input("Cati ani de vechime aveti? "))
        if ani < minani:
            print("Nu poti lua imprumut din cauza ca ai mai putin de",minani,"ani vechime.")
        else:
            print("Poti lua imprumut pentru ca esti un BOSS.")

calificImprumut()
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
* bucla **WHILE**
O condiție controlată face ca o declarație sau un bloc de declarații să se repete atâta timp cât o condiție e adevărată. Python folosește declarația (bucla) while ca să scrie o astfel de condiție.
Bucla while nu se execută niciodată dacă condiția de început e falsă.
 

numara = 5
while (numara < 10):
      print(numara)
      numara=numara+1
      if numara ==9:
          break
          print("STOPPED")
__________________________________________________________________________________________________________________________________________________________________________________

* bucla **FOR**

#Acest program demonstreaza o bucla for
#care utilizeaza o lista de numere
def main():
print(‘Voi afisa numerele de la 1 la 5’)
for num in [1, 2, 3, 4, 5]:
print(num)
-------------------------------------------------------------------------------------------------------------------------------------------------------
for x in range (5):
    print ("Suck my balls!")
    print (x)
    if x == 2:

for ore in range(24):
    for minute in range(60):
        for secunde in range(60):
            print(ore, ":", minute, ":", secunde)
-------------------------------------------------------------------------------------------------------------------------------------------------------
'''Numara in intervalul 1,10 cu pasul 2.Daca pun -2 la pas,va numara invers...ex: (10,1,-2). Functia range creeaza un tip de obiect numit iterabil.'''
for x in range (1,10,2):
    print ("Suck my balls!")
    print (x)
    if x == 2:
        break
-------------------------------------------------------------------------------------------------------------------------------------------------------
Calcul cu acumulator:

max=5
def main ():
    total=0.0
    print("Se calculeaza suma celor")
    print(max, "numere introduse")
    for counter in range(max):
        number=int(input("Introdu un numar: "))
        total=total+number
    print("Totalul este",total)

main()
--------------------------------------------------------------------------------------------------------------------------------------------------------
*Operatori de atribuire augmentata:*

Aceștia ajută la prescurtarea și deci simplificarea codului.  
Exemple: x= x + 1 se mai poate scrie x+=1  
sau: y= y - 2 se mai poate scrie y-=2  
sau: z= z * 5 se mai poate scrie z*=5  
sau: total = total + number devine total += number 
---------------------------------------------------------------------------------------------------------------
VARIANTA IF:

def main():
    ore=int(input("Introdu numarul de ore lucrate pe saptamana: "))
    if ore < 0 or ore >= 40:
        print ("EROARE , va rugam sa introduceti un numar de ore valid !")
    else:
        salorar=float(input("Introdu salariul orar: "))
        salariu=ore*salorar
        print ("Salariul este: " ,format(salariu, ",.2f"),"RON")

main()

VARIANTA WHILE:

def main():
    ore=int(input("Introdu numarul de ore lucrate pe saptamana: "))
    while ore>40 or ore<0:
        print ("EROARE , va rugam sa introduceti un numar de ore valid !")
        break
        salorar=float(input("Introdu salariul orar: "))
        salariu=ore*salorar
        print ("Salariul este: " ,format(salariu, ",.2f"),"RON")

main()
----------------------------------------------------------------------------------------------------------------

* **MODULE**

*DEFINIRE*

modul.functie
Ex: number = random.randint(1,100)
----------------------------------------------------------------------------------------------------------------
import random
number = random.randint(1,100)
print (number)
----------------------------------------------------------------------------------------------------------------
Ex. definire 5 numere aleatoare intre 1 si 100:
import random
def main():
    for count in range(5):
        number = random.randint(1, 100)
        print(number)
main()   
----------------------------------------------------------------------------------------------------------------
*Functia randrange*
numar = random.randrange(10)
Funcția randrange ia același argument ca funcția range. Diferența este că randrange nu returnează o listă de valori. În loc de asta, ea returnează o valoare aleatoare  dintr‐o secvență de valori. Argumentul – în cazul nostru 10 – specifică limita unei secvențe de valori. Funcția va returna un număr aleator selectat din secvența de la 0  în sus dar nu include limita sfârșitului, adică numărul 10. 
Următoarea declarație specifică și valoarea de început dar și de sfârșit a secvenței:  
numar = random.randrange(5, 10)
Când această declarație e executată, un număr întâmplător cuprins între 5 și 9 va fi atribuit variabilei număr. 
Următorul exemplu specifică o valoare de start, una de sfârșit și o altă valoare:   
numar = random.randrange (0, 101, 10)
Funcția uniform returnează un număr aleator în virgulă mobilă, dar îți permite să specifici media valorilor pe care le‐ai selectat:
numar = random.uniform (1.0, 10.0)
Declarația de mai sus face ca funcția uniform să returneze o valoarea aleatoare în virgulă mobilă situată în gama 1.0 până la 10.0 și s-­o atribuie variabilei numar.
       






_________________________________________________________________________________________________________________________________________________________________________________

* **Python native datatypes:** ::

    * 1. Booleans are either True or False .
    * 2. Numbers can be integers ( 1 and 2 ), floats ( 1.1 and 1.2 ), fractions ( 1/2 and 2/3 ), or even complex numbers.
    * 3. Strings are sequences of Unicode characters, e.g. an HTML document.
    * 4. Bytes and byte arrays, e.g. a JPEG image file.
    * 5. Lists are ordered sequences of values.
    * 6. Tuples are ordered, immutable sequences of values.
    * 7. Sets are unordered bags of values.
    * 8. Dictionaries are unordered bags of key-value pairs.

* **Definirea unei functii boolean in Python** ::
      def eadevarat(ceva):
          if ceva:
             print ("Da, e adevarat")
          else:
             print ("Nu, e fals")

* **Creare lista in Python**
Creating a list is easy: use square brackets to wrap a comma-separated list of values.
a_list = ['a', 'b', 'mpilgrim', 'z', 'example']. Avem a_list[0] = a_list[-5] = 'a', a_list[4] = a_list[-1] = 'example'

* **Taierea unei liste in Pythom**
>>> a_list[1:3] --- ['b', 'mpilgrim']
>>> a_list[1:-1] --- ['b', 'mpilgrim', 'z']
>>> a_list[0:3] --- ['a', 'b', 'mpilgrim']
>>> a_list[:3] --- ['a', 'b', 'mpilgrim']
>>> a_list[3:] --- ['z', 'example']
>>> a_list[:] --- ['a', 'b', 'mpilgrim', 'z', 'example']

* **Adding items to a list**
>>> a_list = ['a'] >>> a_list = a_list + [2.0, 3] --- a_list ['a', 2.0, 3] .. (concatenate)
>>> a_list.extend(['four', 'Ω']) --- a_list ['a', 2.0, 3, True, 'four', 'Ω']
>>> a_list.append([True,False]) --- ['a', 2.0, 3, 'four', 'Ω', [True, False]]
>>> len (a_list) --- 6
>>> a_list.insert(0, 'Ω') --- a_list ['Ω', 'a', 2.0, 3, True, 'four', 'Ω'] '''Inserted an item at .. (indicated by the first argument == the index of the first item in the list that will get bumped out of position)

* **Searching items on a list**
>>> a_list = ['a', 'b', 'new', 'mpilgrim', 'new']
>>> a_list.count('new') --- 2 .. (count() method returns the number of occurrences of a specific value in a list.)
>>> 'new' in a_list --- True .. in operator is slightly faster than using the count() method. The in operator always returns True or False ; it will not tell you how many times the value appears in the list.
>>> 'c' in a_list --- False 
>>> a_list.index('mpilgrim') --- 3 .. the count() method will tell you where in the list a value appears. If you need to know where in the list a value is, call the index() method. By default it will search the entire list, although you can specify an optional second argument of the (0-based) index to start from, and even an optional third argument of the (0-based) index to stop searching.
>>> a_list.index('new') --- 2 .. The index() method finds the first occurrence of a value in the list. In this case, 'new' occurs twice in the list, in a_list[2] and a_list[4] , but the index() method will return only the index of the first occurrence.
>>> a_list.index('c') --- Exception

* **Removing items from list**
>>> a_list = ['a', 'b', 'new', 'mpilgrim', 'new']
>>> a_list[1] --- 'b'
>>> del a_list[1] .. You can use the del statement to delete a specific item from a list.
>>> a_list --- ['a', 'new', 'mpilgrim', 'new']
>>> a_list[1] -- 'new'
 
*Don’t know the positional index? Not a problem; you can remove items by value instead.*

>>> a_list --- ['a', 'new', 'mpilgrim', 'new']
>>> a_list.remove('new') .. The remove() method takes a value and removes the first occurrence of that value from the list.
>>> a_list --- ['a', 'mpilgrim', 'new']
>>> a_list.remove('new')
>>> a_list --- ['a', 'mpilgrim']
>>> a_list.remove('new') --- Exception

*Using pop to remove*
>>> a_list = ['a', 'b', 'new', 'mpilgrim']
>>> a_list.pop() 'mpilgrim' .. When called without arguments, the pop() list method removes the last item in the list and returns the value it removed.
>>> a_list ['a', 'b', 'new']
>>> a_list.pop(1) 'b' .. You can pop arbitrary items from a list. Just pass a positional index to the pop() method. It will remove that item
>>> a_list ['a', 'new']
>>> a_list.pop() 'new'
>>> a_list.pop() 'a'
>>> a_list.pop() --- Exception

* **Lists in boolean context**

>>> is_it_true([])
no, it's false
>>> is_it_true(['a']) 
yes, it's true
>>> is_it_true([False])
yes, it's true

1. In a boolean context, an empty list is false.
2. Any list with at least one item is true.
3. Any list with at least one item is true. The value of the items is irrelevant.

* **TUPLES**
A tuple is an immutable list. A tuple can not be changed in any way once it is created.
>>> a_tuple = ("a", "b", "mpilgrim", "z", "example")
>>> a_tuple --- ('a', 'b', 'mpilgrim', 'z', 'example')
>>> a_tuple[0] ---'a'
>>> a_tuple[-1] --- 'example'
>>> a_tuple[1:3] --- ('b', 'mpilgrim')
1. A tuple is defined in the same way as a list, except that the whole set of elements is enclosed in parentheses instead of square brackets.
2. The elements of a tuple have a defined order, just like a list. Tuple indices are zero-based, just like a list, so the first element of a non-empty tuple is always a_tuple[0] .
3. Negative indices count from the end of the tuple, just like a list.
4. Slicing works too, just like a list. When you slice a list, you get a new list; when you slice a tuple, you get a new tuple.
The major difference between tuples and lists is that tuples can not be changed. In technical terms, tuples are immutable. In practical terms, they have no methods that would allow you to change them. Lists have methods like append() , extend() , insert() , remove() , and pop() . Tuples have none of these methods.
You can slice a tuple (because that creates a new tuple), and you can check whether a tuple contains a particular value (because that doesn’t change the tuple).

* **Tuples in boolean context**
>>> def is_it_true(anything):
        if anything:
           print("yes, it's true")
        else:
           print("no, it's false")
>>> is_it_true(()) --- no, it's false
>>> is_it_true(('a', 'b')) --- yes, it's true
>>> is_it_true((False,)) --- yes, it's true
>>> type((False)) --- <class 'bool'>
>>> type((False,)) --- <class 'tuple'>
1. In a boolean context, an empty tuple is false.
2. Any tuple with at least one item is true.
3. Any tuple with at least one item is true. The value of the items is irrelevant.
4. To create a tuple of one item, you need a comma after the value. Without the comma, Python just assumes you have an extra pair of parentheses, which is harmless, but it doesn’t create a tuple.

* **TUPLES -- ASSIGNING MULTIPLE VALUES AT ONCE**
>>> v = ('a', 2, True)
>>> (x, y, z) = v
>>> x --- 'a'
>>> y --- 2
>>> z --- True
.. This has all kinds of uses. Suppose you want to assign names to a range of values. You can use the built-in range() function with multi-variable assignment to quickly assign consecutive values.
>>> (MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY) = range(7)
>>> MONDAY --- 0
>>> TUESDAY --- 1
>>> SUNDAY --- 6

* The built-in range() function constructs a sequence of integers. (Technically, the range() function returns an iterator, not a list or a tuple, but you’ll learn about that distinction later.) MONDAY , TUESDAY , WEDNESDAY , THURSDAY , FRIDAY , SATURDAY , and SUNDAY are the variables you’re defining. (This example came from the calendar module, a fun little module that prints calendars, like the UNIX program cal. The calendar module defines integer constants for days of the week.)
* Now each variable has its value: MONDAY is 0, TUESDAY is 1 , and so forth.You can also use multi-variable assignment to build functions that return multiple values, simply by returning a tuple of all the values. The caller can treat it as a single tuple, or it can assign the values to individual variables. Many standard Python libraries do this, including the os module.

* **SETS** A set is an unordered “bag” of unique values. A single set can contain values of any immutable datatype. Once you have two sets, you can do standard set operations like union, intersection, and set difference.

*Creating a set: 
>>> a_set = {1}
>>> a_set --- {1}
>>> type(a_set) --- <class 'set'>
>>> a_set = {1, 2}
>>> a_set --- {1, 2}

1. To create a set with one value, put the value in curly brackets ( {} ).
2. Sets are actually implemented as classes, but don’t worry about that for now.
3. To create a set with multiple values, separate the values with commas and wrap it all up with curly brackets.

>>> a_list = ['a', 'b', 'mpilgrim', True, False, 42]
>>> a_set = set(a_list)
>>> a_set --- {'a', False, 'b', True, 'mpilgrim', 42}
>>> a_list --- ['a', 'b', 'mpilgrim', True, False, 42]

1. To create a set from a list, use the set() function. (Pedants who know about how sets are implemented will point out that this is not really calling a function, but instantiating a class. I promise you will learn the difference later in this book. For now, just know that set() acts like a function, and it returns a set.)
2. As I mentioned earlier, a single set can contain values of any datatype. And, as I mentioned earlier, sets are unordered. This set does not remember the original order of the list that was used to create it. If you were to add items to this set, it would not remember the order in which you added them.

>>> a_set = set()
>>> a_set set()
>>> type(a_set) --- <class 'set'>
>>> len(a_set) --- 0
>>> not_sure = {}
>>> type(not_sure) --- <class 'dict'>

1. To create an empty set, call set() with no arguments.
2. The printed representation of an empty set looks a bit strange. Were you expecting {} , perhaps? That would denote an empty dictionary, not an empty set. You’ll learn about dictionaries later in this chapter.
3. Despite the strange printed representation, this is a set...
4. ...and this set has no members.
5. Due to historical quirks carried over from Python 2, you can not create a

*MODIFYING A SET*

There are two different ways to add values to an existing set: the add() method, and the update() method.
>>> a_set = {1, 2}
>>> a_set.add(4)
>>> a_set --- {1, 2, 4}
>>> len(a_set) --- 3
>>> a_set.add(1)
>>> a_set --- {1, 2, 4}
>>> len(a_set) --- 3
1. The add() method takes a single argument, which can be any datatype, and adds the given value to the set.
2. This set now has 3 members.
3. Sets are bags of unique values. If you try to add a value that already exists in the set, it will do nothing. It
won’t raise an error; it’s just a no-op.
4. This set still has 3 members.

>>> a_set = {1, 2, 3}
>>> a_set --- {1, 2, 3}
>>> a_set.update({2, 4, 6})
>>> a_set --- {1, 2, 3, 4, 6}
>>> a_set.update({3, 6, 9}, {1, 2, 3, 5, 8, 13})
>>> a_set --- {1, 2, 3, 4, 5, 6, 8, 9, 13}
>>> a_set.update([10, 20, 30])
>>> a_set --- {1, 2, 3, 4, 5, 6, 8, 9, 10, 13, 20, 30}
1. The update() method takes one argument, a set, and adds all its members to the original set. It’s as if you called the add() method with each member of the set.
2. Duplicate values are ignored, since sets can not contain duplicates.
3. You can actually call the update() method with any number of arguments. When called with two sets, the update() method adds all the members of each set to the original set (dropping duplicates).
4. The update() method can take objects of a number of different datatypes, including lists. When called with a list, the update() method adds all the items of the list to the original set.

*REMOVING ITEMS FROM A SET*
There are three ways to remove individual values from a set. The first two, discard() and remove() , have one subtle difference.
>>> a_set = {1, 3, 6, 10, 15, 21, 28, 36, 45}
>>> a_set --- {1, 3, 36, 6, 10, 45, 15, 21, 28}
>>> a_set.discard(10)
>>> a_set --- {1, 3, 36, 6, 45, 15, 21, 28}
>>> a_set.discard(10)
>>> a_set --- {1, 3, 36, 6, 45, 15, 21, 28}
>>> a_set.remove(21)
>>> a_set --- {1, 3, 36, 6, 45, 15, 28}
>>> a_set.remove(21) --- Exception

1. The discard() method takes a single value as an argument and removes that value from the set.
2. If you call the discard() method with a value that doesn’t exist in the set, it does nothing. No error; it’s just a no-op.
3. The remove() method also takes a single value as an argument, and it also removes that value from the set.
4. Here’s the difference: if the value doesn’t exist in the set, the remove() method raises a KeyError exception.

>>> a_set = {1, 3, 6, 10, 15, 21, 28, 36, 45}
>>> a_set.pop() --- 1
>>> a_set.pop() --- 3
>>> a_set.pop() --- 36
>>> a_set --- {6, 10, 45, 15, 21, 28}
>>> a_set.clear()
>>> a_set --- set()
>>> a_set.pop() --- Exception

1. The pop() method removes a single value from a set and returns the value. However, since sets are unordered, there is no “last” value in a set, so there is no way to control which value gets removed. It is completely arbitrary.
2. The clear() method removes all values from a set, leaving you with an empty set. This is equivalent to a_set = set() , which would create a new empty set and overwrite the previous value of the a_set variable.
3. Attempting to pop a value from an empty set will raise a KeyError exception.

*SET OPERATIONS*
>>> a_set = {2, 4, 5, 9, 12, 21, 30, 51, 76, 127, 195}
>>> 30 in a_set --- True
>>> 31 in a_set --- False
>>> b_set = {1, 2, 3, 5, 6, 8, 9, 12, 15, 17, 18, 21}
>>> a_set.union(b_set) --- {1, 2, 195, 4, 5, 6, 8, 12, 76, 15, 17, 18, 3, 21, 30, 51, 9, 127}
>>> a_set.intersection(b_set) --- {9, 2, 12, 5, 21}
>>> a_set.difference(b_set) --- {195, 4, 76, 51, 30, 127}
>>> a_set.symmetric_difference(b_set) --- {1, 3, 4, 6, 8, 76, 15, 17, 18, 195, 127, 30, 51}

1. To test whether a value is a member of a set, use the in operator. This works the same as lists.
2. The union() method returns a new set containing all the elements that are in either set.
3. The intersection() method returns a new set containing all the elements that are in both sets.
4. The difference() method returns a new set containing all the elements that are in a_set but not b_set .
5. The symmetric_difference() method returns a new set containing all the elements that are in exactly one
of the sets.
Three of these methods are symmetric.

>>> b_set.symmetric_difference(a_set) --- {3, 1, 195, 4, 6, 8, 76, 15, 17, 18, 51, 30, 127}
>>> b_set.symmetric_difference(a_set) == a_set.symmetric_difference(b_set) --- True
>>> b_set.union(a_set) == a_set.union(b_set) --- True
>>> b_set.intersection(a_set) == a_set.intersection(b_set) --- True
>>> b_set.difference(a_set) == a_set.difference(b_set) --- False

1. The symmetric difference of a_set from b_set looks different than the symmetric difference of b_set from a_set , but remember, sets are unordered. Any two sets that contain all the same values (with none left over) are considered equal.
2. And that’s exactly what happens here. Don’t be fooled by the Python Shell’s printed representation of these sets. They contain the same values, so they are equal.
3. The union of two sets is also symmetric.
4. The intersection of two sets is also symmetric.
5. The difference of two sets is not symmetric. That makes sense; it’s analogous to subtracting one number from another. The order of the operands matters. Finally, there are a few questions you can ask of sets.

>>> a_set = {1, 2, 3}
>>> b_set = {1, 2, 3, 4}
>>> a_set.issubset(b_set) --- True
>>> b_set.issuperset(a_set) --- True
>>> a_set.add(5)
>>> a_set.issubset(b_set) --- False
>>> b_set.issuperset(a_set) --- False

1. a_set is a subset of b_set — all the members of a_set are also members of b_set .
2. Asking the same question in reverse, b_set is a superset of a_set , because all the members of a_set are also members of b_set .
3. As soon as you add a value to a_set that is not in b_set , both tests return False .

*SETS IN A BOOLEAN CONTEXT*

You can use sets in a boolean context, such as an if statement.
>>> def is_it_true(anything):
...
if anything: print("yes, it's true")
else: print("no, it's false")...
>>> is_it_true(set()) --- no, it's false
>>> is_it_true({'a'}) --- yes, it's true
>>> is_it_true({False}) --- yes, it's true

1. In a boolean context, an empty set is false.
2. Any set with at least one item is true.
3. Any set with at least one item is true. The value of the items is irrelevant.

* **DICTIONARIES**

A dictionary is an unordered set of key-value pairs. When you add a key to a dictionary, you must also ad a value for that key. (You can always change the value later.) Python dictionaries are optimized for retrieving the value when you know the key, but not the other way around. Creating a dictionary is easy. The syntax is similar to sets, but instead of values, you have key-value pairs. Once you have a dictionary, you can look up values by their key.

>>> a_dict = {'server': 'db.diveintopython3.org', 'database': 'mysql'}
>>> a_dict --- {'server': 'db.diveintopython3.org', 'database': 'mysql'}
>>> a_dict['server'] --- 'db.diveintopython3.org'
>>> a_dict['database'] --- 'mysql'
>>> a_dict['db.diveintopython3.org'] --- Exception

1. First, you create a new dictionary with two items and assign it to the variable a_dict . Each item is a key- value pair, and the whole set of items is enclosed in curly braces.
2. 'server' is a key, and its associated value, referenced by a_dict['server'] , is 'db.diveintopython3.org' .
3. 'database' is a key, and its associated value, referenced by a_dict['database'] , is 'mysql' .
4. You can get values by key, but you can’t get keys by value. So a_dict['server'] is 'db.diveintopython3.org' , but a_dict['db.diveintopython3.org'] raises an exception, because
'db.diveintopython3.org' is not a key.

*MODIFYING A DICTIONARY*
Dictionaries do not have any predefined size limit. You can add new key-value pairs to a dictionary at any time, or you can modify the value of an existing key. Continuing from the previous example: 
>>> a_dict --- {'server': 'db.diveintopython3.org', 'database': 'mysql'}
>>> a_dict['database'] = 'blog'
>>> a_dict --- {'server': 'db.diveintopython3.org', 'database': 'blog'}
>>> a_dict['user'] = 'mark' 
>>> a_dict --- {'server': 'db.diveintopython3.org', 'user': 'mark', 'database': 'blog'}
>>> a_dict['user'] = 'dora'
>>> a_dict --- {'server': 'db.diveintopython3.org', 'user': 'dora', 'database': 'blog'}
>>> a_dict['User'] = 'mark'
>>> a_dict --- {'User': 'mark', 'server': 'db.diveintopython3.org', 'user': 'dora', 'database': 'blog'}

1. You can not have duplicate keys in a dictionary. Assigning a value to an existing key will wipe out the old value.
2. You can add new key-value pairs at any time. This syntax is identical to modifying existing values.
3. The new dictionary item (key 'user' , value 'mark' ) appears to be in the middle. In fact, it was just a coincidence that the items appeared to be in order in the first example; it is just as much a coincidence that they appear to be out of order now.
4. Assigning a value to an existing dictionary key simply replaces the old value with the new one.
5. Will this change the value of the user key back to "mark"? No! Look at the key closely — that’s a capital U in "User" . Dictionary keys are case-sensitive, so this statement is creating a new key-value pair, not overwriting an existing one. It may look similar to you, but as far as Python is concerned, it’s completely different.
Dictionaries aren’t just for strings. 

Dictionary values can be any datatype, including integers, booleans, arbitrary objects, or even other dictionaries. And within a single dictionary, the values don’t all need to be the same type; you can mix and match as needed. Dictionary keys are more restricted, but they can be strings, integers, and a few other types. You can also mix and match key datatypes within a dictionary.

Let's tear that apart in the interactive shell.
>>> SUFFIXES = {1000: ['KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'],
...
1024: ['KiB', 'MiB', 'GiB', 'TiB', 'PiB', 'EiB', 'ZiB', 'YiB']}
>>> len(SUFFIXES)
1
2
>>> 1000 in SUFFIXES
2
True
>>> SUFFIXES[1000]
3
['KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB']
>>> SUFFIXES[1024]
4
['KiB', 'MiB', 'GiB', 'TiB', 'PiB', 'EiB', 'ZiB', 'YiB']
>>> SUFFIXES[1000][3]
5
'TB'
1. Like lists and sets, the len() function gives you the number of keys in a dictionary.
2. And like lists and sets, you can use the in operator to test whether a specific key is defined in a dictionary.
3. 1000 is a key in the SUFFIXES dictionary; its value is a list of eight items (eight strings, to be precise).
4. Similarly, 1024 is a key in the SUFFIXES dictionary; its value is also a list of eight items.
5. Since SUFFIXES[1000] is a list, you can address individual items in the list by their 0-based index.

DICTIONARIES IN A BOOLEAN CONTEXT
You can also use a dictionary in a boolean context, such as an if statement.
>>> def is_it_true(anything):
...
if anything:
print("yes, it's true")
else:
print("no, it's false")
...
>>> is_it_true({}) --- no, it's false
>>> is_it_true({'a': 1}) --- yes, it's true

1. In a boolean context, an empty dictionary is false.
2. Any dictionary with at least one key-value pair is true.

* **NONE**

None is a special constant in Python. It is a null value. None is not the same as False . None is not 0. None is not an empty string. Comparing None to anything other than None will always return False . None is the only null value. It has its own datatype ( NoneType ). You can assign None to any variable, but you can not create other NoneType objects. All variables whose value is None are equal to each other.
>>> type(None) --- <class 'NoneType'>
>>> None == False --- False
>>> None == 0 --- False
>>> None == '' --- False
>>> None == None --- True
>>> x = None
>>> x == None --- True
>>> y = None
>>> x == y --- True

In a boolean context, None is false and not None is true.
>>> def is_it_true(anything):
...
if anything:
print("yes, it's true")
else:
print("no, it's false")
...
>>> is_it_true(None) --- no, it's false
>>> is_it_true(not None) --- yes, it's true



















































