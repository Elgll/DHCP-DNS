# DHCP-DNS
4 sottoreti con DNS  e HTTP server

Obiettivo:
Aggiungere all'esercizio con 4 sybnet le seguenti caratteristiche:
 - ogni rete deve avere il proprio DHCP Server, tutti i PC sono configurati dinamicamente
 - su una delle reti ( a vostra scelta) è presente un server DNS che offre il servizio a tutte e 4 le sottoreti.
- sulla stessa rete del DNS è presente anche un server HTTP che deve esporre le proprie pagine web con dominio "SIRulez.it"

Conoscenze teoriche:
In questo piano di indirizzamento si aggiungerà un computer con funzione di DHCP server ossia quel servizio che permette la configurazione dinamica di eventuali host che si potrebbero aggiungere nella rete quindi: indirizzo ip, gateway, DNS server. Un'altra cosa che diventa possibile in questo piano sarà l'associazione di indirizzo ip-dominio attraverso il DNS server, ossia quel computer che che risolve gli indirizzi ip a partire dal dominio. Il web browser (http server) dopo aver ottenuto l'indirizzo ip dal DNS server memorizza la correlazione rendeno più veloce la comunicazione. (le cose che salto sono scritte nelle altre repositories quindi).

Procedimento:
Come prima cosa si aggiunge un computer con funzione DHCP server ossia in grado di svolgere le funzioni sopra descritte in caso di collegamento da part edi nuovi host.
A questo punto in una delle sottoreti si inserisce un pc che avrà la funzione di DNS server. In esso installandovi il programma che gli permette di avere funzione di dns server sitrova una schermata in cui inserendo un'inidizzo ip, quello del web server quindi, e un nome per il dominio sarà possibile creare l'associazione. Nel web server quindi una volta instalato il programma "web server" e cliccando su start si permetterà l'accesso degli host ai dati inserendo il dominiuo nel web brower (scaricato sugli host). Quindi scegliedo un pc e scrivendo il nome del dominio arriverà al DnS server la richiesta dell'ip che manderà al web server il quale comunicerà drettamente con l'host richiedente inviandogli i dati e visualizzando la pagina cercata.

Conclusione: Il problema che avevo era che solo il pc con ip 172.130.20.2 riesce a raggiungere e ad ottenere l'ip dell web browser, questo perchè non avevo specificato negli altri computer della stessa sottorete e della altre reti il domain server nella loro configurazione quindi non sapevano trovare il DNS server e quidn il'ip a cui corrispondeva il dominio digitato.
