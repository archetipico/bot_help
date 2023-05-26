L'accesso è consentito solo agli utenti verificati dal sottoscritto.

# Comandi
N.B.

Il cancelletto `#` serve solo per evidenziare il comando qui nella lista dei comandi, nella realtà, se per esempio si vuole eseguire un comando, come quello per richiedere l'oroscopo, basta digitare `horo scorpio` senza digitare `#`. Il segno `>` indica invece un esempio di utilizzo del comando.
```markdown
# /help
Aiuto
> /help                     # ricorda che è l'unico comando con lo slash

# 8ball[ <testo>]
Agita una Magic 8 Ball in risposta ad un testo o scrivendo una domanda successivamente
> 8ball
> 8ball Domani sarà una bella giornata?
> 8ball Dovrei mettermi a dieta?

# canny[ <min> <max>]
Usato in risposta ad una foto, trova i contorni e li restituisce: il famoso Canny Edge Detector
> canny                     # di default impostato a (50, 150)
> canny 60, 120
> canny 10, 100

# color <hex>
Converte il codice del colore nel nome reale del colore (non serve inserire # prima del colore)
> color 00ff44              # lo detesto come colore ma ha un bell'hex
> color 696969

# cptf <up>, <down>
(CaPTion Fast) Crea caption su immagini (PNG o JPEG) e su GIF (velocizzandole)
> cptf top, bottom          # il classico
> cptf top text,
> cptf , bottom text
> cptf ,                    # velocizza e basta
> cptf                      # come sopra

# edge[ <min> <max>]
Usato in risposta ad una foto, trova i contorni e li restituisce come sovrimposizione dell'immagine (è sempre il Canny Edge Detector ma con un alpha imposto)
> edge                      # di default impostato a (50 150)
> edge 60 120
> edge 10 100

# face
Trova volti e occhi all'interno di una foto (algoritmo MOLTO approssimativo)
> face                      # se siete fortunati trova una faccia ogni dieci

# horo [ye|to|tm|we|mo ]<segno>
Restituisce l'oroscopo dato il segno zodiacale
** N.B. [ye|to|tm|we|mo ] non sono intercalari, sono abbreviazioni di "yesterday", "today", "tomorrow", "weekly" e "monthly" **
> horo scorpio
> horo ye libra             # nel caso tu non sia convinto dell'effetto Barnum
> horo mo gemini

# info
Informazioni
> info                      # non c'è molto da dire

# malus[ show|<user>]|[ add|rm <malus>]
Applica un evento casuale a te stesso o ad un utente rispondendo ad un suo messaggio con malus o taggandolo
> malus
> malus add perde tutti gli amici perché programma troppo
> malus rm malus vecchio che non mi serve più
> malus show
> malus @tizio
> malus Tizio Caio

# manuser add|rm
Rispondi ad un messaggio di un utente per aggiungerlo o rimuoverlo dalla lista degli utenti concessi
** N.B. Solo io posso usarli ma è giusto aggiungere il comando alla documentazione **
> manuser add               # avete il mio rispetto
> manuser rm                # perdete il mio rispetto

# oled[ <white>]
Usalo in risposta ad una foto per mostrarla sullo schermo OLED collegato al mio RaspberryPi! La soglia `white` definisce quando un pixel deve essere considerato bianco, utile per quando si vogliono evidenziare o ignorare dettagli
> oled                      # di default impostato a 127
> oled 90
> oled 3280                 # viene applicato il modulo 256

# palette[ <n>]
Usalo in risposta ad una foto per ricevere la palette dei colori usati in essa: specifica n per il numero di colori [1-10]
> palette                   # di default impostato a 5
> palette 3                 # per i fissati con l'armocromia
> palette 40                # default

# pixel[ <val>]
Pixelizza un'immagine, possibilmente usando un valore <val> di riferimento [1-99]
> pixel                     # di default impostato a 50
> pixel 5                   # gioco in 8-bit
> pixel 60                  # quelle foto in JPEG inoltrate 100 volte nelle chat
> pixel 150                 # viene applicato il modulo 100

# regex <regex>, <testo>
Applica una sostituzione del testo data una regex
> regex [a-zA-Z].+, xyzzy

# relief[ <n> <k>]
Mostra rilievo di una foto: il famoso filtro gaussiano
> relief                    # di default impostato a (30 2)
> relief 15 4
> relief 10 2

# reverse[ list]
Inverte video e audio di GIF, MOV, MP3, MP4, OGG e WEBM (che su Telegram spesso sono gli sticker animati)
** N.B. Nel mio caso il bot gira su un Raspberry: se vedete che l'output non si apre o pesa pochissimo, significa che il comando richiede troppa RAM **
> reverse list                # l'elenco di tutti i formati supportati
> reverse

# roll[ <n>]
Lancia un dado ad n facce: il comando senza valore <n> esegue un lancio di un dado a 6 facce
> roll                      # di default impostato a 6
> roll 6                    # beh...
> roll 20                   # DnD gamers rise up
> roll 30                   # a quanto pare esistono
> roll -1                   # a tuo rischio e pericolo: verrai deriso

# scale[ <val>]
Scala un'immagine usando la tecnica del Liquid Rescaling usando un valore <val> di riferimento [1-99]
> scale                     # di default impostato a 50
> scale 10                  # smarmellamento
> scale 90                  # deformazione
> scale 1                   # radiazione cosmica di fondo

# solve <calcolo>
Risolvi qualsiasi cosa passando un <comando>
> solve 1 + 1
> solve 6 feet to m
> solve problemi vita       # purtroppo i nostri problemi dobbiamo risolverceli da soli

# stats
Mostra l'utilizzo dei comandi
** N.B. "Fallito" non si riferisce a chi usa il comando **
> stats

# strip[ list]
Rimuove metadati e prova a ridurre la dimensione di determinati file
> strip list                # l'elenco di tutti i formati supportati
> strip                     # nessun doppio senso

# tts[ <lingua>[ <testo>]]|[ lang]
Legge il <testo> nella lingua selezionata (nel caso di risposta ad un messaggio, <testo> è il messaggio a cui si risponde)
> tts lang                  # l'elenco delle lingue supportate
> tts                       # di default impostato in inglese
> tts it Ciao gente         # Ciao anche a te!

# urban <ricerca>
Ricerca sull'Urban Dictionary
** N.B. Il risultato è in inglese **
> urban most deranged thing ever

# wttr <luogo>
Dato un luogo restituisce il meteo, dati sull'inquinamento e sui pollini: sono concessi municipi, zone, vie,...
> wttr Roma                 # questa è facile
> wttr posto sconosciuto    # 99.9% delle volte te lo trova o lo inventa
> wttr CASA DI CHI LEGGE    # STACCA STACCA

# xkcd
Invia una vignetta casuale da xkcd.com
** N.B. Il risultato è in inglese **
> xkcd                      # probabilmente invierà qualcosa di triste

Infine il bot cerca di pulire gli URL che considera sporchi.