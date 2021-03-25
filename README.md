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
