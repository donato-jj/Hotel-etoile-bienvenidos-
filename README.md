
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Asistente Virtual</title>

<style>
/* ================= RESET ================= */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* ================= BASE ================= */
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f4f4f4;
    color: #222;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

/* ================= CONTENEDOR ================= */
.chat-container {
    width: 100%;
    max-width: 420px;
    background: #ffffff;
    border: 1px solid #ddd;
    display: flex;
    flex-direction: column;
    height: 90vh;
}

/* ================= HEADER ================= */
.chat-header {
    background: #111;
    color: #fff;
    padding: 16px;
    text-align: center;
    font-size: 16px;
    font-weight: bold;
}

/* ================= MENSAJES ================= */
.chat-messages {
    flex: 1;
    padding: 15px;
    overflow-y: auto;
}

/* ================= BURBUJAS ================= */
.message {
    margin-bottom: 12px;
    line-height: 1.4;
    font-size: 14px;
}

.user {
    text-align: right;
    color: #000;
}

.bot {
    text-align: left;
    color: #444;
}

/* ================= INPUT ================= */
.chat-input {
    display: flex;
    border-top: 1px solid #ddd;
}

.chat-input input {
    flex: 1;
    padding: 12px;
    border: none;
    font-size: 14px;
}

.chat-input button {
    padding: 12px 18px;
    border: none;
    background: #111;
    color: #fff;
    cursor: pointer;
}

.chat-input button:hover {
    background: #333;
}

/* ================= RESPONSIVE ================= */
@media (max-width: 480px) {
    .chat-container {
        height: 100vh;
        border: none;
    }
}
</style>
</head>

<body>

<div class="chat-container">
    <div class="chat-header">
        Asistente Virtual
    </div>

    <div class="chat-messages" id="chat">
        <div class="message bot">
            Hola, soy el asistente virtual. Estoy disponible para ayudarte con información, servicios y consultas generales.
        </div>
    </div>

    <div class="chat-input">
        <input type="text" id="userInput" placeholder="Escribí tu consulta..." />
        <button onclick="sendMessage()">Enviar</button>
    </div>
</div>

<script>
/* ================= IA CONVERSACIONAL ================= */

function sendMessage() {
    const input = document.getElementById("userInput");
    const text = input.value.trim();
    if (text === "") return;

    addMessage(text, "user");
    input.value = "";

    setTimeout(() => {
        const response = getResponse(text);
        addMessage(response, "bot");
    }, 500);
}

function addMessage(text, sender) {
    const chat = document.getElementById("chat");
    const message = document.createElement("div");
    message.className = "message " + sender;
    message.textContent = text;
    chat.appendChild(message);
    chat.scrollTop = chat.scrollHeight;
}

function getResponse(message) {
    const msg = message.toLowerCase();

    if (msg.includes("horario")) {
        return "Nuestro horario de atención es de lunes a viernes de 9:00 a 18:00.";
    }

    if (msg.includes("contacto") || msg.includes("telefono")) {
        return "Podés contactarnos a través del formulario del sitio o por nuestros medios oficiales de atención.";
    }

    if (msg.includes("servicios")) {
        return "Ofrecemos atención personalizada, información clara y soporte continuo para nuestros usuarios.";
    }

    if (msg.includes("ubicación") || msg.includes("direccion")) {
        return "Nuestra información de ubicación está disponible en la sección de contacto del sitio.";
    }

    if (msg.includes("politica") || msg.includes("condiciones")) {
        return "Trabajamos con políticas claras, orientadas a la transparencia y el buen servicio al usuario.";
    }

    if (msg.includes("ayuda")) {
        return "Estoy acá para ayudarte. Podés consultarme sobre servicios, horarios, contacto o uso del sitio.";
    }

    return "No logré entender tu consulta con claridad. ¿Podrías reformularla o indicar qué información necesitás?";
}
</script>

</body>
</html>
