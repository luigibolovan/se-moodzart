# Sisteme expert - proiect

# Sistem expert de recomandare de melodii

## Tehnologii
 - **Python 3.x**
 - **JSON**

## Utilizare
Interfata cu utilizatorul a acestui program este realizata prin intermediul consolei. \
In prima faza, utilizatorului ii este cerut anul de nastere pentru a-i putea sugera melodii din deceniul in care acesta s-a nascut. \
![year](year_question.png) \
Apoi utilizatorul isi va alege dispozitia curenta dintr-o lista care va fi afisata in consola, iar pe baza anului introdus si a dispozitiei curente, sistemul ii va sugera o lista de melodii(nume + link youtube) bazandu-se pe cele doua input-uri. \
![mood](mood_question.png) \
![result](result.png) \

## Descrierea sistemului
Sistemul este alcatuit din 
 - masina de inferenta(```main.py```)
 - setul de reguli(```rules.json```)
 - setul de facts(```facts.json```)

Bazandu-se pe datele introduse de utilizator, sistemul isi va verifica setul de reguli din fisierul ```rules.json``` si isi va construi lista de concluzii partiale in cazul in care se vor gasi reguli pentru input-ul utilizatorului. In caz contrar, utilizatorul va fi anuntat ca nu a fost gasita nicio regula. \
Dupa ce au fost gasite concluzii partiale pentru input(an & dispozitie), sistemul va cauta concluziile finale bazandu-se pe cele partiale.
In cazul in care au fost gasite concluziile finale, se vor cauta in functie de acestea melodiile in fisierul ```facts.json```.
