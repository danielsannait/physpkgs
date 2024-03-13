# ```physpkgs```: latex packages for physics
Collezione di pacchetti per un articolo scritto in LaTeX (```\documentclass{article}``` o simili) riguardo ambiti di fisica e matematica con testo in italiano. Compatibile con ```sapthesis```.

## Utilizzo
Dopo aver inserito il file ```physpkgs.sty``` nella cartella del file di tex principale, caricare il pacchetto con ```\usepackage{physpkgs}```.
Per un utilizzo senza molte pretese questo è quanto basta per scrivere un articolo.

### Opzioni del pacchetto ```\usepackage[options]{physpkgs}```
- ```article```: _default_, per impaginare un A4 per classi article, report o simili.
- ```noindent```: rimuove tutte le indentazioni ad inizio paragrafo.
- ```sectionbarrier``` e ```subsectionbarrier```: attivano automaticamente un ```\FloatBarrier``` alla fine di ogni sezione (la prima) o di ogni sezionamento (la seconda), quindi anche ```\subsubsection{}```.
- ```tikz```: include i pacchetti tikz e circuitikz per le grafiche vettoriali
- ```code```: include il pacchetto listings per i listati con una formattazione per python.
- ```biblatex```: includ il pacchetto biblatex e sceglie come sorgente ```ref.bib```.

Se si sceglie la documentclass ```sapthesis```, automaticamente sono selezionati i pacchetti compatibili e attivata l'opzione ```biblatex```.

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



