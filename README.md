# padel-league-site

Mirror di pubblicazione per l'app di [Ale6699/PadelsLeague](https://github.com/Ale6699/PadelsLeague) (repo non di mia proprietà, quindi non modificabile direttamente).

Il workflow [`build-and-deploy.yml`](.github/workflows/build-and-deploy.yml):

1. Ogni 15 minuti (o su push manuale / `workflow_dispatch`) fa checkout del repo sorgente pubblico `Ale6699/PadelsLeague` in sola lettura.
2. Builda l'app Vite (`baraonda-padel/`) con `base=/` (dominio custom in root, non sotto-percorso).
3. Aggiunge un file `CNAME` con il dominio custom.
4. Pubblica su GitHub Pages di questo repo.

Sito pubblicato su: **https://padel.sagliettiluca.it**

## Setup DNS richiesto

Aggiungere presso il provider DNS di `sagliettiluca.it` un record:

```
CNAME  padel  sgluca.github.io.
```
