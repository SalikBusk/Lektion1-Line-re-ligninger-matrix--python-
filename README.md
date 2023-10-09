# Matrix og Lineære Ligninger med Python
Dette repository indeholder noter og kodeeksempler relateret til matrix, lineære ligninger og grundlæggende lineær algebraoperationer udført med Python.

## Indhold
1. **Lineære ligningssystemer**
   - hvad er en lineære ligningssystem
   - Visualisering af lineære ligninger ved hjælp af python
   - løsninger af lineært system
     
3. **Matrix eliminering**
   -
4. **Matricer i python**

5. **Matrix løsning i python**
   - Rækkeoperationer
   - Echelonform
     
6. **Begreber*** 


## Visualisering af lineære ligninger
For at få en bedre forståelse af, hvordan to lineære funktioner krydser hinanden og finde ud af, hvor mange timer der kræves for at tjene det samme beløb i begge job, vil vi visualisere de to ligninger på et plot ved hjælp af Python og Matplotlib.

### Python-kode til visualisering
Vi kan bruge Python til at udføre denne opgave. Her er den nødvendige kode:

    # importer de nødvendige pakker
    import numpy as np
    import matplotlib.pyplot as plt

    # Generer 1000 jævnt fordelte værdier mellem 0 og 50 som x
    x = np.linspace(0, 50, 1000)

    # Beregn y-værdierne for begge ligninger
    y1 = 1000 + 150 * x
    y2 = 500 + 200 * x

    # Lav et plot for tutoring med guld farve
    plt.plot(x, y1, color='gold', label='Tutoring')

    # Lav et plot for deltidsjob med blå farve
    plt.plot(x, y2, color='blue', label='Part-time job')

    # Tilføj labels til akserne
    plt.xlabel('Antal undervisningstimer om ugen')
    plt.ylabel('Beløb tjent om ugen')

    # Tilføj en legende for at identificere de to funktioner
    plt.legend()

    # Vis plottet
    plt.show()


Dette stykke Python-kode genererer et plot, der viser de to lineære funktioner, hvor de skærer hinanden, og hvordan beløbet tjent afhænger af antallet af undervisningstimer om ugen. Visualiseringen giver os en intuitiv forståelse af, hvordan løsningerne afhænger af variablerne i de lineære ligninger.

    
## Løsninger af lineære ligningssystemer med python og NumPy
I denne del vil vi se på, hvordan løser lineære ligningssystemer ved hjælp af python og NumPy-pakker. NumPy er en kraftig pakke til numerisk begregning, der gør det nemt at arbejde med matricer og vektorer.



### **Trin 1:** importer NumPy 
Først skal vi importere NumPy for at kunne bruge dets funktioner til matriceregning og løsning af ligningssystermer. Dette gøres med følgende importstatement:

    import numpy as np



### **Trin 2:** Definér koefficientmatricen A og vektormatricen B
Vi skal definere koeffientmatricen A og vektormatricen B basseret på dit specifikke lineære ligningssystem. For eksempel, hvis system ser sådan ud: 

**Ligning 1:** $2x + 4y=10$, 
<br/>
**Ligning 2:** $4x - 2y=8$

Så er koefficientmatricen A og vektormatricen B som følger:

    A = np.array([[2, 3],
                  [4, -2]])
                  
    B = np.array([10, 8])



### **Trin 3:**  Løs Ligningssystemet
Brug **np.linalg.solve()-funktionen** til at finde løsningen for x:

    x = np.linalg.solve(A, B)



### **Trin 4:** Udskriv Resultatet
Endelig kan du udskrive resultaterne for de ukendte variabler, fx x og y:

    print("Løsningen er:")
    print("x =", x[0])
    print("y =", x[1])
