# ```physpkgs```: latex packages for physics
Collezione di pacchetti per un articolo scritto in Latex (```\documentclass{article}``` o simili) riguardo ambiti di fisica e matematica con testo in italiano.

## Utilizzo
Dopo aver inserito il file ```physpkgs.sty``` nella cartella del file di tex principale, caricare il pacchetto con ```\usepackage{physpkgs}```.
Per un utilizzo senza molte pretese questo è quanto basta per scrivere un articolo.

Per esigenze specifiche (e non sono affatto rare), potrebbe essere necessario rimuovere alcuni pacchetti oppure modificarne le impostazioni: aprendo il file .sty è possibile modificarne il contenuto per adattarlo alle necessità del proprio progetto.

## Riassunto delle _features_ principali

I pacchetti selezionati introducono le seguenti _features_ principali:
- Layout: formattazione pagina per un A4 a margini di 2 cm su-giù, 3 cm sx-dx, testo giustificato, appendici, sommario.
- Matematica, fisica: varie per equazioni (alfabeti di simboli speciali), unità di misura (```\unit{}```) e ambienti per teoremi e definizioni.
- Riferimenti: citazioni migliorate in italiano (```\cref{}```), link estetici (hyperref), note a piè pagina.
- Float: immagini, tabelle con celle multiriga e multicolonna, _caption_ migliorate, ```\FloatBarrier``` automatici al cambio di _section_ (da attivare).
- Codice: _snippet_ per listati di Python (_color-coded_).

## Note sulle funzioni aggiunte

Sono state aggiunte alcune funzioni utili:
- ```\lqq[]``` è ispirata a ```\qq{}``` di physics e introduce virgola e testo a fianco di equazioni in ambiente matematica (al suo interno si può ridichiarare un ambiente matematica con ```$...$```).
- ```sapred``` è il colore rosso de 'La Sapienza' di Roma.

## Errori e incompatibilità tra pacchetti

Sono stati risolti tutti gli errori di compilazione e selezionato accuratamente l'ordine e le opzioni di importazione dei pacchetti per assicurare una buona compatibilità.

In particolare si fa notare che:
- ```\qty{}``` è in conflitto tra i pacchetti physics e siunitx. Si è scelto di preservare la funzione di physics come parentesi adattive. Per la funzione di siunitx di numero con unità si può usare ```\SI``` (e.g. ```\SI{10}{m}```)
- ntheorem è in conflitto con amsthm (disabilitato)



