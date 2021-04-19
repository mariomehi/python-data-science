Foglio 1 Dataframe

Considerate i dati delle partite dei campionati del mondo di calcio dal 1872 al 2020 
disponibili gratuitamente sul sito Kaggle:
https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017
Il file csv (con “,” come separatore) contiene le seguenti colonne:
date home_team away_team home_score away_score tournament city country neutral
esempio:
1872-11-30,Scotland,England,0,0,Friendly,Glasgow,Scotland,FALSE
…
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


Foglio 3 NetworkX 

Contesto 
Consideriamo la formazione e relativa disposizione in campo della squadra del Genoa: 
(1,{"nome": "Perin"}),
(55,{"nome": "Masiello"}),(21,{"nome": "Radovanovic"}),(4,{"nome": "Criscito"}),
(99,{"nome": "Czyborra"}),(20,{"nome": " Strootman"}),(47,{"nome": " Badelj"}),
(16,{"nome": "Zajic"}),(77,{"nome": "Zappacosta"}),
(9,{"nome": "Scamacca"}),(23,{"nome": "Destro"})
 
Consideriamo le seguenti statistiche (inventate) sui passaggi tra i giocatori della squadra per 
un certo numero di partite di campionato:
(1,55,21.0),(55,1,34.0),(1,21,54.0),(21,1,43.0),(1,4,23.0),(4,1,12.0),(4,55,56.0),(55,4,23.0),(21,55,10.0),
(55,21,34.0),(21,4,34.0),(4,21,44.0),(1,99,21.0),(99,1,5.0),(99,55,3.0),(55,99,6.0),(99,21,47.0),
(99,21,47.0),(20,21,15.0),(20,47,80.0),(20,99,16.0),(20,77,35.0),(16,21,5.0),(16,20,34.0),(16,47,45.0),
(16,77,22.0),(16,4,15.0),(16,9,15.0),(16,23,25.0),(16,21,12.0),(77,21,10.0),(77,47,35.0),(77,9,28.0),
(77,23,25.0),(77,16,25.0),(77,20,32.0),(23,9,15.0),(9,23,12.0),(23,77,12.0),(9,77,11.0),(9,16,15.0),
(23,16,21.0),(23,20,2.0),(23,21,4.0),(23,47,15.0),(23,99,11.0),(1,23,25.0),(1,9,14.0),(21,9,8.0),
(21,23,15.0),(4,9,5.0),(4,23,4.0),(47,9,15.0),(47,23,15.0)
Ad es.
(1,4,23.0) indica che Perin ha passato 23 volte la palla a Criscito, ecc.
(continua)Esperimenti proposti 
Usando NetworkX create un grafo diretto dove i nodi sono gli 11 giocatori della formazione 
base (con i loro numeri di maglia) e gli archi pesati rappresentano il numero di passaggi tra 
coppie di giocatori.
Usando le librerie di NetworkX per analisi e navigazione nei grafi provate a valutare strategie 
ed efficacia della formazione base individuando ad esempio:
- Il numero di passaggi effettuati e ricevuti dai singoli giocatori
- i giocatori centrali nel gioco e quelli che facilitano il passaggio di palla tra giocatori
(usando le misure di centralità ecc per grafi senza pesi)
- le zone di campo (difesa, ecc) più o meno coperte (es numero di passaggi in/out)
dalla squadra
- altre misure a vostra scelta
Provate aad analizzare possibili usi dell’algoritmo di PageRank (disponibile in NetworkX) in 
questo caso di studio

