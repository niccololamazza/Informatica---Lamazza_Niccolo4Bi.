## Esercizio 2

PS Z:\> cd "Z:\Documenti"
PS Z:\Documenti> mkdir esercizio-percorsi


    Directory: Z:\Documenti


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        18/09/2026     14:03                esercizio-percorsi


PS Z:\Documenti> cd Z:\Documenti\esercizio-percorsi\
PS Z:\Documenti\esercizio-percorsi> mkdir dati


    Directory: Z:\Documenti\esercizio-percorsi


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        18/09/2026     14:05                dati


PS Z:\Documenti\esercizio-percorsi> mkdir risultati


    Directory: Z:\Documenti\esercizio-percorsi


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        18/09/2026     14:05                risultati


PS Z:\Documenti\esercizio-percorsi> cd dati
PS Z:\Documenti\esercizio-percorsi\dati> cd ../risultati
PS Z:\Documenti\esercizio-percorsi\risultati> Get-Location

Path
----
Z:\Documenti\esercizio-percorsi\risultati