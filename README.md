# mi-pagina-web
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Nexus Game Store - Jean Pierre Honores</title>
        <link rel="stylesheet" href="style.css">
        <style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');
*{
    margin: 0%;
    padding: 0%;
    box-sizing: border-box;
    text-decoration: none;
    list-style: none;
}

body {
    font-family: 'Poppins', sans-serif;
    background-color: #1b1721;
    color: #e0e0e0;
}

img {
    max-width: 100%;                        
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.header {
    background-image: linear-gradient(rgba(27, 23, 33, 0.7), rgba(27, 23, 33, 0.7)), url(images/menugamer.jpeg);
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    min-height: 80vh;
    padding: 80px 0;
}

.menu {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
    background-color: rgba(27, 23, 33, 0.95);
    border-bottom: 2px solid #80EDFF;
    z-index: 1000;
    backdrop-filter: blur(10px);
    height: 70px;
}

.logo {
    color: #00FBFF;
    font-size: 25px;
    font-weight: 800;
    text-transform: uppercase;
    text-decoration: none;
    z-index: 1000;
    letter-spacing: 1px;
    transition: all 0.3s ease;
}

.logo:hover {
    color: #80EDFF;
    text-shadow: 0 0 10px rgba(128, 237, 255, 0.5);
}

.menu .navbar ul li {
    position: relative;
    float: left;
}

.menu .navbar ul li a {
    font-size: 16px;
    padding: 20px;
    color: #FFFFFF;
    font-weight: 600;
    display: block;
    transition: color 0.3s ease, background-color 0.3s ease;
    text-decoration: none;
}

.menu .navbar ul li a:hover {
    color: #80EDFF;
    background-color: rgba(128, 237, 255, 0.1);
}

#menu {
    display: none;
}

.menu-icono {
    width: 25px;
    cursor: pointer;
}

.menu label {
    cursor: pointer;
    display: none;
}

.header-content {
    display: flex;
    align-items: center;
    width: 100%;
    margin-top: 80px;
}

.header-txt {
    flex-basis: 50%;
    animation: fadeInLeft 0.8s ease;
}

.header-txt h1 {
    font-size: 60px;
    color: #FFFFFF;
    line-height: 1.3;
    margin-bottom: 25px;
    font-weight: 800;
}

.header-txt span {
    color: #80EDFF;
    text-shadow: 0 0 20px rgba(128, 237, 255, 0.5);
}

.header-txt p {
    font-size: 17px;
    color: #e0e0e0;
    margin-bottom: 45px;
    line-height: 1.6;
}

.butons {
    display: flex;
    gap: 15px;
}

.btn-1, .btn-2, .btn-3 {
    display: inline-block;
    padding: 11px 35px;
    border: 2px solid #80EDFF;
    border-radius: 25px;
    font-size: 17px;
    color: #ffffff;
    transition: all 0.3s ease;
    text-align: center;
    text-decoration: none;
    font-weight: 600;
    cursor: pointer;
}

.btn-1 {
    background-color: transparent;
}

.btn-1:hover {
    background-color: #80EDFF;
    color: #1b1721;
    box-shadow: 0 0 20px rgba(0, 251, 255, 0.6);
    transform: translateY(-3px);
}

.popular {
    padding: 100px 0;
    text-align: center;
    margin-top: 40px;
}

.popular video {
    margin-bottom: 50px;
    border-radius: 15px;
    border: 2px solid #80EDFF;
    width: 100%;
    box-shadow: 0 0 30px rgba(128, 237, 255, 0.3);
    transition: transform 0.3s ease;
}

.popular video:hover {
    transform: scale(1.02);
}

h2 {
    color: #ffffff;
    font-size: 35px;
    margin-bottom: 45px;
    font-weight: 700;
    position: relative;
    padding-bottom: 15px;
}

h2::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100px;
    height: 3px;
    background: linear-gradient(90deg, transparent, #80EDFF, transparent);
}

.popular-content {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
}

.popular-content a {
    transition: transform 0.3s ease;
}

.popular-content img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 10px;
    border: 2px solid #80EDFF;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.popular-content img:hover {
    transform: scale(1.1) rotateY(5deg);
    box-shadow: 0 0 20px rgba(255, 90, 44, 0.6);
}

.product-content {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    margin-bottom: 50px;
}

.product-1 {
    background: linear-gradient(135deg, #2a223a 0%, #3f3456 100%);
    border-radius: 15px;
    overflow: hidden;
    transition: all 0.3s ease;
    border: 2px solid #80EDFF;
    cursor: pointer;
    position: relative;
}

.product-1::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(128, 237, 255, 0.2), transparent);
    transition: left 0.5s ease;
    z-index: 1;
}

.product-1:hover::before {
    left: 100%;
}

.product-1:hover {
    transform: translateY(-15px);
    box-shadow: 0 15px 40px rgba(128, 237, 255, 0.4);
}

.product-1 img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: transform 0.3s ease;
}

.product-1:hover img {
    transform: scale(1.1);
}

.product-txt {
    padding: 30px;
    position: relative;
    z-index: 2;
}

h3 {
    font-size: 20px;
    color: #FFFFFF;
    margin-bottom: 20px;
    font-weight: 600;
}

.price {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.price p {
    font-size: 17px;
    color: #80EDFF;
    font-weight: 600;
}

.btn-2 {
    padding: 8px 25px;
    background-color: #1E3A8A;
    border: 2px solid #80EDFF;
    margin-right: 0;
    text-decoration: none;
}

.btn-2:hover {
    background-color: #80EDFF;
    color: #1b1721;
    box-shadow: 0 0 20px rgba(128, 237, 255, 0.5);
    transform: translateY(-2px);
}

/* NOTIFICACIONES TOAST */
.toast-container {
    position: fixed;
    top: 20px;
    right: 20px;
    z-index: 9999;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.toast {
    background: linear-gradient(135deg, #80EDFF 0%, #00FBFF 100%);
    color: #1b1721;
    padding: 16px 24px;
    border-radius: 10px;
    border-left: 5px solid #00FBFF;
    box-shadow: 0 4px 20px rgba(128, 237, 255, 0.5);
    display: flex;
    align-items: center;
    gap: 12px;
    font-weight: 600;
    min-width: 300px;
    animation: slideIn 0.4s ease;
}

.toast.success {
    background: linear-gradient(135deg, #1E3A8A 0%, #0A5FBF 100%);
    color: #80EDFF;
    border-left-color: #80EDFF;
}

.toast.error {
    background: linear-gradient(135deg, #8B0000 0%, #DC143C 100%);
    color: #FFFFFF;
    border-left-color: #FF6B6B;
}

.toast.info {
    background: linear-gradient(135deg, #4B0082 0%, #8B008B 100%);
    color: #80EDFF;
    border-left-color: #80EDFF;
}

.toast.warning {
    background: linear-gradient(135deg, #FF8C00 0%, #FFD700 100%);
    color: #1b1721;
    border-left-color: #FFD700;
}

@keyframes slideIn {
    from {
        transform: translateX(400px);
        opacity: 0;
    }
    to {
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes slideOut {
    from {
        transform: translateX(0);
        opacity: 1;
    }
    to {
        transform: translateX(400px);
        opacity: 0;
    }
}

@keyframes fadeInLeft {
    from {
        opacity: 0;
        transform: translateX(-30px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.toast.hide {
    animation: slideOut 0.4s ease forwards;
}

.toast-icon {
    font-size: 20px;
    flex-shrink: 0;
}

.toast-content {
    flex: 1;
}

.toast-close {
    cursor: pointer;
    font-size: 18px;
    font-weight: bold;
    opacity: 0.7;
    transition: opacity 0.3s ease;
    flex-shrink: 0;
}

.toast-close:hover {
    opacity: 1;
}

/* Modal de Notificación */
.modal {
    display: none;
    position: fixed;
    z-index: 2000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    animation: fadeIn 0.3s ease;
    overflow-y: auto;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

.modal-content {
    background: linear-gradient(135deg, #2a223a 0%, #3f3456 100%);
    margin: 5% auto;
    padding: 40px;
    border: 2px solid #80EDFF;
    border-radius: 15px;
    width: 90%;
    max-width: 500px;
    box-shadow: 0 0 40px rgba(128, 237, 255, 0.4);
    animation: slideDown 0.3s ease;
}

@keyframes slideDown {
    from {
        transform: translateY(-50px);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

.close-modal {
    color: #80EDFF;
    float: right;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
    transition: color 0.3s ease;
}

.close-modal:hover {
    color: #FFFFFF;
}

.modal h2 {
    color: #80EDFF;
    margin-bottom: 15px;
    font-size: 24px;
}

.modal-game-title {
    color: #FFFFFF;
    font-size: 18px;
    margin-bottom: 20px;
    font-weight: 600;
}

.modal-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.modal-form input {
    padding: 12px 15px;
    background-color: #3f3456;
    border: 2px solid #80EDFF;
    border-radius: 8px;
    outline: none;
    color: #80EDFF;
    font-size: 15px;
    transition: all 0.3s ease;
}

.modal-form input:focus {
    background-color: #4a4063;
    box-shadow: 0 0 15px rgba(128, 237, 255, 0.6);
    border-color: #FFFFFF;
}

.modal-form input::placeholder {
    color: #b0b0b0;
}

.btn-notify {
    padding: 12px 25px;
    background: linear-gradient(135deg, #80EDFF 0%, #00FBFF 100%);
    color: #1b1721;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn-notify:hover {
    background: linear-gradient(135deg, #FFFFFF 0%, #80EDFF 100%);
    box-shadow: 0 0 20px rgba(128, 237, 255, 0.6);
    transform: translateY(-2px);
}

.notification-message {
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 8px;
    text-align: center;
    font-weight: 600;
    display: none;
}

.notification-message.success {
    background-color: #1E3A8A;
    color: #80EDFF;
    border: 2px solid #80EDFF;
    display: block;
}

.notification-message.error {
    background-color: #8B0000;
    color: #FFFFFF;
    border: 2px solid #FF6B6B;
    display: block;
}

/* Secciones */
.section-title {
    color: #80EDFF;
    font-size: 14px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 10px;
}

.section-description {
    color: #b0b0b0;
    text-align: center;
    margin-bottom: 30px;
    font-size: 15px;
}

.contact {
    padding: 100px 50px;
}

.contact-content {
    background: linear-gradient(135deg, #2a223a 0%, #3f3456 100%);
    text-align: center;
    padding: 50px;
    border-radius: 50px;
    border: 2px solid #80EDFF;
    box-shadow: 0 0 30px rgba(128, 237, 255, 0.2);
}

.contact-content h3 {
    margin-bottom: 30px;
    font-size: 24px;
    color: #80EDFF;
}

.contact-content p {
    margin-bottom: 30px;
    color: #e0e0e0;
}

form {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
}

input {
    padding: 18px 25px;
    background-color: #3f3456;
    border: 2px solid #80EDFF;
    border-radius: 25px;
    outline: none;
    color: #80EDFF;
    font-size: 17px;
    transition: all 0.3s ease;
}

input[type="email"] {
    min-width: 300px;
}

input:focus {
    background-color: #4a4063;
    box-shadow: 0 0 20px rgba(128, 237, 255, 0.6);
    border-color: #FFFFFF;
}

::placeholder {
    color: #b0b0b0;
    font-size: 17px;
}

.btn-3 {
    background: linear-gradient(135deg, #1E3A8A 0%, #0A5FBF 100%);
    cursor: pointer;
    margin-right: 0;
    border: 2px solid #80EDFF;
    padding: 18px 35px;
}

.btn-3:hover {
    background: linear-gradient(135deg, #80EDFF 0%, #00FBFF 100%);
    color: #1b1721;
    box-shadow: 0 0 20px rgba(128, 237, 255, 0.6);
    transform: translateY(-2px);
}

.footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 50px 0;
    border-top: 2px solid #80EDFF;
    flex-wrap: wrap;
    gap: 30px;
    margin-top: 80px;
}

.link {
    flex: 1;
    min-width: 250px;
}

.link ul {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    list-style: none;
}

.link ul li > a {
    font-size: 17px;
    color: #FFFFFF;
    margin-right: 20px;
    transition: all 0.3s ease;
    text-decoration: none;
}

.link ul li > a:hover {
    color: #ff5a2c;
    transform: translateX(5px);
}

/* Responsive Design */
@media (max-width: 1024px) {
    .product-content {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .menu label {
        display: block;
    }

    .menu .navbar {
        position: absolute;
        top: 70px;
        left: 0;
        right: 0;
        background-color: rgba(27, 23, 33, 0.98);
        display: none;
        backdrop-filter: blur(10px);
    }

    #menu:checked ~ .navbar {
        display: block;
    }

    .menu .navbar ul {
        flex-direction: column;
    }

    .menu .navbar ul li a {
        padding: 15px 20px;
        border-bottom: 1px solid #3f3456;
    }

    .header {
        min-height: 60vh;
    }

    .header-content {
        flex-direction: column;
        margin-top: 120px;
    }

    .header-txt {
        flex-basis: 100%;
        text-align: center;
    }

    .header-txt h1 {
        font-size: 40px;
    }

    .butons {
        justify-content: center;
        flex-direction: column;
        align-items: center;
    }

    .btn-1 {
        width: 100%;
    }

    .product-content {
        grid-template-columns: 1fr;
        gap: 30px;
    }

    .contact {
        padding: 50px 20px;
    }

    .contact-content {
        padding: 30px;
        border-radius: 30px;
    }

    input[type="email"] {
        min-width: 250px;
    }

    .footer {
        flex-direction: column;
        text-align: center;
    }

    .link ul {
        justify-content: center;
    }

    .modal-content {
        width: 85%;
        margin: 30% auto;
    }

    .toast-container {
        top: 10px;
        right: 10px;
    }

    .toast {
        min-width: 280px;
    }
}

@media (max-width: 480px) {
    .header-txt h1 {
        font-size: 30px;
    }

    .header-txt p {
        font-size: 15px;
    }

    h2 {
        font-size: 24px;
    }

    .butons {
        flex-direction: column;
        width: 100%;
    }

    .btn-1, .btn-2, .btn-3 {
        width: 100%;
    }

    form {
        flex-direction: column;
    }

    input[type="email"] {
        min-width: 100%;
        width: 100%;
    }

    .popular-content {
        justify-content: center;
    }

    .popular-content img {
        width: 120px;
        height: 120px;
    }

    .modal-content {
        margin: 50% auto;
        padding: 25px;
    }

    .modal h2 {
        font-size: 20px;
    }

    .modal-form input {
        font-size: 14px;
    }

    .toast-container {
        top: 5px;
        right: 5px;
    }

    .toast {
        min-width: 250px;
        padding: 12px 16px;
        font-size: 14px;
    }

    .product-content {
        gap: 15px;
    }
}
        </style>
    </head>
    <body>

        <!-- ======================== CONTENEDOR DE NOTIFICACIONES ======================== -->
        <div class="toast-container" id="toastContainer"></div>

        <!-- ======================== MODAL DE NOTIFICACIÓN ======================== -->
        <div id="notificationModal" class="modal">
            <div class="modal-content">
                <span class="close-modal">&times;</span>
                <h2>🎮 Notificación de Lanzamiento</h2>
                <div id="notificationMessage" class="notification-message"></div>
                <p class="modal-game-title" id="gameTitle"></p>
                <form class="modal-form" id="notificationForm">
                    <input type="text" id="playerName" placeholder="Tu nombre" required>
                    <input type="email" id="playerEmail" placeholder="Tu correo electrónico" required>
                    <button type="submit" class="btn-notify">Notificarme</button>
                </form>
            </div>
        </div>

        <!-- ======================== HEADER ======================== -->
        <header class="header">
            <div class="menu container">
                <a href="#inicio" class="logo">NEXUS</a>
                <input type="checkbox" id="menu" />
                <label for="menu">
                    <img src="images/menu-icon.jpg" class="menu-icono" alt="Menú">
                </label>
                <nav class="navbar">
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#populares">Populares</a></li>
                        <li><a href="#destacados">Destacados</a></li>
                        <li><a href="#ofertas">Ofertas</a></li>
                        <li><a href="#proximos">Próximos</a></li>
                        <li><a href="#masvendidos">Más Vendidos</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </nav>
            </div>
            <div class="header-content container">
                <div class="header-txt">
                    <h1>Nexus <span>Game</span> <br> Store</h1>
                    <p>
                        Bienvenido a tu tienda de videojuegos en línea. Descubre los mejores títulos de 
                        las principales plataformas de gaming. Desde juegos indie hasta blockbusters AAA, 
                        encuentra todo lo que necesitas para tu próxima aventura gamer.
                    </p>
                    <div class="butons">
                        <a href="https://www.steampowered.com" target="_blank" class="btn-1">Steam</a>
                        <a href="https://www.epicgames.com/store/es-MX/" target="_blank" class="btn-1">Epic Games</a>
                    </div>
                </div>
            </div>
        </header>

        <!-- ======================== SECCIÓN BIENVENIDA ======================== -->
        <section class="popular container" id="inicio">
            <h2 style="margin-top: 0;">Bienvenido a Nexus Game Store</h2>
            <video width="100%" height="auto" controls poster="images/imagen-previa.jpg">
                <source src="videos/games.mp4" type="video/mp4">
                Tu navegador no soporta el formato de video.
            </video>
        </section>

        <!-- ======================== SECCIÓN JUEGOS POPULARES ======================== -->
        <section class="popular container" id="populares">
            <h2>Juegos Populares</h2>
            <p class="section-description">Los títulos más jugados y aclamados del momento</p>

            <div class="popular-content">
                <a href="https://www.steampowered.com/app/220840/Far_Cry_3/" target="_blank" title="Far Cry 3">
                    <img src="images/g1.jpg" alt="Far Cry 3">
                </a>
                <a href="https://store.playstation.com" target="_blank" title="PlayStation Store">
                    <img src="images/g2.jpg" alt="Juego popular 2">
                </a>
                <a href="https://www.xbox.com/es-ES/xbox-game-pass" target="_blank" title="Xbox Game Pass">
                    <img src="images/g3.jpg" alt="Juego popular 3">
                </a>
                <a href="https://www.gog.com" target="_blank" title="GOG">
                    <img src="images/g4.jpg" alt="Juego popular 4">
                </a>
                <a href="https://www.epicgames.com/store/es-MX/" target="_blank" title="Epic Games Store">
                    <img src="images/g5.jpg" alt="Juego popular 5">
                </a>
                <a href="https://www.nintendo.com/store/" target="_blank" title="Nintendo eShop">
                    <img src="images/g7.jpg" alt="Juego popular 6">
                </a>
                <a href="https://www.ubisoft.com" target="_blank" title="Ubisoft">
                    <img src="images/g6.jpg" alt="Juego popular 7">
                </a>
            </div>
        </section>

        <!-- ======================== SECCIÓN PRODUCTOS DESTACADOS ======================== -->
        <main class="product container" id="destacados">
            <h2>Productos Destacados</h2>
            <p class="section-description">Nuestros juegos más vendidos con ofertas especiales</p>

            <div class="product-content">
                <div class="product-1">
                    <img src="images/l6.jpg" alt="Juego de Acción Premium">  
                    <div class="product-txt">
                        <h3>Juego de Acción Premium</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Experimenta la acción pura con gráficos de última generación</p>
                        <div class="price">
                            <p>$59.99 USD</p>
                            <a href="https://www.steampowered.com" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l9.jpg" alt="RPG Aventura Épica">  
                    <div class="product-txt">
                        <h3>RPG Aventura Épica</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Sumérgete en un mundo fantástico lleno de misterios</p>
                        <div class="price">
                            <p>$49.99 USD</p>
                            <a href="https://www.epicgames.com/store/es-MX/" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l8.jpg" alt="Indie Estrategia">  
                    <div class="product-txt">
                        <h3>Indie Estrategia</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Desafía tu mente con este juego de estrategia innovador</p>
                        <div class="price">
                            <p>$29.99 USD</p>
                            <a href="https://www.gog.com" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>
            </div>
        </main>

        <!-- ======================== SECCIÓN OFERTAS ESPECIALES ======================== -->
        <section class="product container" id="ofertas">
            <h2>Ofertas Especiales</h2>
            <p class="section-description">Descuentos increíbles en juegos seleccionados</p>

            <div class="product-content">
                <div class="product-1">
                    <img src="images/l1.jpg" alt="Oferta 1">  
                    <div class="product-txt">
                        <h3>Oferta Game 1</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-40% descuento limitado</p>
                        <div class="price">
                            <p>$29.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l2.jpg" alt="Oferta 2">  
                    <div class="product-txt">
                        <h3>Oferta Game 2</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-50% descuento limitado</p>
                        <div class="price">
                            <p>$24.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l3.jpg" alt="Oferta 3">  
                    <div class="product-txt">
                        <h3>Oferta Game 3</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-35% descuento limitado</p>
                        <div class="price">
                            <p>$32.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/gta6.jpg" alt="Oferta 4">  
                    <div class="product-txt">
                        <h3>Oferta Game 4</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-45% descuento limitado</p>
                        <div class="price">
                            <p>$39.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/requiem.jpg" alt="Oferta 5">  
                    <div class="product-txt">
                        <h3>Oferta Game 5</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-30% descuento limitado</p>
                        <div class="price">
                            <p>$41.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/w.jpg" alt="Oferta 6">  
                    <div class="product-txt">
                        <h3>Oferta Game 6</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">-55% descuento limitado</p>
                        <div class="price">
                            <p>$22.49 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ======================== SECCIÓN PRÓXIMOS LANZAMIENTOS ======================== -->
        <section class="product container" id="proximos">
            <h2>Próximos Lanzamientos</h2>
            <p class="section-description">Los juegos más esperados que llegarán pronto</p>

            <div class="product-content">
                <div class="product-1">
                    <img src="images/gta6.jpg" alt="GTA 6">  
                    <div class="product-txt">
                        <h3>GTA 6</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el 19 de noviembre de 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="GTA 6" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/requiem.jpg" alt="Resident Evil Requiem">  
                    <div class="product-txt">
                        <h3>Resident Evil Requiem</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el 20 de Junio 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="Resident Evil Requiem" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/w.jpg" alt="Wolverine">  
                    <div class="product-txt">
                        <h3>Marvel's Wolverine</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el 10 de Julio 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="Marvel's Wolverine" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/Saros.jpg" alt="Próximo 4">  
                    <div class="product-txt">
                        <h3>SAROS</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el	30 de abril de 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="Próximo Lanzamiento 4" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/ph.jpg" alt="Próximo 5">  
                    <div class="product-txt">
                        <h3>Próximo Lanzamiento 5</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el 9 de septiembre de 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="Próximo Lanzamiento 5" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/fabjpg.jpg" alt="Próximo 6">  
                    <div class="product-txt">
                        <h3>Fable</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Disponible el 7 de junio de 2026</p>
                        <div class="price">
                            <p>Preventa</p>
                            <button type="button" class="btn-2 notify-btn" data-game="Próximo Lanzamiento 6" onclick="abrirModalNotificacion(this)">Notificar</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ======================== SECCIÓN MÁS VENDIDOS ======================== -->
        <section class="product container" id="masvendidos">
            <h2>Más Vendidos</h2>
            <p class="section-description">Los juegos con más éxito de este año</p>

            <div class="product-content">
                <div class="product-1">
                    <img src="images/l6.jpg" alt="Top 1">  
                    <div class="product-txt">
                        <h3>🥇 Game Top 1</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Mejor juego del año</p>
                        <div class="price">
                            <p>$59.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l9.jpg" alt="Top 2">  
                    <div class="product-txt">
                        <h3>🥈 Game Top 2</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Segundo más vendido</p>
                        <div class="price">
                            <p>$49.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l8.jpg" alt="Top 3">  
                    <div class="product-txt">
                        <h3>🥉 Game Top 3</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Tercero más vendido</p>
                        <div class="price">
                            <p>$44.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l1.jpg" alt="Top 4">  
                    <div class="product-txt">
                        <h3>Game Top 4</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Cuarto más vendido</p>
                        <div class="price">
                            <p>$39.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l2.jpg" alt="Top 5">  
                    <div class="product-txt">
                        <h3>Game Top 5</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Quinto más vendido</p>
                        <div class="price">
                            <p>$34.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>

                <div class="product-1">
                    <img src="images/l3.jpg" alt="Top 6">  
                    <div class="product-txt">
                        <h3>Game Top 6</h3>
                        <p style="color: #b0b0b0; font-size: 14px; margin-bottom: 15px;">Sexto más vendido</p>
                        <div class="price">
                            <p>$29.99 USD</p>
                            <a href="#" target="_blank" class="btn-2">Comprar</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ======================== SECCIÓN CONTACTO ======================== -->
        <section class="contact container" id="contacto">
            <div class="contact-content">
                <h3>Suscríbete a Nuestro Boletín</h3>
                <p>Recibe las últimas noticias, ofertas exclusivas y lanzamientos próximos</p>
                <form>
                    <input type="email" placeholder="tu@correo.com" required>
                    <input type="submit" class="btn-3" value="Enviar">
                </form>
            </div>
        </section>

        <!-- ======================== FOOTER ======================== -->
        <footer class="footer container">
            <div class="link">      
                <a href="#inicio" class="logo">NEXUS</a>
            </div>

            <div class="link">
                <h3 style="color: #80EDFF; margin-bottom: 15px; font-size: 16px;">Navegación</h3>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#populares">Populares</a></li>
                    <li><a href="#destacados">Destacados</a></li>
                    <li><a href="#ofertas">Ofertas</a></li>
                    <li><a href="#proximos">Próximos</a></li>
                    <li><a href="#masvendidos">Más Vendidos</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </div>

            <div class="link">
                <h3 style="color: #80EDFF; margin-bottom: 15px; font-size: 16px;">Plataformas</h3>
                <ul>
                    <li><a href="http://www.steampowered.com" target="_blank">Steam</a></li>
                    <li><a href="https://www.epicgames.com/store/es-MX/" target="_blank">Epic Games</a></li>
                    <li><a href="https://store.playstation.com" target="_blank">PlayStation</a></li>
                    <li><a href="https://www.xbox.com/es-ES/xbox-game-pass" target="_blank">Xbox</a></li>
                </ul>
            </div>

            <div class="link">
                <h3 style="color: #80EDFF; margin-bottom: 15px; font-size: 16px;">Más</h3>
                <ul>
                    <li><a href="https://www.gog.com" target="_blank">GOG</a></li>
                    <li><a href="https://www.nintendo.com/store/" target="_blank">Nintendo</a></li>
                    <li><a href="https://www.ubisoft.com" target="_blank">Ubisoft</a></li>
                </ul>
            </div>
        </footer>

        <script>
// ======================== FUNCIÓN DE NOTIFICACIONES TOAST ========================
function showToast(message, type = 'success', duration = 4000) {
    const toastContainer = document.getElementById('toastContainer');
    
    const toast = document.createElement('div');
    toast.className = `toast ${type}`;
    
    const icons = {
        success: '✅',
        error: '❌',
        info: 'ℹ️',
        warning: '⚠️'
    };
    
    toast.innerHTML = `
        <span class="toast-icon">${icons[type]}</span>
        <span class="toast-content">${message}</span>
        <span class="toast-close">&times;</span>
    `;
    
    toastContainer.appendChild(toast);
    
    // Cerrar al hacer click
    const closeBtn = toast.querySelector('.toast-close');
    closeBtn.addEventListener('click', () => {
        toast.classList.add('hide');
        setTimeout(() => toast.remove(), 400);
    });
    
    // Auto-cerrar después del tiempo especificado
    setTimeout(() => {
        if (toast.parentNode) {
            toast.classList.add('hide');
            setTimeout(() => toast.remove(), 400);
        }
    }, duration);
}

// ======================== FUNCIÓN PARA ABRIR MODAL ========================
function abrirModalNotificacion(button) {
    const gameName = button.getAttribute('data-game');
    const modal = document.getElementById('notificationModal');
    const gameTitle = document.getElementById('gameTitle');
    
    gameTitle.textContent = gameName;
    modal.style.display = 'block';
    
    // Mostrar notificación
    showToast(`🎮 Abriendo formulario para: ${gameName}`, 'info', 3000);
}

// ======================== MODAL Y FUNCIONALIDAD DE NOTIFICACIONES ========================
const modal = document.getElementById('notificationModal');
const closeModal = document.querySelector('.close-modal');
const notificationForm = document.getElementById('notificationForm');
const notificationMessage = document.getElementById('notificationMessage');

// Cerrar modal
closeModal.addEventListener('click', function() {
    modal.style.display = 'none';
});

window.addEventListener('click', function(event) {
    if (event.target === modal) {
        modal.style.display = 'none';
    }
});

// Enviar notificación
notificationForm.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const name = document.getElementById('playerName').value;
    const email = document.getElementById('playerEmail').value;
    const game = document.getElementById('gameTitle').textContent;
    
    // Validar email
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    
    if (!emailRegex.test(email)) {
        showToast('Por favor ingresa un email válido', 'error', 4000);
        notificationMessage.textContent = '❌ Por favor ingresa un email válido';
        notificationMessage.className = 'notification-message error';
        return;
    }
    
    // Guardar en localStorage
    const notifications = JSON.parse(localStorage.getItem('gameNotifications') || '[]');
    notifications.push({
        name: name,
        email: email,
        game: game,
        date: new Date().toLocaleString('es-ES')
    });
    localStorage.setItem('gameNotifications', JSON.stringify(notifications));
    
    // Mostrar toast de éxito
    showToast(`✅ ¡Te notificaremos cuando ${game} se lance!`, 'success', 5000);
    
    // Mostrar mensaje en modal
    notificationMessage.innerHTML = `✅ <strong>¡Registro completado!</strong><br>Te notificaremos cuando <strong>${game}</strong> se lance.`;
    notificationMessage.className = 'notification-message success';
    
    // Contar registros
    console.log(`Total de registros: ${notifications.length}`);
    
    // Cerrar modal y resetear formulario
    setTimeout(() => {
        notificationForm.reset();
        modal.style.display = 'none';
        notificationMessage.innerHTML = '';
        notificationMessage.className = 'notification-message';
    }, 3000);
});
        </script>

    </body>
</html>
