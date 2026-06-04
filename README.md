# CV

Repository privata per versionare il curriculum in più lingue.

## Struttura

- `cv/it/` — curriculum in italiano (`CV-IT.tex`)
- `cv/en/` — curriculum in inglese (`CV_EN.tex`)
- `data/` — dati condivisi e note di aggiornamento
- `assets/` — foto, loghi o altri asset opzionali

## File principali

- Italiano: `cv/it/CV-IT.tex`
- English: `cv/en/CV_EN.tex`

## Build automatico

La repository contiene un workflow GitHub Actions (`.github/workflows/build-cv.yml`) che compila automaticamente i PDF quando cambiano i file `.tex` su `main` o in una pull request.

I PDF completi vengono pubblicati come artifact separati e privati del workflow:

- `cv-it-pdf` — PDF completo del CV italiano
- `cv-en-pdf` — PDF completo del CV inglese

Le versioni public-safe, senza numero di telefono, sono compilate da:

- `cv/it/CV-IT-public.tex`
- `cv/en/CV_EN-public.tex`

Queste versioni vengono pubblicate su GitHub Pages per l'accesso da browser.

## Workflow consigliato

1. Aggiornare prima i contenuti nella lingua principale.
2. Riportare le modifiche nelle altre lingue.
3. Controllare che GitHub Actions compili correttamente i PDF.
4. Fare commit con messaggi chiari, ad esempio:
   - `Aggiorna esperienze lavorative`
   - `Add English CV version`
   - `Update skills section`

## Privacy

Questo repository può contenere dati personali. Mantenerlo privato e non pubblicare file con informazioni sensibili non necessarie.
