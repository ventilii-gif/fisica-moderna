# Fisica moderna — introduzione alla fisica quantistica

Web app didattica interattiva in italiano per il quinto anno di liceo scientifico.
Tutto in un unico file: [`index.html`](index.html).

## Come aprirla

Scarica `index.html` e aprilo con un doppio clic in qualunque browser recente.
Non serve installare nulla né avviare un server. L'unica risorsa esterna è il CDN
di MathJax per la tipografia delle formule: senza connessione l'app resta
utilizzabile, ma le formule appaiono in notazione TeX grezza.

## Struttura

1. **Teoria** — crisi della fisica classica (corpo nero, catastrofe ultravioletta,
   ipotesi di Planck), effetto fotoelettrico, effetto Compton, dualismo
   onda-particella e ipotesi di de Broglie, doppia fenditura con elettroni,
   modelli atomici da Thomson a Bohr con spettri a righe, principio di
   indeterminazione di Heisenberg, funzione d'onda e interpretazione
   probabilistica. Diagrammi in SVG, formule con MathJax.
2. **Simulazioni** — tre esperimenti su canvas: effetto fotoelettrico (lunghezza
   d'onda, intensità, materiale del catodo, tensione frenante, grafico
   *K*<sub>max</sub>(*f*)); doppia fenditura con costruzione del pattern punto per
   punto, confronto una/due fenditure e rivelatore di percorso; modello di Bohr
   con transizioni animate e spettro accumulato.
3. **Esercizi** — 12 problemi a difficoltà crescente con aiuti progressivi,
   verifica numerica tollerante (virgola o punto, notazione scientifica) e
   diagnostica degli errori tipici.
4. **Verifica finale** — 10 domande di teoria e 5 problemi, punteggio e
   spiegazioni alla consegna. Ogni sezione ha inoltre il proprio quiz a riscontro
   immediato (10 + 5) sui soli argomenti di quella sezione. La posizione della
   risposta esatta è casuale e viene rimescolata a ogni tentativo.

## Note su grafica e accessibilità

- Tema giorno/notte con transizione animata; la scelta viene ricordata nel browser
  e, al primo accesso, segue la preferenza di sistema.
- Palette viola-ambra-teal, senza coppie rosso-verde per codificare informazione.
  Unica eccezione dichiarata: le righe spettrali dell'idrogeno usano i colori reali
  corrispondenti alla loro lunghezza d'onda (H-α rosso, H-β ciano, H-γ e H-δ
  blu-violetto), perché il colore è in quel caso un dato fisico.
- Layout responsive, verificato anche su viewport da 390 px. I canvas si
  ridisegnano al ridimensionamento della finestra e al cambio di tema.
- Le simulazioni usano scale spaziali e temporali compresse per essere leggibili:
  dove la scala non è realistica è indicato nel pannello.

## Costanti usate

*h* = 6,626·10⁻³⁴ J s = 4,136·10⁻¹⁵ eV s · *hc* = 1240 eV nm · *c* = 3,00·10⁸ m/s ·
*m*<sub>e</sub> = 9,11·10⁻³¹ kg · 1 eV = 1,602·10⁻¹⁹ J · *a*₀ = 0,0529 nm ·
*E*₁(H) = −13,6 eV

## Pubblicazione con GitHub Pages

Il sito è il file `index.html` nella radice del repository, quindi non serve alcun
passaggio di build.

**Opzione A — deploy da branch (la più semplice).**
In *Settings → Pages → Build and deployment*, scegli come *Source* la voce
**Deploy from a branch**, poi il branch `main` e la cartella `/ (root)`, e salva.
Dopo un paio di minuti il sito è su `https://<utente>.github.io/fisica-moderna/`.

**Opzione B — deploy con GitHub Actions.**
In *Settings → Pages* scegli come *Source* la voce **GitHub Actions**, poi avvia il
workflow *Deploy su GitHub Pages* dalla scheda *Actions* (si esegue solo su
richiesta manuale, così non produce esecuzioni fallite se Pages non è ancora
attivo).

Su piano gratuito GitHub Pages richiede un repository pubblico.
