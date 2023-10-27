# physpkgs (physics packages)
Collezione di pacchetti per un articolo scritto in Latex (```\documentclass{article}```) riguardo ambiti di fisica e matematica con testo in italiano.

## Utilizzo
Dopo aver inserito il file ```physpkgs.sty``` nella cartella del file di tex principale, caricare il pacchetto con ```\usepackage{physpkgs}```.
Per un utilizzo senza molte pretese questo è quanto basta.

Per esigenze specifiche (e non sono affatto rare), potrebbe essere necessario rimuovere alcuni pacchetti oppure modificarne le impostazioni: aprendo il file .sty è possibile modificarne il contenuto per adattarlo alle proprie necessità.

## Riassunto delle _features_ principali

I pacchetti selezionati introducono le seguenti _features_ principali:
- Layout: formattazione pagina per un A4 a margini di 2 cm, testo giustificato, appendici, sommario.
- Matematica, fisica: varie per equazioni (alfabeti di simboli speciali), unità di misura (```\unit{}```) e ambienti per teoremi e definizioni.
- Riferimenti: citazioni migliorate in italiano (```\cref{}```), link estetici (hyperref), note a piè pagina.
- Float: immagini, tabelle con celle multiriga e multicolonna, caption migliorate, ```\FloatBarrier``` automatici al cambio di section (da attivare).
- Codice: snippet per listati di Python (color-coded).

## Note sulle funzioni aggiunte

Sono state aggiunte alcune funzioni utili:
- ```\lqq{}``` è ispirata a ```\qq{}``` di physics e introduce virgola e testo a fianco di equazioni in ambiente matematica (al suo interno si può ridichiarare un ambiente matematica con ```$...$```).
- ```sapred``` è il colore rosso de 'La Sapienza' di Roma.

## Errori e incompatibilità tra pacchetti

Sono stati risolti tutti gli errori di compilazione e selezionato accuratamente l'ordine e le opzioni di importazione dei pacchetti per assicurare una buona compatibilità.

In particolare si fa notare che:
- ```\qty{}``` è in conflitto tra i pacchetti physics e siunitx. Si è scelto di preservare la funzione di physics come parentesi adattive. Per la funzione di siunitx di numero con unità si può usare ```\SI``` (e.g. ````\SI{10 m}```
- 


