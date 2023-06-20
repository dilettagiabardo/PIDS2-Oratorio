# PIDS2-Oratorio
Progetto di Ingegneria del Software 2 - Magistrale Informatica UNIUD

Il progetto consiste nell'ottimizzare alcuni processi relativi all'iscrizione all'oratorio estivo. 
L'iscrizione avveniva tramite la compilazione di un Google Form apposito. I dati venivano poi inseriti automaticamente all'interno del Google Sheets, che tramite il codice inserito in App Script, completava un Google Doc apposito con i dati relativi all'iscrizione. Poi questo file veniva stampato dalla parrocchia e fatto firmare alla riunione precedente all'inizio dell'oratorio estivo.

Le richieste da parte del parrocco sono state due:
1. Rendere la compilazione del Form più semplice per le persone iscritte da anni. Quindi, al fronte di un utente che negli anni passati ha già iscritto i propri figli, inviare il sondaggio con alcuni campi precompilati in base ai dati precedenti.
2. Inviare il documento creato con i dati relativi all'iscrizione, in formato pdf, tramite mail all'utente. Questo per permettere la stampa e la firma in vista della raccolta dei documenti da parte del parroco.

Quindi il procedimento per l'utente è il seguente:
1. 1.1 Se l'utente è stato iscritto negli anni precedenti: Inserire la Mail precedentemente usata nel primo form;

   1.2 Se l'utente non è stato iscritto negli anni precedenti: Inserire la propria Mail nel primo form.
3. 2.1 Controllare la casella posta, aprire la mail "Iscrizione Oratorio" e copiare ed incollare il link precompilato in una nuova pagina;

   2.2 Controllare la casella posta, aprire la mail "Iscrizione Oratorio" e copiare ed incollare il link in una nuova pagina.
5. Inserire i propri dati nel secondo form;
6. Controllare la casella posta, aprire la mail "Pdf Iscrizione Oratorio" e recuperare il file pdf.



Per la realizzazione del progetto sono stati creati due file di App Script, il primo(Send Mail from Google Sheets) collegato al primo form ed il secondo al secondo form(Send Mail with Pdf Attachment).

Il primo permette l'invio della Mail in base a quanti figli ci sono ed in base al fatto che la mail sia o meno presente nel database.
Il secondo permette l'invio della Mail con il pdf in allegato. Inoltre permette la creazione del pdf stesso.


Per quando riguarda il recupero dei dati dal database e la creazione del link precompilato si è proceduto in questo modo:
E' stato prima generato un link precompilato del secondo form e per ogni elemento del database è stata utilizzata questa formula: =SOSTITUISCI(TestoPrincipale; TestoDaSostituire; TestoCheSostituisce)
In modo tale da sostituire gli elementi del link e rendere il sondaggio precompilato a doc.

