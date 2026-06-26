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

I PDF completi vengono pubblicati come artifact separati e privati del workflow:

- `cv-it-pdf` — PDF completo del CV italiano
- `cv-en-pdf` — PDF completo del CV inglese
- `cv-en-cbi-unibo-pdf` — PDF inglese mirato per candidatura CBI/Unibo
- `cv-fr-public-pdf` — PDF francese public-safe
- `cv-fr-alternance-ia-data-pdf` — PDF francese mirato alternance IA/data/RAG
- `cv-fr-alternance-ia-spatial-pdf` — PDF francese mirato alternance IA/sistemi critici/spatial
- `cv-it-retail-pdf` — PDF privato del CV italiano orientato a retail/lavoro part-time
- `cv-it-retail-photo-pdf` — PDF privato del CV italiano retail con foto

Le versioni public-safe, senza numero di telefono, sono compilate da:

- `cv/it/CV-IT-public.tex`
- `cv/en/CV_EN-public.tex`
- `cv/fr/CV_FR-public.tex`
- `cv/fr/CV_FR-alternance-ia-data.tex`
- `cv/fr/CV_FR-alternance-ia-spatial.tex`

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
 
