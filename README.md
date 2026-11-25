AlHammami · Portfolio Grafico & Assistenza IT Level 1

Sito web statico multilingua (FR / IT / EN / AR) che unisce tre collezioni di progetti grafici (AlHammami, Don Viruss, Sofisticata Ignoranza) a un modulo di prenotazione per lavori grafici su misura e supporto tecnico IT Level 1, con generazione automatica del codice ordine (AH-...) e pagamento tramite Flouci.

Struttura del repository

/
├── index.html        # Pagina principale completa (HTML, CSS e JavaScript)
├── img/              # Cartella per le opere delle gallerie e l'eventuale logo Flouci
└── README.md         # Documentazione del repository


Nota per GitHub Pages: rinomina il file HTML principale in index.html affinché venga caricato automaticamente come home page del sito.

Come aggiungere immagini nelle gallerie

Carica i file immagine (.jpg, .png, .webp) nella cartella img/ del repository.

Apri index.html e individua la costante GALLERY nella sezione <script>:

const GALLERY = {
  donh: [
    { src: 'img/alhammami-01.jpg', title: 'Identità Visiva' }
  ],
  donviruss: [
    { src: 'img/donviruss-01.jpg', title: 'Illustrazione Libera' }
  ],
  sof: [
    { src: 'img/sof-01.jpg', title: 'Campagna Comunicazione' }
  ]
};


Salva ed esegui il commit delle modifiche: le immagini appariranno automaticamente nelle rispettive collezioni scorrevoli.

Configurazione ordini e pagamento Flouci

Nella costante CFG all'interno di index.html puoi impostare i tuoi riferimenti:

const CFG = {
  ownerEmail: 'graphicamed.hammami@gmail.com',
  flouciLink: 'https://...',   // Link diretto di pagamento Flouci (opzionale)
  flouciPhone: '+216 ...',     // Numero/ID Flouci mostrato se flouciLink è vuoto
  flouciLogo: 'img/flouci.png',
  emailjs: {
    publicKey: '',
    serviceId: '',
    templateId: ''
  }
};


Invio email: se i campi emailjs restano vuoti, il modulo genera comunque il codice ordine e apre l'applicazione email del cliente (mailto:) già precompilata.

Pagamento Flouci: se flouciLink è compilato, il pulsante apre direttamente il link di pagamento; in alternativa mostra il contatto inserito in flouciPhone insieme al codice ordine.

Pubblicazione su GitHub Pages

Vai su Settings → Pages nel repository GitHub.

Alla voce Branch, seleziona main e la cartella /(root), quindi clicca su Save.

Attendi 1–2 minuti per l'attivazione del link pubblico.
