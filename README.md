
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hotel Etoile - Mar del Plata</title>
  <style>
    /* ===== RESET ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Arial', sans-serif;
    }

    body {
      background-color: #f7f7f7;
      color: #333;
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* ===== HEADER ===== */
    header {
      background-color: #1a1a1a;
      color: #fff;
      padding: 20px;
      text-align: center;
    }

    header h1 {
      font-size: 2em;
      margin-bottom: 5px;
    }

    header p {
      font-size: 1em;
    }

    /* ===== NAV / BOTONES ===== */
    .contact-buttons {
      display: flex;
      justify-content: center;
      margin: 15px 0;
      gap: 10px;
      flex-wrap: wrap;
    }

    .contact-buttons a {
      background-color: #ff6b6b;
      color: white;
      padding: 10px 20px;
      border-radius: 8px;
      transition: background-color 0.3s;
    }

    .contact-buttons a:hover {
      background-color: #ff4c4c;
    }

    /* ===== SECCIONES ===== */
    section {
      max-width: 1200px;
      margin: 30px auto;
      padding: 20px;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.1);
    }

    section h2 {
      margin-bottom: 15px;
      color: #1a1a1a;
    }

    /* Servicios */
    .services {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }

    .service {
      flex: 1 1 200px;
      background-color: #f0f0f0;
      padding: 20px;
      border-radius: 10px;
      text-align: center;
    }

    .service img {
      width: 50px;
      margin-bottom: 10px;
    }

    /* ===== SOBRE NOSOTROS ===== */
    .about p {
      text-align: center;
    }

    /* ===== FOOTER ===== */
    footer {
      background-color: #1a1a1a;
      color: #fff;
      padding: 20px;
      text-align: center;
      margin-top: 30px;
    }

    footer p {
      margin: 5px 0;
    }

    /* ===== CHAT ===== */
    .chat-container {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 300px;
      max-height: 400px;
      display: flex;
      flex-direction: column;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      overflow: hidden;
      font-size: 14px;
      z-index: 1000;
    }

    .chat-header {
      background-color: #ff6b6b;
      color: #fff;
      padding: 10px;
      text-align: center;
      cursor: pointer;
    }

    .chat-messages {
      flex: 1;
      padding: 10px;
      overflow-y: auto;
    }

    .chat-messages div {
      margin-bottom: 10px;
    }

    .chat-messages .user {
      text-align: right;
    }

    .chat-input {
      display: flex;
      border-top: 1px solid #ccc;
    }

    .chat-input input {
      flex: 1;
      padding: 10px;
      border: none;
      outline: none;
    }

    .chat-input button {
      padding: 10px;
      background-color: #ff6b6b;
      color: #fff;
      border: none;
      cursor: pointer;
    }

    .chat-input button:hover {
      background-color: #ff4c4c;
    }

    @media(max-width: 768px){
      .services {
        flex-direction: column;
      }
      .chat-container {
        width: 90%;
        right: 5%;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Hotel Etoile</h1>
    <p>Mar del Plata - Centro | Santiago del Estero 1869 | Tel: 0223 493-4968</p>
    <div class="contact-buttons">
      <a href="tel:+542234934968">Llamar</a>
      <a href="mailto:info@hoteletoile.com">Enviar Email</a>
      <a href="https://wa.me/542236055208" target="_blank">WhatsApp</a>
    </div>
  </header>

  <section class="services">
    <h2>Servicios</h2>
    <div class="services">
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/wifi.png" alt="WiFi">
        <p>WiFi Gratis</p>
      </div>
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/bed.png" alt="Habitaciones">
        <p>Habitaciones Estándar y Premium</p>
      </div>
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/restaurant.png" alt="Desayuno">
        <p>Desayuno Incluido</p>
      </div>
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/cleaning-tools.png" alt="Limpieza">
        <p>Limpieza Diaria</p>
      </div>
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/car.png" alt="Parking">
        <p>Parking</p>
      </div>
      <div class="service">
        <img src="https://img.icons8.com/ios-filled/50/000000/reception-bell.png" alt="Recepción">
        <p>Recepción 24/7</p>
      </div>
    </div>
  </section>

  <section class="about">
    <h2>Sobre Nosotros</h2>
    <p>En Hotel Etoile, nos esforzamos por ofrecer una estadía confortable y agradable. Nuestro personal amable está disponible para atender todas sus consultas, garantizando una experiencia memorable en Mar del Plata.</p>
  </section>

  <footer>
    <p>Hotel Etoile - Santiago del Estero 1869, Mar del Plata</p>
    <p>Tel: 0223 493-4968 | Email: info@hoteletoile.com</p>
  </footer>

  <!-- CHAT -->
  <div class="chat-container" id="chatContainer">
    <div class="chat-header" id="chatHeader">Chat con el Hotel</div>
    <div class="chat-messages" id="chatMessages"></div>
    <div class="chat-input">
      <input type="text" id="chatInput" placeholder="Escribe tu mensaje...">
      <button id="sendBtn">Enviar</button>
    </div>
  </div>

  <script>
    // ===== CHAT FUNCTIONALITY =====
    const chatContainer = document.getElementById('chatContainer');
    const chatHeader = document.getElementById('chatHeader');
    const chatMessages = document.getElementById('chatMessages');
    const chatInput = document.getElementById('chatInput');
    const sendBtn = document.getElementById('sendBtn');

    let chatOpen = true;

    // Toggle chat
    chatHeader.addEventListener('click', () => {
      chatOpen = !chatOpen;
      chatMessages.style.display = chatOpen ? 'block' : 'none';
      chatInput.parentElement.style.display = chatOpen ? 'flex' : 'none';
    });

    // Predefined responses
    const responses = [
      { keywords: ['horario','abre','cierra'], answer: 'Nuestro hotel tiene recepción 24/7 y puede acceder a su habitación en cualquier momento.' },
      { keywords: ['reserva','reservar'], answer: 'Puede realizar su reserva llamando al 0223 493-4968 o enviando un email a info@hoteletoile.com.' },
      { keywords: ['wifi','internet'], answer: 'Contamos con WiFi gratuito en todas las habitaciones y áreas comunes.' },
      { keywords: ['desayuno'], answer: 'El desayuno está incluido para todos nuestros huéspedes y se sirve diariamente en el comedor.' },
      { keywords: ['parking'], answer: 'Disponemos de parking para nuestros huéspedes sin cargo adicional.' },
      { keywords: ['habitaciones','tipos'], answer: 'Ofrecemos habitaciones estándar y premium, todas equipadas para su comodidad.' },
      { keywords: ['ubicación','dónde'], answer: 'Nos encontramos en Santiago del Estero 1869, Centro, Mar del Plata.' },
      { keywords: ['contacto','teléfono','email'], answer: 'Puede contactarnos al 0223 493-4968 o info@hoteletoile.com.' },
      { keywords: ['limpieza'], answer: 'La limpieza de habitaciones se realiza diariamente para su confort.' }
    ];

    function getResponse(message){
      message = message.toLowerCase();
      for(let i=0;i<responses.length;i++){
        for(let j=0;j<responses[i].keywords.length;j++){
          if(message.includes(responses[i].keywords[j])){
            return responses[i].answer;
          }
        }
      }
      return 'Lo sentimos, no entendí tu consulta. Por favor contacte directamente al hotel al 0223 493-4968.';
    }

    function appendMessage(user, text){
      const msgDiv = document.createElement('div');
      msgDiv.className = user ? 'user' : 'hotel';
      msgDiv.textContent = text;
      chatMessages.appendChild(msgDiv);
      chatMessages.scrollTop = chatMessages.scrollHeight;
    }

    sendBtn.addEventListener('click', () => {
      const message = chatInput.value.trim();
      if(message === '') return;
      appendMessage(true, message);
      const reply = getResponse(message);
      setTimeout(()=> appendMessage(false, reply), 500);
      chatInput.value = '';
    });

    chatInput.addEventListener('keypress', (e) => {
      if(e.key === 'Enter'){
        sendBtn.click();
      }
    });
  </script>

</body>
</html>
