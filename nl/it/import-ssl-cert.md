---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importazione di un certificato SSL
{: #importing-an-ssl-certificate}

Dopo che un certificato SSL è stato emesso per un sito web, è possibile importarlo nel Portale del cliente. Importando i SSL Certificates nel Portale del cliente, è possibile applicarli ai prodotti e ai servizi che potrebbero averne bisogno, come ad esempio l'offload SSL di un programma di bilanciamento del carico. Per impostazione predefinita, i SSL Certificates emessi da IBM© Cloud non sono importati nell'elenco poiché si prevede che vengano manipolati solo dal destinatario. Pertanto, qualsiasi certificato SSL per l'utilizzo con un prodotto o un servizio IBM Cloud deve essere importato manualmente da un utente autorizzato sull'account.

Esegui la seguente procedura per importare un certificato SSL nel Portale del cliente.

1. Dal browser, apri il [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} ed esegui l'accesso nel tuo account.
2. Nella navigazione del Portale del cliente, seleziona **Security > SSL > Certificates**.
3. Fai clic sul link **Import SSL Certificate** nel lato superiore destro della pagina **SSL Certificates**.
2. Immetti i dettagli del certificato SSL. 

	**Nota:** i dettagli immessi nella casella a comparsa Import SSL Certificate devono essere immessi esattamente come sono forniti dalla CA (Certificate Authority - Autorità di certificazione), compresi gli spazi e le interruzioni di riga. Se non vengono immessi esattamente come sono forniti, si verificherà un errore. Compilare i campi nel seguente modo:
  - **Certificate:**  i dettagli del certificato, forniti dalla CA (Certificate Authority - Autorità di certificazione). Si tratta in genere di un blocco di testo alfanumerico.
  - **Private Key:** i dettagli della chiave privata, forniti dalla CA (Certificate Authority - Autorità di certificazione). Si tratta in genere di un blocco di testo alfanumerico.
  - **Intermediate Certificate:** i dettagli del certificato intermedio, forniti dalla CA (Certificate Authority - Autorità di certificazione). I certificati intermedi non sono obbligatori. Tuttavia, se sono disponibili, le informazioni per il certificato SSL dovrebbero essere immesse.
  - **Certificate Signing Request:** i dettagli della CSR (Certificate Signing Request), forniti dalla CA (Certificate Authority - Autorità di certificazione). I dettagli della CRS non sono obbligatori, ma dovrebbero essere forniti se fanno parte del certificato. Non modificare in alcun modo la CSR. Con la CSR può essere inclusa una chiave pubblica e non deve essere sostituita dalla chiave privata.
  - **Notes:** le eventuali note relative al certificato SSL che potrebbero essere utili per gli altri utenti.
4. Fai clic su **Import** per importare il certificato SSL. Fai clic su **Cancel** per annullare l'azione.

Dopo che il certificato SSL è stato importato nel Portale del cliente, verrà archiviato nella schermata SSL Certificates finché non verrà eliminato manualmente. Per tutti i prodotti o i servizi che richiedono i dettagli del certificato SSL, il nuovo certificato SSL sarà presente nell'elenco dei certificati disponibili per l'utilizzo in caso di interazione con la funzione SSL per il prodotto o il servizio desiderati. Puoi aggiornare il certificato o scaricarne in modo protetto i dettagli in qualsiasi momento.
