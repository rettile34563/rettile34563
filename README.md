<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>Guida ai Codici</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f3f3f3;
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      background-color: #333;
      color: #fff;
      padding: 20px 0;
      text-align: center;
      width: 100%;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    h1 {
      margin: 0;
      font-size: 48px;
      letter-spacing: 2px;
    }

    nav ul {
      list-style: none;
      padding: 0;
      display: flex;
      justify-content: center;
    }

    nav ul li {
      margin-right: 20px;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-size: 20px;
      transition: color 0.3s ease;
    }

    nav ul li a:hover {
      color: #ff6600;
    }

    main {
      max-width: 800px;
      margin: 20px;
      padding: 20px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    section {
      margin-bottom: 40px;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      display: none;
    }

    h2 {
      border-bottom: 2px solid #333;
      padding-bottom: 10px;
      margin-bottom: 20px;
      font-size: 28px;
      color: #333;
    }

    p {
      line-height: 1.6;
      font-size: 18px;
    }

    .show {
      display: block;
      animation: fadeIn 0.5s ease-in-out;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(-20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Esplora i Codici</h1>
    <nav>
      <ul>
        <li><a href="#qr" class="code-link">QR Code</a></li>
        <li><a href="#isbn" class="code-link">Codice ISBN</a></li>
        <li><a href="#iban" class="code-link">Codice IBAN</a></li>
        <li><a href="#fiscale" class="code-link">Codice Fiscale</a></li>
        <li><a href="#barcode" class="code-link">Codice a Barre</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <section id="qr" class="show">
      <h2>QR Code</h2>
      <p>Il QR Code (Quick Response Code) è un tipo di codice a barre bidimensionale che può contenere diverse informazioni, come link a siti web, testo, numeri di telefono, ecc.</p>
      <p>Viene comunemente utilizzato per l'accesso rapido a informazioni tramite smartphone.</p>
      <p>È presente in pubblicità, biglietti da visita, ecc.</p>
      <p>Per decodificarlo, è necessaria un'applicazione dedicata che legge e interpreta le informazioni contenute nel codice.</p>
    </section>
    
    <section id="isbn">
      <h2>Codice ISBN</h2>
      <p>Il Codice ISBN (International Standard Book Number) è un identificatore univoco per i libri.</p>
      <p>È utilizzato per catalogare e identificare un libro in modo univoco, includendo informazioni come l'editore, l'edizione e il formato.</p>
      <p>Un ISBN è spesso stampato sul retro di un libro sopra il codice a barre.</p>
    </section>
    
    <section id="iban">
      <h2>Codice IBAN</h2>
      <p>Il Codice IBAN (International Bank Account Number) è un codice bancario internazionale utilizzato per identificare univocamente un conto bancario.</p>
      <p>È composto da una serie di caratteri alfanumerici che variano in lunghezza a seconda del paese e dell'istituto bancario.</p>
      <p>Il Codice IBAN è fondamentale per le transazioni bancarie internazionali.</p>
    </section>

    <section id="fiscale">
      <h2>Codice Fiscale</h2>
      <p>Il Codice Fiscale è un identificativo fiscale utilizzato in Italia per identificare in modo univoco le persone fisiche.</p>
      <p>È composto da una combinazione di lettere e numeri derivati da nome, cognome, data e luogo di nascita.</p>
      <p>Viene utilizzato in una vasta gamma di procedure amministrative e fiscali.</p>
    </section>

    <section id="barcode">
      <h2>Codice a Barre</h2>
      <p>Il Codice a Barre (EAN-13) è un sistema di codifica a barre numeriche utilizzato per identificare in modo univoco i prodotti in tutto il mondo.</p>
      <p>È ampiamente utilizzato nel settore commerciale e al dettaglio per gestire l'inventario e le vendite.</p>
      <p>L'EAN-13 è composto da 13 cifre numeriche e può essere letto da lettori di codici a barre per ottenere informazioni sul prodotto.</p>
    </section>
  </main>

  <script>
    const codeLinks = document.querySelectorAll('.code-link');
    const codeSections = document.querySelectorAll('section');

    codeLinks.forEach(link => {
      link.addEventListener('click', (e) => {
        e.preventDefault();
        const targetSectionId = link.getAttribute('href').substring(1);

        codeSections.forEach(section => {
          section.classList.remove('show');
        });

        document.getElementById(targetSectionId).classList.add('show');
      });
    });
  </script>
</body>
</html>
