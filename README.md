# Matrix og Lineære Ligninger med Python
Dette repository indeholder noter og kodeeksempler relateret til matrix, lineære ligninger og grundlæggende lineær algebraoperationer udført med Python.

## Indhold
1. **Introduktion til Matricer**
   - Hvad er en matrix ?
   - Matrixoperation: addition, Subtraktion, Skalarmultiplikation
   - Matrixtransponering

# Løsninger af lineære ligningssystemer med python og NumPy
I denne del vil vi se på, hvordan løser lineære ligningssystemer ved hjælp af python og NumPy-pakker. NumPy er en kraftig pakke til numerisk begregning, der gør det nemt at arbejde med matricer og vektorer.

## *Trin 1:* importer NumPy 
Først skal vi importere NumPy for at kunne bruge dets funktioner til matriceregning og løsning af ligningssystermer. Dette gøres med følgende importstatement:

    import numpy as np

## *Trin 2:* Definér koefficientmatricen A og vektormatricen B
Vi skal definere koeffientmatricen A og vektormatricen B basseret på dit specifikke lineære ligningssystem. For eksempel, hvis system ser sådan ud: 

**Ligning 1:** $2x + 4y=10$, 
<br/>
**Ligning 2:** $4x - 2y=8$

Så er koefficientmatricen A og vektormatricen B som følger:

    A = np.array([[2, 3],
                  [4, -2]])
                  
    B = np.array([10, 8])




