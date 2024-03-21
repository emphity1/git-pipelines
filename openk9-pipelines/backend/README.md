---
# Pipeline per ogni app lato backend

### L'esecuzione di una pipeline lato backend è triggerata quanto:

- cambia un file lato backend
- cambia un file nelle dipendenze delle varie app 


### Il flusso nel caso delle applicazioni lato backend si riduce a:

- test, build and push immagine
- deploy immagine su ambiente k9-backend (tramite Argo Cd)


---


- nel repo Openk9 si definisce la parte di pipeline che fa test, build and push immagine
- nel repo Openk9 Helm local si definisce la parte di pipeline che fa deploy immagine
- le due pipeline comunicano tramite il meccanismo del trigger