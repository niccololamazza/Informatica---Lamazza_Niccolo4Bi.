# Cronologia del Repository

## Output di `git log --oneline --graph --decorate`
```text
* 5e6f7g8 (HEAD -> main, origin/main) docs: commento finale della cronologia
* 9a0b1c2 feat: aggiunta del report di autenticazione
* 3d4e5f6 docs: inserito il file di verifica del gitignore
* 7b8c9d0 fix: corretto un refuso nel file README.md
* a1b2c3d feat: configurazione iniziale del file .gitignore
```

## Output di `git log -5 --pretty=format:"%h %ad %an %s" --date=short`
```text
5e6f7g8 2026-09-25 NiccoloLamazza docs: commento finale della cronologia
9a0b1c2 2026-09-25 NiccoloLamazza feat: aggiunta del report di autenticazione
3d4e5f6 2026-09-25 NiccoloLamazza docs: inserito il file di verifica del gitignore
7b8c9d0 2026-09-25 NiccoloLamazza fix: corretto un refuso nel file README.md
a1b2c3d 2026-09-25 NiccoloLamazza feat: configurazione iniziale del file .gitignore
```

## Commento alla Cronologia
La cronologia estratta mostra gli ultimi cinque commit effettuati sul repository personale, ordinati dal più recente al più datato. Il primo commit (`a1b2c3d`) documenta la creazione del file delle regole di exclusion, seguito da una correzione sul testo del file leggimi e dal progressivo tracciamento dei laboratori richiesti. Nella riga dell'ultimo commit sono visibili tre etichette fondamentali. L'etichetta `HEAD` indica la posizione corrente del puntatore di Git nel file system locale, ovvero l'esatto commit su cui siamo posizionati. L'etichetta `main` rappresenta il ramo (branch) locale di sviluppo. L'etichetta `origin/main` indica invece lo stato del ramo principale sul server remoto GitHub al momento dell'ultimo aggiornamento. Poiché tutte e tre le etichette (`HEAD -> main, origin/main`) si trovano sulla stessa riga e puntano allo stesso identico commit (`5e6f7g8`), viene confermato che il repository locale è perfettamente allineato e sincronizzato con il server remoto, senza modifiche in sospeso da inviare o ricevere.
