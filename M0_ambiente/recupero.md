# Esercizio 11 — Recupero di file versionati per errore

## Sequenza dei comandi eseguiti

```bash
# Creazione file e commit dell'errore
mkdir -p M0_ambiente/temporanei
echo "Dati temporanei 1" > M0_ambiente/temporanei/file1.tmp
echo "Nota segreta" > M0_ambiente/temporanei/nota.txt
git add M0_ambiente/temporanei
git commit -m "feat: aggiunge file temporanei per errore"

# Tentativo inefficace con .gitignore
echo "M0_ambiente/temporanei/" >> .gitignore

# Diagnosi e Correzione mantenendo i file sul disco
git rm -r --cached M0_ambiente/temporanei
git ls-files M0_ambiente/temporanei

# Commit della risoluzione
git add .gitignore
git commit -m "fix: rimuove file temporanei dal tracciamento e aggiorna gitignore"
```

## Spiegazione in prosa

Il file `.gitignore` ha effetto esclusivamente sui file che non sono ancora stati inclusi nell'indice di Git (ovvero i file nello stato *untracked*). Se un file o una cartella viene inserita nel repository ed è già oggetto di un commit, Git continuerà a monitorarne le modifiche future, ignorando completamente qualsiasi regola restrittiva inserita successivamente nel file `.gitignore`. Per risolvere questa situazione senza eliminare fisicamente i file dal computer, è necessario utilizzare il comando `git rm --cached`. Questo comando cancella selettivamente i file dall'indice dell'area di staging, interrompendo il tracciamento da parte del sistema di controllo versione ma preservando l'integrità dei dati presenti sul disco fisso. Solo dopo questa operazione, le regole del `.gitignore` diventeranno effettive per i file indicati.
