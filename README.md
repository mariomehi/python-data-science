# python-dataframe
Python: Dataframe Pandas

Dati delle partite dei campionati del mondo di calcio dal 1872 al 2020

Il file csv (con “,” come separatore) contiene le seguenti colonne:
date home_team away_team home_score away_score tournament city country neutral

esempio:
1872-11-30,Scotland,England,0,0,Friendly,Glasgow,Scotland,FALSE
...
2020-12-09,United States,El Salvador,6,0,Friendly,Fort Lauderdale,US,FALSE

Caricate i dati nel csv in un Dataframe Pandas.

Scegliete quindi la vostra squadra preferita che chiameremo nel seguito S.

Usando maschere, filtri, ecc risolvete le seguenti query riguardandi S:

- calcolare il numero di vittorie, sconfitte e pareggi e la media dei goal fatti e subiti
indicati nel seguito come “indicatori” dalla squadra S
- graficare l’andamento delle partite giocate da S in termini di goal fatti e subiti
- selezionare tutte le squadre con indicatori migliori di S
- calcolare il numero massimo di vittorie consecutive di S



Foglio 2 Itertools


Considerate nuovamente i dati delle partite dei campionati del mondo di calcio dal 1872 al 2020 
disponibili gratuitamente sul sito Kaggle:
https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017
Il file csv (con “,” come separatore) contiene le seguenti colonne:
date home_team away_team home_score away_score tournament city country neutral
Esempio:
1872-11-30,Scotland,England,0,0,Friendly,Glasgow,Scotland,FALSE
…
2020-12-09,United States,El Salvador,6,0,Friendly,Fort Lauderdale,US,FALSE
Usate generatori e librerie di itertools per realizzare una pipeline con valutazione lazy che realizza la 
seguente sequenza di trasformazioni e filtri:
1) Leggere i dati riga per riga (usando un generatore)
2) Convertire ogni record in un dizionario usando i nomi di colonna come nomi di attributi e 
unendo tutti i dizionari in una sola lista
Es. la riga sul match US-El Salvador del 2020-12-09 deve essere convertita in:
{'date': '2020-12-09', 
'home_team': 'United States', 
'away_team': 'El Salvador', 
'home_score': '6', 
'away_score': '0', 
'tournament': 'Friendly', 
'city': 'Fort Lauderdale', 'country': 'United States', 'neutral': 
'FALSE'}
(hint: provate ad usare zip)
3) Elaborare i dizionari ottenuti al passo 2 per calcolare usando le librerie di itertool (e quindi 
ottimizzando l’uso della memoria) la somma totale di goal realizzati dall’Italia in tutte le partite 
della World Cup.
4) Usate memory_profiler (https://pypi.org/project/memory-profiler/) o strumenti simili per 
analizzare l’uso della memoria e tempi del p

