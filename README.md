# CV

Repository privata per versionare il curriculum in più lingue.

## Struttura

- `cv/it/` — curriculum in italiano (`CV-IT.tex`)
- `cv/en/` — curriculum in inglese (`CV_EN.tex`)
- `cv/fr/` — curriculum in francese e varianti mirate per alternance
- `data/` — dati condivisi e note di aggiornamento
- `assets/` — foto, loghi o altri asset opzionali

## File principali

- Italiano accademico/AI: `cv/it/CV-IT.tex`
- English academic/AI: `cv/en/CV_EN.tex`
- English CBI/Unibo application variant: `cv/en/CV_EN-cbi-unibo.tex`
- Français public-safe: `cv/fr/CV_FR-public.tex`
- Français alternance IA/data/RAG: `cv/fr/CV_FR-alternance-ia-data.tex`
- Français alternance IA/systèmes critiques/spatial: `cv/fr/CV_FR-alternance-ia-spatial.tex`
- Italiano retail part-time: `cv/it/CV-IT-retail.tex`
- Italiano retail part-time con foto: `cv/it/CV-IT-retail-photo.tex`

## Build automatico

La repository contiene un workflow GitHub Actions (`.github/workflows/build-cv.yml`) che compila automaticamente i PDF quando cambiano i file `.tex` su `main` o in una pull request.

Il workflow compila **solo** le versioni public-safe, senza numero di telefono:

- `cv/it/CV-IT-public.tex`
- `cv/en/CV_EN-public.tex`
- `cv/fr/CV_FR-public.tex`
- `cv/fr/CV_FR-alternance-ia-data.tex`
- `cv/fr/CV_FR-alternance-ia-spatial.tex`

Queste versioni vengono pubblicate su GitHub Pages per l'accesso da browser.

Le versioni con numero di telefono (`CV-IT.tex`, `CV_EN.tex`, `CV_EN-cbi-unibo.tex`, `CV-IT-retail.tex`, `CV-IT-retail-photo.tex`) **non** vengono compilate in CI, perché la repository è pubblica: vanno compilate in locale (vedi sotto).

## Compilare le versioni private in locale

I file con numero di telefono usano la macro `\PrivatePhone`, definita in `cv/private-contact.tex` — un file **non tracciato da git** (vedi `.gitignore`), così il numero non finisce mai nella cronologia del repository pubblico.

Per compilarle in locale:

1. Copia il template: `cp cv/private-contact.tex.example cv/private-contact.tex`
2. Apri `cv/private-contact.tex` e inserisci il numero reale in `\PrivatePhone`
3. Compila normalmente, ad esempio: `cd cv/it && latexmk -pdf CV-IT.tex`

`cv/private-contact.tex` resta solo sulla tua macchina.

## Workflow consigliato

1. Aggiornare prima i contenuti nella lingua principale.
2. Riportare le modifiche nelle altre lingue.
3. Controllare che GitHub Actions compili correttamente i PDF.
4. Fare commit con messaggi chiari, ad esempio:
   - `Aggiorna esperienze lavorative`
   - `Add English CV version`
   - `Update skills section`

## Privacy

Questo repository è **pubblico**. Il numero di telefono non è mai committato (vedi sopra): resta solo in `cv/private-contact.tex`, ignorato da git. Prima di aggiungere nuovi contenuti, verificare che non contengano altri dati sensibili non necessari.
 
