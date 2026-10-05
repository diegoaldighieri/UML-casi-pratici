# Esercizio 8 - Libreria online
 
Una libreria con più negozi vuole vendere online libri, CD e DVD solo ai clienti registrati, con consegna a casa tramite corriere. Si paga con un credito ricaricato alla cassa del negozio.
 
## Requisiti funzionali
 
| ID | Requisito |
|---|---|
| RF1 | Login per i clienti registrati |
| RF2 | Consultare il catalogo e la scheda di ogni articolo (autore, titolo, editore, foto, descrizione) |
| RF3 | Ordinare uno o più prodotti, anche in più copie |
| RF4 | Accettare l'ordine solo se il credito basta e poi scalarlo |
| RF5 | Salvare data e ora di ricezione, inoltro al corriere e consegna |
| RF6 | Vedere lo stato degli ordini e il credito residuo |
| RF7 | Registrare clienti e ricaricare il credito (cassiere) |
| RF8 | Gestire gli articoli del catalogo (amministratore) |
 
## Requisiti non funzionali
 
- Sicurezza: HTTPS e password cifrate
- Privacy: dati dei clienti trattati secondo il GDPR
- Usabilità: il sito deve funzionare anche da telefono
## Requisiti di dominio
 
- Comprano solo i clienti registrati
- Il credito si ricarica solo in negozio
- Si vendono solo libri, CD e DVD
## Attori
 
Cliente registrato, Cassiere, Addetto spedizioni, Corriere, Amministratore.