
Riferimento

- https://git-scm.com/book/en/v2/
- http://nfarina.com/post/9868516270/git-is-simpler
- https://www.youtube.com/watch?v=4XpnKHJAok8&t
- https://www.youtube.com/watch?v=vKRZKau-8MY
- http://gitimmersion.com/
- http://rogerdudler.github.io/git-guide/



Testo

- Benvenuti e presentazione agenda
- Command line: basic introduction
	Che cos'è la command line, o meglio command line interface o cli?
	E' uno strumento che ci permette di "parlare" direttamente con il computer, in realta' con il sistema operativo, senza dover passare per l'interfaccia grafica
	che in alcuni casi potrebbe rallentare le operazioni (questo perchè è uno strato intermedio che puo' richiedere diversi step per eseguire un unico comando).
		Ad esempio: se devo muovermi in una specifica cartella da cli posso farlo con un comando mentre da GUI sono necessari più click

	Da questa "guerra" cli vs gui sono nati ovvimente tantissimi meme più o meno simpatici.

	Tipi di cli -> unix like vs windows
		Noi prenderemo come riferimento git-bash, che ci aiuta ad avere alcuni tool da cli di Linux (ma è purtroppo una emulazione) su windows e offre l'integrazione di git

	Ma perchè introduzione alla command line? ci serve esclusivamente per utilizzare git?
		No, ci sono anche sw di GUI.
		Però spesso questi sw con GUI nascondono delle insidie se non si sa di preciso cosa stiamo facendo.
		Quindi se si conosce la cli si può utilizzare al meglio anche la GUI.
		Inoltre se è vero che conoscendo la cli è facile utilizzare la GUI, il viceversa non è affatto vero.

	Vediamo qualche esempio di comandi linux che utilizzeremo su git bash, ad esempio per navigare nei repository git.

- VCS
	Introduzione: per capire cosa sono i software "vcs" cerchiamo di capire prima di tutto quale problema risolvono
	abbiamo dei file sui quali vogliamo lavorare, vogliamo tracciare ogni modifica che facciamo ai file, possibilmente in un modo
	sicuro e che ci permetta di ripercorrere la "storia" dei file.
	Come facciamo?
	Esempio 1, assegnamo un nome al file ogni volta che lo modifichiamo...ma prima o poi non sapremmo piu che nome dargli
	Esempio 2, allora diamo un numero progressivo che indichi la progressione delle modifiche...ma immaginiamo di avere un progetto di 100 o piu file, non è fattibile a mano
		Da qui i software VCS!

	Da descrizione: "un software di version control sono sistemi che permettono di registrare modifiche a file, in modo da poterle rinavigare in seguito"

	I VCS si dividono in due tipi diversi
		Centralizzati: Questa tipologia di VCS è del tipo client-server.
					   significa che ci permette di avere un database centralizzato su una macchina server, dove vengono salvate tutte le modifiche ai file.
					   In questo modo è possibile condividere queste modifiche con tra diverse persone.
					   Questa tipologia di SVC è stato lo standard dei VCS per diversi anni.
					   Però questa tipologia ha alcuni punti negativa. Il principale è che il server centralizzato rappresenta un "single point of failure", cioè un punto
					   critico il quale, nel caso gli succeda qualcosa, bloccherebbe il funzionamento del sw stesso.
					   In tal caso infatti nessuno potrebbe collaborare in nessun modo o salvare le modifiche ai file.
		Distribuiti:   In questa tipologia di VCS, viene meno il meccanismo client-server.
					   Infatti qui ogni partecipante ha un completo clone di tutto il repository sulla propria macchina, con tutta la storia inclusa.
					   Inoltre può appoggiarsi (MA non è necessario) ad un server centrale in modo da poter condividere le modifiche prendendo un unico repository come
					   punto di riferimento.
					   Di conseguenza, se il server muore, si può continare a lavorare passandosi le modifiche tra i repository client.
					   Inoltre il server puo' essere ricreato a partire da uno dei repository dei client.
					   Altro vantaggio è che, avendo tutti i repository in locale, è possibile lavorare offline, ovvero continuare ad utilizzare il sw di versionamento
					   senza essere online; ovviamente non potremo condividere queste modifiche, ma nel frattempo saranno versionate.
					   Git rientra in questa tipologia di SVC.
- Why git
			Vediamo innanzitutto un po' di storia di git.

			[Angry Torvalds!]
			Git è stato creato dallo stesso creatore del kernel linux, Linus Torvalds... GAF CON LA FOTO e spiego perchè li era arrabbiato con Nvidia e del fatto che è
			piuttosto istintivo nel suo modo di fare, il che me lo fa apprezzare ancora di piu'.

			*Scusate, ricominciamo*

			[Foto torvalds > linux (con anno) > icona bit tracker (con anno) > git (con anno)]
			Git è stato creato dallo stesso creatore del kernel linux, Linus Torvalds, nel 2005 in quanto serviva un nuovo tool SVC proprio per lo sviluppo open source del
			kernel linux, ovvero quel componente core di tutti i sistemi operativi GNU/Linux che letteralmente permettono al web di essere tale in quanto è presente su piu' del 90% dei server
			a livello mondiale.
			Questo era fondamentale in quando da sempre lo sviluppo del kernel linux è stato portato avanti da tantissimi sviluppatori dislocati in tutto il mondo essendo
			un progetto open source.
			All'inizio dello sviluppo di linux, tutte le modifiche apportate al codice venivano spedite per email a Linus e lui stesso (se approvate) le portava
			all'interno del progetto.
			Successivamente vennero concesse gratuitamente delle license di un software VCS ai sviluppatori del kernel, per poi essere in seguito negate.
			Da qui l'idea di Linus di concentrarsi alcuni mesi sullo sviluppo di un nuovo software VCS, ovviamente open source, che avesse tutte le caratteristiche di un
			sw VCS ideale, cioè che fosse veloce, distribuito, efficiente per quanto riguarda la gestione di progetti grandi, che supporti sviluppi "non lineari" (quindi branch),
			e che abbia un design semplice.
			Cosi nacque git.

			[slide nome git]
			Cosa significa il nome?
			Come possiamo vedere dalla slide Linus stesso afferma che dipende un pò dall'umore che si ha, c'è una definizione più "professionale" come la terza, fino ad una piu'
			"emotiva" come l'ultima.

- Who use it
			[slide a lot of people]
			Chi usa git?
			Tante persone!
			Si ma quante precisamente?

			[slide A LOT OF PEOPLE!]
			TANTE PERSONE!

			[foto enterprise]
			Git è ormai molto diffuso da anni anche nel mondo enterprise dello sviluppo software, ad esempio in Red Hat, SUSE, Google, Netflix e Amazon solo per citarne alcuni
			sia per i loro progetti open source che per i loro progetti "interni".

			[foto enterprise + foto wiki]
			Ma non possiamo dimenticarci di tutto il mondo open source

			[slide github]
			Sono nate infatti piattaforme online per collaborare a progetti open source, github la più utilizzata, che come dice il nome basa il proprio workflow di lavoro
			proprio su git e possiamo vedere che numeri di persone e repository possiede.
			- 43 milioni di utenti (https://github.com/search?q=type%3Auser&type=Users)
			- 176 milioni di repository (https://github.com/search?q&type=Repositories refreshando diverse volte esce quanti sono i repo)

- Git basics
			[slide "so you told me: git, linux, linus ecc.. faccia confusa su git"]
			Ok, abbiamo passato solo l'introduzione e abbiamo parlato già di tante cose.
			Linux kernel, github, abbiamo visto un pinguino e altre icone carine.
			Potreste ancora essere piuttosti confusi.

			Veniamo finalmente al dunque.

			[slide git vs svn, team foundation server, mercurial]
			Cos'è git? In che modo si distingue dagli altri SVC sw? Quale sono le sue caratteristiche principali?
			Affronteremo queste domande nelle prossime slide.

			Capire cos'è git e come lui stesso internamente funziona (ad alto livello ovviamnete) ci aiuterà veramente tanto per capire come utilizzarlo al meglio.
			Inizieremo con il capire come git salva le modifiche ai file e come si comporta rispetto ad esse, soprattutto facendo un paragone con gli altri SVC che,
			per i più junior, aiuterà loro per comprendere un modo alternativo di fare la stessa cosa, mentre a chi ha usato altri prodotti SVC aiuterà a capirne le differenze.

			Proprio questo aspetto quindi [ossia come git e gli altri svc pensano ai dati] è la principale differenza tra Git e gli altri software VCS (es. SVN).

			"Snapshots, Not Differences"
			[slide vcs delta-based]
			La maggior parte degli altri SVC , da un punto di vista concettuale, salvano informazioni riguardo le modifiche ai file come una lista di "cambiamenti", di "differenze"
			agli stessi.
			Quindi quello che fanno è organizzare le informazioni che contengono come  un set di file e di modifiche apportate a questi nel tempo, un approccio "delta-based".

			[slide git stream of snapshots]
			Git tratta i dati del progetto sul quale è utilizzato come una serie di snapshot del progetto stesso.
			Ogni volta che "salviamo" delle modifiche (spoiler: in seguito useremo il termine "commit" [e da li l'orribile ma appropiato "committato"] al posto di parlare di
			modifche salvate) quello che Git fa è prendere una "foto", uno snapshot dello stato attuale dei file in quel momento e salvare un riferimento a quella foto.
			Per ragioni di efficienza, se dei file non sono stati modificati allora git non li salverà all'interno dello snapshot ma terrà all'interno di questa un
			link all'ultime versione del file che era stata già salvata.
			Stiamo parlando quindi di salvataggio di snapshot e non di differenze, e quindi possiamo dire che Git pensa ai dati come ad uno "stream di queste foto",
			uno "stream di snapshots".

			Quella appena introdotta è un importante e fondamentale differenza, in quanto rende Git una sorta di mini file-system, in parole piu' semplici una sorta di
			database contentente le info del progetto, con potenti strumenti da utilizzare per lavorarci sopra, cosa ben piu' avanzata di tra virgolette "un semplice VCS".
			Ad ogni modo vedremo i vantaggi di questa differenza in Git quando cominceremo a parlare di branch.

			"Nearly Every Operation Is Local"
			[slide sul fatto che i repository su cui lavoriamo sono in realtà in locale]
			Altra importante caratteristica di Git che lo differenzia dagli altri VCS è che, per quanto abbiamo già detto, Git è distribuito, il che significa che quando lavoriamo
			su un repo git questo è in realtà in locale, abbiamo l'intera storia del progetto in locale.
			Di conseguenza quasi tutte le operazioni che ci permettono di interagire con il repo sono "offline" e quindi immediate.
				Ad esempio, se vogliamo consultare la storia del progetto con Git accederemo alla storia salvata nel repo sul nostro computer; al contrario con gli altri VCS,
				in particolare quelli centralizzati, la storia del progetto non è sul nostro computer, manderemo quindi una richiesta al server, questo leggerà la storia
				del progetto e ce la invierà in risposta.

			"Git Has Integrity"
			[foto repo git, con db .git]
			Abbiamo discusso quindi di come git salva i dati in una sorta di database.
			Vediamo cosa significa.
			Questo in foto è un repository git di esempio, possiamo vedere la distinzione tra i file nel repository, quelli che noi abbiamo voluto versionare e che sono da noi
			direttamente utilizzabili e il db git, ovvero la cartella .git.
			Quella è la cartella che conterrà gli oggetti git, ovvero oggetti composti dai nostri file + alcuni metadata di git.
			Possiamo ispezionare gli oggetti all'interno del db git ma sono comandi poco utili per un utilizzo del repo git.
			Il db git è organizzato come chiave-valore, ovvero ogni oggetto git ha un id, un identificativo univoco in tutto il db, che lo appunto identifica.

			Cerchiamo ora di capire logicamente come è organizzato il db, questo ci aiuterà poi soprattutto per comprendere il ruolo dei commit e il loro identificativo.
			[slide con oggetti e i loro id che sono l'hash calcolato, metodo chiave-valore quindi]
			Abbiamo detto che git prende delle "snapshot" dei file che contiene e le identifica con un id univoco.
			Infatti git immagazzina qualsiasi cosa nel suo database non con i nomi dei file, ma attraverso l'hash ottenuto dal contenuto stesso.
			Cosa significa?
			Un hash, calcolato con un apposito algoritmo, è una stringa composta da 40 caratteri esadecimali (da 0 a 9 e da A a F).
			Questa stringa, con la quale viene etichettata uno snapshot di git, è calcolata a partire dal contenuto stesso della snapshot, il che significa che se il contenuto
			viene in qualche modo modificato, allora anche l'hash sarà ricalcolato e sarà diverso.
			Nella foto d'esempio possiamo vedere come il "third commit" ha il proprio id.
			Questo meccanismo ci permette di avere un hash univoco ogni volta che viene calcolato a partire da un certo contenuto.
			Per questi motivi Git utilizza hash per salvare qualsiasi dato.
			Infatti la percetuale di collisione degli id, ossia che dopo aver calcolato l'hash di due oggetti, questi due id abbiano lo stesso valore è praticamente 0.

			[slide wolf]
			Alcuni esempi per capire quanto è bassa la possibilità di collisione con algoritmo SHA-1
			"una collisione data dall'algoritmo SHA-1 è meno probabile del fatto di avere ogni membro del tuo team di sviluppo attaccato e ucciso da dei lupi in incidenti
			distinti nella stessa serata"
			Da qui l'integrità assicurata in git.
			Nonostante lo sha-1 sia tra gli algoritmi usati in ambito sicurezza, per git la sicurezza è solo un side-effect per aver utilizzato lo sha-1 con un altro scopo.
			---
			Alternativa
			---
			Questo perchè ogni dato che si salva in un repo git passa attraverso una funzione di hashing (con algoritmo SHA-1) e il risultato della funzione è cio che
			viene poi usato come chiave.
			Quuesta chiave è una stringa alfanumerica esadecimale di 40 caratteri ed è usata come ID per gli oggetti nel repo git ed è univoca per quello specifico contenuto
			di dati.
			Qualsiasi tipo di data corruption verrebbe trovato immediatamente in quanto ci sarebbe un mismatch tra il contenuto dei file stessi e la stringa hash calcolata.
			---

			"The Three States"
			[foto working directory <> staging area <> repository]
			Attenzione ora, una delle caratteristiche che più impatta nella pratica il lavorare con git.
			Quando lavoriamo con git, i nostri preziosi file possono assumere 3 stati possibili:
			- Modificati
			- In stato "staged"
			- In stato "committed"
			Vediamo cosa significa
			- In stato "modificati": significa che abbiamo apportato delle modifiche ai file ma non abbiamo ancora salvato queste modifiche
			- In stato "staged": significa che, su un file precedentemente modificato, abbiamo detto a git di prepararlo per il prossimo salvataggio
							     che in termini di git significa che abbiamo preparato il file per essere inserito nel prossimo "commit" (per essere "committato")
			- In stato "committed": significa che i dati (cioè le ultime modifiche apportate a uno o piu' file) sono state salvate in modo sicuro sul database locale,
									cioè il repository

			Tramite questi tre stati possibili dei file possiamo quindi identificare tre principali "zone" di un progetto git
			- La working tree, ovvero la zona contenente i file del progetto (che per quanto detto prima sono cosi come sono salvati sul repository, quindi senza modifiche
						       di nessun tipo), sono proprio una copia dei file contenuti nel repository.
			- L'area di staging, chiamata anche "index", ovvero la zona che contiene i file modificati e pronti per essere inseriti in un commit
			- La directory Git, ovvero il repository in se, dove git salva i file attraverso le sue logiche e nei suoi "tipi di oggetto" (questioni di git di piu' basso
								livello). Questa è probabilmente la zona piu' importante ed è quella che ci prendiamo e copiamo quando "cloniamo" un repository.

			[sequenza di slide con il workflow con screen di git bash che esegue le azioni]
			Vediamo un esempio di quanto detto possiamo per identificare qual'è il workflow quando si lavora con git:
			1. Prendiamo dei file della working tree e li modifichiamo.
			2. Adesso abbiamo quindi una serie di file modificati.
			   Tra questi possiamo scegliere quali vogliamo mettere insieme "in un unica snapshot", ossia quali di questi vogliamo che siano contenuti in unico e stesso commit.
			   Questi sono i file che aggiungiamo alla staging area, detti quindi "staged".
			3. Facciamo un commit, quindi git per noi prenderà tutti(!!!) i file nella staging area (sono i file che noi abbiamo manualmente aggiunto alla staging area) e li
			   salva nel repository.
			   I file all'interno del repository git vengono detti "committed", "committati".

			"Repository hosting"
			[slide repository hosting]
			ne ho accennato uno prima, Github.
			In realtà Github ha diversi "concorrenti", come ad esempio phabricator che usavamo fino a poco tempo fa e aws codecommit che utilizziamo attualmente.
			Questi software sono servizi che mettono a disposizione l'hosting di repository git, ovvero sui loro server possiamo mettere dei repository git, pubblici o privati
			a nostro piacimento.
			Ognuno di loro si distingue in diversi modi, ad ogni modo in generale tutti questi servizi permettono di
				- avere un account con il quale fare login
				- definire policy di accesso ai propri login
				- eseguire varie azioni sui repository, come ad esempio code review
			In generale possiamo dire che sono sw per la gestione dei repo git.

			[slide tipi autenticazione]
			Per concludere questo discorso con qualche info in piu vediamo i tipi di autenticazione verso i servizi di hosting di repo git possibili.
				- username e password, autenticazione necessaria quando si utilizza il protocollo di comunicazione https
				- chiave pubblica e privata, quando si utilizza il protocollo di comunicazione ssh
					Questo è il tipo di autenticazione piu diffusa per i repo git, sia pubblici che privati, in quanto ritenuta
						* sia più sicura (richiede che la chiave privata sul pc che si sta utilizzando sia la corrispondente della chiave pubblica presente sul server)
						* sia piu veloce (sia per scambio dati che per il fatto che il file che deve essere presente sul pc viene automaticamente utilizzato dal protocollo e
						  quindi non è necessario ogni volta utilizzare username e password)
			Nel nostro caso, utilizzando un servizio di aws, codecommit, il protocollo che usiamo è https ma l'autenticazione avviene mediante l'aws cli che abbiamo configurata
			sul pc, quindi comunque non ci viene richiesta ogni volta username e password.

- Git basics

			"Initial setup"
			[no slide]
			Con il semplice workflow visto qualche slide fa abbiamo in realtà cominciato a vedere qualche comando git ed il suo funzionamento.
			Adesso finalmente entreremo più nel dettaglio, ma prima vediamo alcune delle configurazioni consigliate per lavorare con git, ovvero la configurazione del proprio
			username, email e editor preferito.
			Queste configurazioni è possibile settarle e modificarle sia da command line che accedendo direttamente al file .gitconfig, che si trova nella cartella del nostro
			utente, quindi C:\Users\nome.cognome

			[slide git che chiede di configurare username e email]
			Come possiamo vedere nella slide è git stesso a consigliarci di configurare username ed email, questo perchè queste due informazioni sono quelle che compariranno nel
			repository git per identificare un utente.

			[slide esempio di commit evidenziando lo username e email del commit]
			Come vedremo in seguito infatto username e email sono alcuni dei meta dati dei commit che riportano appunto informazioni riguardo l'utente che lo ha creato

			[slide configurazione editor di default]
			L'altra configurazione è importante in quanto altrimenti git utilizzerebbe come editor di default vim, un editor da riga di comando non troppo semplice per utenti
			neofiti della command line.

			"Create a project"
			[slide transizione con utente verso un repo nuovo e con utente verso repo che già esiste]
			Per iniziare a lavorare con git abbiamo bisogno di un repository.
			Le opzioni che abbiamo a disposizione dunque sono due
				1. Creare un nuovo repository e lavorare su quello
				2. Lavorare ad un repo già esistente.
				   Avendo già detto che git è un sistema VCS distribuito, lavorare ad un repo già esistente significa che quello che faremo sarà crearci sul nostro pc, in locale
				   quindi, una copia di un repository già esistente.

			Di conseguenza i due comandi sono
				1. git init, per creare un nuovo repository
				2. git clone, per appunto clonarci in locale un repo già esistente.


			[slide git init vs git clone, con il clone che è una concatenazioni di comandi tra cui git init]
			[https://stackoverflow.com/questions/16427600/how-git-clone-actually-works]
			Come vedremo anche più avanti con altri esempi, in git alcuni comandi eseguono in realtà una serie, una concatenazione di altri comandi git "sotto il cofano".
			In questo caso git init è un comando che potremmo definire "base", al contrario git clone invece è un comando concatenazione di altri comandi tra cui l'init.
			Come possiamo vedere dalla slide quindi il clone non farà altro che inizializzarci in locale un nuovo repository e "agganciarlo" al repository condiviso con i nostri
			colleghi.
			Capiremo in seguito cosa significa "agganciarlo", ad ogni modo il risultato è che in locale avremo la nostra copia del repo con annesse tutta una serie di informazioni
			tra cui la storia del repo stesso.


			"Check repo status"
			[slide screenshot bash con l'output di git status]
			Vediamo adesso un comando git tanto semplice quanto fondamentale, il comando "status".
			Come abbiamo detto più volte, lavorare con git significa lavorare su un repository git.
			Questo significa che in qualsiasi momento potremmo aver bisogno di sapere in che stato siamo, rispetto anche alle tre zone di lavoro viste in precedenza.

			[slide con gli screenshot dei git status della transazione delle tre zone precedente]
			Infatti è proprio il comando git status che nella transizione precedente ci dava info in merito alla working directory o alla staging area, come possiamo vedere
			dalle slide.

			[slide con output di un git diff]
			Altro comando utile per ispezionare le modifiche introdotte è il comando git diff.
			Lo rivedremo anche piu' avanti, con lo stesso scopo ma in una forma diversa.
			La sua forma piu' semplice invece, ovvero senza argomenti e solo come "git diff", ci mostra le differenze appunto tra la working three originale e quella attuale
			in seguito alle nostre modifiche.
			Abbiamo visto infatti come apportare le modifiche ad un file NON lo fa spostare dalla working three, ma utilizzando git status vedremo il file di color rosso;
			ecco, git diff ci mostra le modifiche sui "file rossi".

			[slide git diff file1 vs git diff (dove abbiamo modifiche a file1, file2 e file3)]
			Se vogliamo vedere le modifiche di un solo file, e non tutti, possiamo passarlo come argomento al comando diff.


			"Staging changes"
			[slide output git add + git status]
			Vediamo ora un altro comando visto nel workflow precedente, il git add.
			Questo comando ci permette di aggiungere un file modificato dal working three alla staging area, ovvero quella zona che permette di mettere da parte i file per
			un commit.

			[slide output git status con stesso file sia modificato in rosso, che presente nella staging e quindi verde]
			Particolarità della staging area è che è possibile aggiungerci la modifica ad un file, per poi modificare quello stesso file nuovamente.
			Cosi facendo la seconda modifica al file NON andrà automaticamente nella staging area.
			In questo modo è possibile elegere una modifica come "pronta per il commit", per poi continuare a lavorare su quello stesso file, come nell'esempio della slide.

			[slide transizioni di screenshot dell'esempio]
			Vediamo un esempio, dobbiamo modificare il file 1, allora lo modifichiamo e lo aggiungiamo alla staging.
			Per portare a termine l'intervento, ad esempio una fix, dobbiamo modificare anche il file 2, allora lo modifichiamo e lo aggiungiamo alla staging.
			Ci accorgiamo ora che manca un ulteriore modifica sul file 1.
			Allora facciamo anche quest'ulteriore modifica, siamo pronti?
			No, perchè in questo modo la nuova modifica è ancora nella working three e non nella staging.
			Allora aggiungiamola e siamo pronti.
			In realtà questo meccanismo non è una trappola, ma puo' anche tornarci utile se ad esempio la nuova modifica NON deve finire nella staging (e cioè spoiler: non deve finire
			nello stesso commit delle altre modifiche), possiamo quindi continuarci a lavorare mantenendo le nuove modifiche nella working three.

			"Committing changes"
			[slide output di git commit -m "Esempio di messaggio"]
			Vediamo finalmente come fare commit delle nostre modifiche.
			Questo comando in realtà ve l'ho già un po' spoilerato nelle spiegazioni precedente.
			git commit ci permette quindi di spostare TUTTE le modifiche presenti nella staging area, inserirle in un oggetto git detto appunto "commit" e aggiungerlo al repo.
			Mentre capiremo cosa significa "inserire il commit all'interno del repo" successivamente, vediamo cos'è un commit e la sintassi del comando.

			[slide screenshot di un commit estrapolato da git log]
			Un commit contiene diverse info, tra cui
				- Lista file modificati e in che modo
				- Autore del commit (notare username e email)
				- Messaggio del commit
			Tutte queste info sono importanti, ma l'unica che dobbiamo fornire noi al comando git commit, oltre alle modifiche ai file stessi ovviamente, è il messaggio.

			[slide git commit vs git commit -m "Esempio di messaggio"]
			Utilizzando il comando senza argomenti, git commit quindi, git ci aprirà automaticamente l'editor che abbiamo impostato come default e ci richiederà di inserire
			un messaggio.
			L'alternativa è passare il messaggio al comando commit da command line, ovvero come argomento, quindi git commit -m "MSG".

			[slide messaggio commit ben formato]
			Esistono alcune best practice per la scrittura dei messaggi dei commit, in modo da avere poi una storia dei commit il più informativa possibile.
			Alcune di queste sono:
				- Deve cominciare in modo da completare la frase "se questo commit viene introdotto...", quindi con un imperativo, ad esempio un buon inizio commit potrebbe
				  essere "Add new property"
				- Il messaggio deve iniziare con una riga singola e non deve avere più di 50 caratteri, descrivendo brevemente le modifiche che apporta.
				- Il corpo del messaggio conterrà dettagli in più rispetto alla riga iniziale.
			Tra queste, che sono già un subset di tutte le best practice, vi consiglio almeno la prima in quanto permetterà di avere la storia del repo costituita dai messaggi
			dei commit in modo piu' pulito possibile ed inoltre è la piu' semplice da utilizzare nel formato del comando con il messaggio come argomento, cioè git commit -m "msg".

			[slide output git show]
			Rimanendo in tema commit, vediamo come vedere dettagli in più di un commit, come mostrato in slide.
			Questo è l'output del comando show.
			Senza argomenti, come mostrato nello screenshot, mostra le informazioni dell'ultimo commit.

			[slide output git show SHA-DI-UN-COMMIT]
			Però è possibile passare al comando lo sha di un commit come argomento, in questo modo di mostrerà le info di quello specifico commit.
			Questo comando è molto utile quando si vuole capire cosa è stato fatto in uno specifico commit e si vogliono navigare le differenze apportate ai file.


			"Share Changes"
			[slide from local to remote!]
			Vediamo adesso come è possibile collaborare ad uno stesso progetto git con altre persone.
			Abbiamo fin'ora parlato del repository git, specificando diverse volte il fatto che il repo è "locale".
			Questo proprio perchè come detto all'inizio git è distribuito, ovvero ogni partecipante al progetto ha il proprio repository in locale.
			Ma avendo l'esigenza di condividere il repository con altre persone, quello che si fa è sincronizzare il proprio repository locale con un repository remoto.

			[slide repo sincronizzati tra utenti vs tra repo centrale]
			Per repository remoto si intende sia il repository di un'altra persona che un repository centrale, dal quale tutti si sincronizzano
			Ad esempio nella slide possiamo vedere come Alice può sincronizzare il proprio repository con David e viceversa, stessa cosa tra Davide e Clair,
			oppure come tutti loro possono sincronizzarsi tramite il repository remoto che nel gergo git viene chiamato repository "origin".
			Mentre il primo approccio è possibile, è comunque il meno adottato sopratutto in progetti grandi e con molte persone.
			E' quindi il secondo approcccio il piu' diffuso.
			Il repo centrale è quello che sarà ospitato da uno dei servizi di hosting visti in precedenza.

			[slide push, pull, fetch]
			Vediamo adesso in dettaglio i comandi per sincronizzarci con il repository "origin".

			[slide git push]
			- git push ci permette di sincronizzare il repository remoto con il nostro, il che significa portare i nostri nuovi commit sul repo remoto e quindi ci permette di
			  condividere le nuove modifiche ai file.

			[slide git fetch vs git pull]
			- git fetch e git pull permettono invece di sincronizzare il nostro repository con quello remoto, ma i due comandi funzionano in modo diverso
				- git fetch permette la sincronizzazione dal remoto al nostro repository, ma non ci porta quelle stesse modifiche all'interno della nostra working directory
			      come possiamo vedere dalle freccie della slide.

				  [slide esempio git fetch]
				  Infatti dopo aver fatto il fetch dal repository remoto, se verifichiamo lo stato del nostro repo con il comando status possiamo vedere come questo ci dice
				  che "siamo indietro di qualche commit" rispetto allo stato del repository origin e infatti non avremo quelle modifiche sui file.

				  [slide esempio git pull]
				- git pull invece non solo sincronizza i due repo, ma ci porta anche quelle modifiche nel working three e quindi avremo a disposizione quelle modifiche nei
				  file.
				  [slide git fetch vs git pull]
				  git pull è un altro esempio di concatenazione di comandi, infatti unisce "git init" con un altro comando che vedremo tra poco.

			"Play with branches"
			[slide immagine serie di commit]
			Adesso uniamo un pò i punti tra le caratteristiche di git di cui abbiamo parlato all'inizio e il concetto di commit in git che abbiamo visto poco fa.
			Abbiamo detto che git effettua il versionamento delle modifiche facendo uno snapshot dei nostri file e successivamente abbiamo capito che questi snapshot sono
			chiamati "commit" e contengono varie informazioni al proprio interno.
			Sotto il cofano, ogni commit contiene l'id (ovvero lo sha) del commit precedente, quindi una seguenza di commit può essere rappresentata come nella slide,
			da sx verso dx.
			Questa seguenza di commit formano un branch, che viene alimentato man mano si aggiungono altri commit.

			[slide branch come pointer]
			In realtà quella appena data è una spiegazione semplificata di cos'è un branch, che è vera per gli altri VCS e che possiamo prendere come riferimento anche in git.
			Ma per completezza cerco di farvi capire cos'è realmente un branch.
			Un branch in git non è altro che un pointer con un nome, ad esempio nella slide vediamo due branch, master e testing.
			La differenza tra i due branch è l'ultimo commit più a destra.
			Modificare un branch in git non significa altro che spostare quel pointer in avanti (ad esempio aggiungendo un nuovo commit), o indietro (ad esempio spostandoci su
			una snapshot più vecchia).

			[slide nuovo branch]
			Vediamo ora qualche comando per la manipolazione dei branch.
			Per creare un nuovo branch usiamo il comando "branch" appunto con argomento il nome che vogliamo dare al nuovo branch.
			Questo comando non ha output, per verificare che è stato creato possiamo usare sempre il comando "branch" ma con l'argomento "-a", che sta per "all" e che stampa
			tutti i branch che abbiamo attualmente nel nostro repository locale.
			Cosi facendo abbiamo creato un nuovo branch a partire dal branch corrente, che nell'esempio è "master" come si puo' vedere da git bash, cioè il branch che di default
			viene creato in git.
			Questo significa che i branch "master" e "test" puntano allo stesso commit.
			Aver creato il nuovo branch però non ci ha spostato su quel branch, siamo ancora sul branch master.

			[slide checkout]
			Il comando per spostarci da un branch all'altro è "checkout", con argomento il nome del branch sul quale vogliamo spostarci.
			In realtà al comando "checkout" possiamo anche fornire un altro parametro che ci permette di spostarci su un nuovo branch, cioè su un branch che non esiste.

			[slide checkout -b]
			In questo caso quindi checkout crea il nuovo branch e ci sposta su quel branch, come possiamo vedere dalla slide.

			[slide vuota merge]
			Andiamo ora a vedere una delle azioni che più caratterizzano l'utilizzo di branch e che spesso causano problemi ai primi utilizzi del comando stesso.

			[slide con gif del merge]
			Problemi come ad esempio questi in slide, per cui mi raccomando fatemi sapere se avete dubbi o domande!!

			[slide merge seria]
			Scherzi a parte, siamo nella situazione che vediamo nella slide.
			Per cui abbiamo il branch master che, a partire dal commit C2, ha subito l'introduzione di un ulteriore commit, il C4.
			Noi stavamo lavorando sul branch issue53, creato sempre a partire dal commit C2, e abbiamo introdotto due nuovi commit, il C3 e il C5.
			Il comando di merge è quello che ci permette di portare i nuovi commit di un branch sull'altro o viceversa, a seconda di quale sia il branch principale.
			Seguendo i nomi dell'esempio, supponiamo che ora dobbiamo portare i nuovi commit di issue53 sul branch master.

			[slide del merge tra master e issue53]
			Allora quello che possiamo fare è spostarci sul branch master e da li dare il comando "git merge issue53".
			Il comando prende come argomento i nomi dei branch che si vogliono mergiare.
			Nel caso gli si da in pasto soltanto un nome branch, git effettuerà il merge tra il branch attuale e quello specifico branch, come nell'esempio.
			Nota: notate l'ordinamento delle freccie, è sempre "all'indietro" perchè sappiamo che ogni commit contiene il riferimento al suo commit padre.
				  Nel caso di merge tra branch, il git creerà un nuovo commit per annotare l'avvenimento di un merge.
				  Questo nuovo commit, come vediamod alla slide, sarà "speciale" ed avrà due commit padre.

			[slide conflitto durante il merge]
			Il merge della slide precedente è un "happy path" del merge, ossia è una situazione ideale, in cui git per noi prende il contenuto dei file dei due branch e li
			unisce senza aver bisogno del nostro intervento.
			Che succede se git non riesce a capire in che modo unire una o più modifiche agli stessi file?
			Questa situazione si chiama situazione di "conflitto" e va risolta da noi in modo manuale.
			E' qualcosa che non deve scoraggiarvi in quanto è una situazione più che frequente quando si lavora in più persone ad un progetto.
			Il caso più frequente di conflitto si ha quando un file è stato modificato in modo differente tra branch su una stessa riga, quindi git non può a prescindere scegliere
			quale delle due modifiche mantenere e quale scartare.
			Vediamo un esempio

			[slide esempio di conflitto durante il merge]
			[slide 1]
			Iniziamo con il creare un nuovo branch a partire da master, il branch fix-that-bug.
			In questo momento i due branch sono uguali.

			[slide 2]
			Adesso su master vogliamo creare un commit, introducendo una modifica al file file-3.
			Quindi aggiungiamo e committiamo questa modifica.

			[slide 3]
			Adesso spostiamoci sul branch fix-that-bug, modifichiamo il file-3 anche su questo branch e committiamo la modifica.

			[slide differenza dei branch master e fix-that-bug]
			La situazione in cui ci troviamo adesso è che i due branch, master e fix-that-bug, sono divergenti tra di loro per un commit entrambi.
			Prima di procedere al tentativo di merge però voglio riproporvi un comando che abbiamo già visto ma nel contesto dei branch, ossia il comando git.

			[slide diff tra branch]
			Il comando diff infatti può prendere come argomento anche due branch o due commit.
			Il suo output sarà la differenza appunto tra i due branch o i due commit.
			Vediamo nel nostro esempio nella slide il diff tra i due branch master e fix-that-bug.
			La sintassi, proprio come per il comando merge, non richiede esplicitamente due branch o commit per mostrarne la differenza.
			Infatti se diamo come argomento un solo branch, come nella slide, il comando diff ci darà la differenza tra il branch corrente e quello passato come argomento.
			Quindi vediamo nel primo screenshot la differenza tra master, ovvero il branch corrente, e fix-that-bug.
			Nel secondo screenshot vediamo la differenza tra fix-that-bug e master, proprio perchè in questo caso siamo con il branch attuale su fix-that-bug.
			Notare come la differenza tra i branch in un verso o l'altro è ovviamente la stessa, ma risulta invertita la modifica introdotta, la parte "in verde",
			ossia la modifica in aggiunta al file è sempre quella del branch corrente.

			[slide git merge tra master e fix-that-bug con output di conflitto]
			Adesso procediamo con il merge.
			Ci mettiamo sul branch master e vogliamo mergiare qui il branch fix-that-bug.
			L'output del merge tra i due branch è nella slide.
			Possiamo vedere come git prova a fare un auto-merge di file-3, per poi segnalarci un "merge conflict" su quello stesso file, dicendoci di aver fallito l'auto-merge
			e che dobbiamo risolvere il conflitto e commitare il risultato.
			Come possiamo vedere dall'intestazione della cli, abbiamo l'informazione che siamo in stato "MERGING", ovvero siamo nel bel mezzo della fase di merge.

			[slide merge --abort]
			Nel caso non sappiamo come risolvere il conflitto oppure ci proviamo ma non abbiamo successo possiamo sempre uscire da questo stato con "git merge --abort",
			questo grazie al fatto di aver lavorato sul nostro repository che è locale, quindi non abbiamo apportato nessuna modifica al repository condiviso.

			[slide status in merging]
			Vediamo invece come procedere alla risoluzione del conflitto.
			Nella slide c'è l'output del comando status durante lo stato di merging, che ci da informazioni su come procedere, se abortire il merge come visto poco fa oppure
			di risolvere il conflitto e commitare per proseguire.
			Ci dice inoltre quali sono i file in conflitto, in questo caso uno solo.
			Abbiamo modo di vedere dove abbiamo conflitto?
			git status ci dice che il file file-3 è in conflitto in quanto è stato modificato da entrambi i branch

			[git diff in stato di merging]
			Ma se questo file è in stato "modificato" possiamo vederne il diff!
			Se ad una prima occhiata ci potrebbe sembrare confuso il contenuto del file, in realtà git ci indica quale parte del file è in conflitto e soprattuto ci dice
			quale parte appartiene a quale branch.
			Nel nostro esempio abbiamo una prima parte del file delimitata da <<<HEAD e ====.
			Questa modifica è stata introdotta dal branch corrente, quindi master nell'esempio, identificato come HEAD.
			Infatti HEAD è una label particolare che identifica sempre l'ultimo commit del branch nel quale siamo.
			Abbiamo poi la modifica che va dagli === a >>> fix-that-bug che è stata introdotta dal branch indicato, in questo caso fix-that-bug appunto.
			Questa identificazione del conflitto fornita da git è in genere rappresentata graficamente dagli IDE e editor di testo piu' comuni.

			[slide vs code diff]
			Ad esempio Guidewire Studio, Eclipse o, come nell'esempio in slide, VS Code.
			E' sicuramente più facile risolvere i conflitti all'interno dell'editor o dell'IDE che si utilizza per il proprio progetto anche per avere la sintassi del linguaggio
			riconosciuta.

			[slide risoluzione conflitto]
			Nel nostro semplice esempio risolviamo il conflitto innanzitutto rimuovendo i delimitatori del conflitto introdotti da git e poi modificando il contenuto del file
			come riteniamo piu' opportuno.
			Nella slide un esempio del diff sul file appena mergiato.
			Dobbiamo ora commitare il file.
			Come detto prima, il comando merge creerebbe per noi in caso vada a buon fine senza conflitti un commit che identifica l'evento di merge.
			Nel nostro esempio abbiamo avuto conflitto, ma git ci fornisce comunque il messaggio di merge che avrebbe utilizzato, in modo da rendere noto
			che c'è stato un merge.

			[slide commit post merge]
			Quindi lancio git add del file modificato e poi git commit, senza dargli un messaggio come argomento.
			Git allora mi apre l'editor di default, vim in questo caso, e possiamo vedere dalla slide che ho già il commit popolato all'interno dell'editor.
			Le righe che iniziano con cancelletto sono in realtà dei commenti che non compariranno nel commit, ma sono a nostro supporto per adesso che stiamo
			scrivendo il messaggio del commit.
			Salviamo questo contenuto in modo da finalizzare il commit.

			[slide post commit del merge]
			In questo modo usciamo dalla fase di "merging", ci troviamo finalmente nella seguente situazione

			[slide post merge di master e fix-that-bug]
			Ovvero abbiamo eseguito il merge del branch fix-that-bug sul branch master, il che ha introdotto un nuovo commit che identifica l'evento del merge e contiene
			la modifica apportata al file file-3 che era il file che causava il conflitto durante il merge.

			[slide git show del commit di merge]
			Se vogliamo verificare il contenuto di questo commit di merge lanciamo, dal branch master che ha ospitato il merge, il comando git show.
			Rispetto all'output dello show di un commit normale, lo show di un commit di merge riporta un'informazione in più, cioè la riga subito sotto lo sha del commit
			che riporta l'informazione dei due commit padre di questo merge commit.


