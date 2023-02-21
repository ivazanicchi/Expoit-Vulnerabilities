# Expoit-Vulnerabilities
Come si possono ottenere le password in un database di utenti? La risposta a questa domanda può essere effettuata in due modi, di cui in entrambi i casi abbiamo bisogno degli hash:
Nel primo caso abbiamo sfruttato la SQL injection (Blind) in cui si ha ottenuto il cookie di sessione attraverso burpsuite e successivamente abbiamo utilizzato il tool SQLMAP per ottenere il database con tutti gli utenti iscritti ad un determinato SitoWeb (in questo caso Metasploit). Da qui infatti abbiamo ottenuto l'hash delle password (un metodo di criptaggio delle password) e sfruttando il tool JohnTheRipper le abbiamo anche decriptate.
Nel secondo caso invece cambia solo il procedimento iniziale da cui, nella sezione XSS Stored abbiamo inserito uno script che permettesse di inviarci su di una porta in ascolto il cookie di sessione dell'utente, dal quale poi abbiamo effettuato lo stesso procedimento del passo precedente.

Per maggiori dettagli sui tool utilizzati e le sezioni analizzate, questi i link di riferimento:
SQL Injection: https://it.wikipedia.org/wiki/SQL_injection
XSS Stored: https://it.wikipedia.org/wiki/Cross-site_scripting
SQLMap: https://it.wikipedia.org/wiki/Sqlmap
JohnTheRipper: https://it.wikipedia.org/wiki/John_the_Ripper
