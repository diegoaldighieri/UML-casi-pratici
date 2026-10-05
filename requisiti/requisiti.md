# Esercizio 8 - Libreria online
 
Analisi dei requisiti e diagrammi UML dei casi d'uso per il servizio di acquisto online di una libreria.
 
## Descrizione
 
Una libreria con più punti vendita vuole vendere online libri, CD e DVD solo ai clienti registrati, con consegna tramite corriere. Il cliente paga con un credito versato prima alle casse e non può spendere più di quello. Ogni ordine può avere più prodotti in più copie, e il cliente deve poter vedere online quando l'ordine è stato ricevuto, spedito e consegnato.
 
## Ipotesi
 
- Il cliente si registra in negozio insieme alla prima ricarica
- Non ci sono spese di spedizione
- La consegna viene registrata dal corriere, l'inoltro da un dipendente della libreria
## Requisiti funzionali
 
Priorità: M = indispensabile, S = importante, C = facoltativo.
 
| ID | Requisito | Attore | Priorità |
|---|---|---|---|
| RF01 | Login con username e password | Tutti | M |
| RF02 | Consultare e cercare nel catalogo | Cliente | M |
| RF03 | Vedere la scheda dell'articolo (autore, titolo, editore, foto, descrizione, prezzo) | Cliente | M |
| RF04 | Gestire il carrello scegliendo le quantità | Cliente | M |
| RF05 | Confermare l'ordine solo se il credito basta, e scalarlo | Cliente | M |
| RF06 | Salvare data e ora di ricezione, inoltro e consegna | Sistema | M |
| RF07 | Vedere stato degli ordini e credito residuo | Cliente | M |
| RF08 | Registrare clienti e ricaricare il credito | Cassiere | M |
| RF09 | Registrare l'inoltro al corriere | Addetto spedizioni | M |
| RF10 | Registrare la consegna | Corriere | M |
| RF11 | Gestire gli articoli del catalogo | Amministratore | M |
| RF12 | Avvisare il cliente via e-mail quando cambia lo stato | Sistema | C |
 
## Requisiti non funzionali
 
| ID | Requisito |
|---|---|
| RNF1 | Sicurezza: HTTPS, password con hash, ogni ruolo vede solo le sue funzioni |
| RNF2 | Privacy: dati personali trattati secondo il GDPR |
| RNF3 | Integrità: addebito e ordine salvati insieme, così non si perde credito |
| RNF4 | Disponibilità: sito sempre attivo, con backup regolari |
| RNF5 | Usabilità: il sito funziona su PC, tablet e telefono |
 
## Requisiti di dominio
 
- Comprano solo i clienti registrati
- Il credito si versa solo alle casse dei negozi
- Un ordine non può superare il credito
- Si vendono solo libri, CD e DVD, consegnati con il corriere
## Attori
 
| Attore | Cosa fa |
|---|---|
| Cliente registrato | Ordina e controlla ordini e credito |
| Cassiere | Registra clienti e ricarica il credito |
| Addetto spedizioni | Registra l'inoltro al corriere |
| Corriere | Registra la consegna (attore esterno) |
| Amministratore | Gestisce il catalogo |
 
Cassiere, Addetto e Amministratore sono generalizzati in "Personale libreria".
 
### Conferma ordine
 
1. Il cliente apre il carrello e conferma
2. Il sistema controlla il credito
3. Il sistema scala il totale e salva l'ordine con data e ora
Se il credito non basta, l'ordine non viene creato e il sistema mostra quanto manca.