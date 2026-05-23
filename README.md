<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TechWorld — Мир Компьютеров</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: #0d1117;
      color: white;
      overflow-x: hidden;
      position: relative;
    }

    .background-animation {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: -1;
    }

    .background-animation span {
      position: absolute;
      display: block;
      width: 220px;
      height: 220px;
      background: rgba(0, 217, 255, 0.08);
      border-radius: 50%;
      animation: move 25s linear infinite;
      bottom: -250px;
      backdrop-filter: blur(10px);
      box-shadow: 0 0 40px rgba(0,217,255,0.2);
    }

    .background-animation span:nth-child(1) {
      left: 10%;
      width: 300px;
      height: 300px;
      animation-duration: 22s;
    }

    .background-animation span:nth-child(2) {
      left: 25%;
      animation-duration: 18s;
      animation-delay: 2s;
    }

    .background-animation span:nth-child(3) {
      left: 40%;
      width: 260px;
      height: 260px;
      animation-duration: 30s;
    }

    .background-animation span:nth-child(4) {
      left: 55%;
      animation-duration: 20s;
      animation-delay: 1s;
    }

    .background-animation span:nth-child(5) {
      left: 70%;
      width: 340px;
      height: 340px;
      animation-duration: 26s;
    }

    .background-animation span:nth-child(6) {
      left: 85%;
      animation-duration: 17s;
      animation-delay: 3s;
    }

    .background-animation span:nth-child(7) {
      left: 5%;
      width: 180px;
      height: 180px;
      animation-duration: 28s;
    }

    .background-animation span:nth-child(8) {
      left: 90%;
      width: 240px;
      height: 240px;
      animation-duration: 24s;
    }

    @keyframes move {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 0;
      }

      10% {
        opacity: 1;
      }

      50% {
        transform: translateY(-500px) rotate(180deg);
      }

      100% {
        transform: translateY(-1200px) rotate(360deg);
        opacity: 0;
      }
    }

    @keyframes rainbow {
      0% { filter: hue-rotate(0deg); }
      100% { filter: hue-rotate(360deg); }
    }

      10% {
        opacity: 1;
      }

      50% {
        transform: translateY(-500px) rotate(180deg);
      }

      100% {
        transform: translateY(-1200px) rotate(360deg);
        opacity: 0;
      }
    }

    @keyframes animatedBg {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    header {
      width: 100%;
      position: fixed;
      top: 0;
      left: 0;
      padding: 20px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: rgba(0,0,0,0.5);
      backdrop-filter: blur(10px);
      z-index: 1000;
    }

    .logo {
      font-family: 'Orbitron', sans-serif;
      font-size: 28px;
      font-weight: 700;
      color: #00d9ff;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 30px;
      transition: 0.3s;
      font-weight: 500;
    }

    nav a:hover {
      color: #00d9ff;
    }

    .hero {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      background: linear-gradient(to right, rgba(0,0,0,0.8), rgba(0,0,0,0.6)),
      url('https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=1600&auto=format&fit=crop') center/cover;
      padding: 0 20px;
    }

    .hero-content h1 {
      font-size: 70px;
      font-family: 'Orbitron', sans-serif;
      margin-bottom: 20px;
      animation: fadeDown 1s ease;
    }

    .hero-content p {
      font-size: 22px;
      max-width: 700px;
      margin: auto;
      margin-bottom: 35px;
      color: #d1d5db;
      animation: fadeUp 1s ease;
    }

    .btn {
      padding: 15px 35px;
      border: none;
      background: linear-gradient(90deg, #00d9ff, #7c3aed);
      color: white;
      border-radius: 40px;
      font-size: 18px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 0 25px rgba(0,217,255,0.5);
      position: relative;
      overflow: hidden;
    }

    .btn::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: rgba(255,255,255,0.2);
      transition: 0.5s;
    }

    .btn:hover::before {
      left: 100%;
    }

    .btn:hover {
      transform: scale(1.08);
      box-shadow: 0 0 35px rgba(0,217,255,0.8);
    }

    .btn:active {
      transform: scale(0.96);
    }

    .btn:hover {
      transform: scale(1.05);
      background: white;
    }

    section {
      padding: 100px 8%;
    }

    .title {
      text-align: center;
      font-size: 42px;
      margin-bottom: 60px;
      font-family: 'Orbitron', sans-serif;
      color: #00d9ff;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 30px;
    }

    .card {
      background: #161b22;
      padding: 30px;
      border-radius: 20px;
      transition: 0.4s;
      border: 1px solid rgba(255,255,255,0.1);
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      width: 100%;
      height: 5px;
      background: linear-gradient(90deg, #00d9ff, #7c3aed);
      top: 0;
      left: 0;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 0 25px rgba(0,217,255,0.3);
    }

    .card h3 {
      font-size: 26px;
      margin-bottom: 15px;
      color: #00d9ff;
    }

    .card p {
      color: #cbd5e1;
      line-height: 1.7;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
    }

    .gallery img {
      width: 100%;
      height: 260px;
      object-fit: cover;
      border-radius: 20px;
      transition: 0.4s;
      box-shadow: 0 0 20px rgba(0,0,0,0.4);
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 25px;
      align-items: stretch;
    }

    .gallery img:hover {
      transform: scale(1.03);
    }

    .stats {
      display: flex;
      justify-content: center;
      gap: 60px;
      flex-wrap: wrap;
      text-align: center;
    }

    .stat-box h2 {
      font-size: 50px;
      color: #00d9ff;
    }

    .stat-box p {
      color: #cbd5e1;
      margin-top: 10px;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #05080d;
      color: #94a3b8;
    }

    .scroll-top {
      position: fixed;
      right: 20px;
      bottom: 20px;
      background: #00d9ff;
      color: black;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      font-size: 22px;
      opacity: 0;
      pointer-events: none;
      transition: 0.3s;
    }

    .scroll-top.show {
      opacity: 1;
      pointer-events: auto;
    }

    @keyframes fadeDown {
      from {
        opacity: 0;
        transform: translateY(-40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media(max-width: 768px) {
      .hero-content h1 {
        font-size: 42px;
      }

      nav {
        display: none;
      }
    }
  </style>
</head>
<body>

  <div class="background-animation">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>

  <header>
    <div class="logo">TechWorld</div>

    <nav>
      <a href="#about">О нас</a>
      <a href="#components">Комплектующие</a>
      <a href="#gallery">Галерея</a>
      <a href="#stats">Статистика</a>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h1>Мир Современных Компьютеров</h1>
      <p>
        Изучай мощные ПК, игровые системы, современные технологии и комплектующие будущего.
      </p>
      <button class="btn" onclick="showMessage()">Узнать больше</button>
    </div>
  </section>

  <section id="about">
    <h2 class="title">О Компьютерах</h2>

    <div class="cards">
      <div class="card">
        <h3>Что такое компьютер?</h3>
        <p>
          Компьютер — это электронное устройство для обработки информации. Современные компьютеры используются для игр, работы, программирования, монтажа видео, создания графики и обучения.
        </p>
      </div>

      <div class="card">
        <h3>История компьютеров</h3>
        <p>
          Первые компьютеры занимали целые комнаты и имели очень низкую производительность. Сегодня даже домашние ПК мощнее суперкомпьютеров прошлого.
        </p>
      </div>

      <div class="card">
        <h3>Современные технологии</h3>
        <p>
          Искусственный интеллект, трассировка лучей, облачные вычисления и VR технологии активно развиваются благодаря мощным компьютерам.
        </p>
      </div>

      <div class="card">
        <h3>Игровые компьютеры</h3>
        <p>
          Игровые ПК отличаются мощными видеокартами, быстрыми процессорами и RGB подсветкой. Они подходят для современных игр на высоких настройках.
        </p>
      </div>
    </div>
  </section>

  <section id="components">
    <h2 class="title">Подробно о Комплектующих ПК</h2>

    <div class="cards">
      <div class="card">
        <h3>Процессор (CPU)</h3>
        <p>
          Процессор — это главный компонент компьютера. Он выполняет вычисления и управляет работой системы. Популярные производители: Intel и AMD.
        </p>
      </div>

      <div class="card">
        <h3>Видеокарта (GPU)</h3>
        <p>
          Видеокарта отвечает за графику в играх и программах. RTX видеокарты поддерживают технологии DLSS и Ray Tracing.
        </p>
      </div>

      <div class="card">
        <h3>Материнская плата</h3>
        <p>
          Материнская плата соединяет все компоненты компьютера. От нее зависит поддержка процессора, памяти и накопителей.
        </p>
      </div>

      <div class="card">
        <h3>Оперативная память RAM</h3>
        <p>
          RAM хранит временные данные программ и игр. Чем больше оперативной памяти, тем быстрее работает компьютер.
        </p>
      </div>

      <div class="card">
        <h3>SSD накопители</h3>
        <p>
          SSD работают намного быстрее HDD. Они ускоряют запуск системы, загрузку игр и копирование файлов.
        </p>
      </div>

      <div class="card">
        <h3>Жесткие диски HDD</h3>
        <p>
          HDD подходят для хранения больших объемов данных: фильмов, игр, архивов и документов.
        </p>
      </div>

      <div class="card">
        <h3>Система охлаждения</h3>
        <p>
          Кулеры и водяное охлаждение предотвращают перегрев процессора и видеокарты.
        </p>
      </div>

      <div class="card">
        <h3>Блок питания</h3>
        <p>
          Блок питания обеспечивает электроэнергией все комплектующие компьютера.
        </p>
      </div>

      <div class="card">
        <h3>Игровой корпус</h3>
        <p>
          Красивый корпус с RGB подсветкой делает компьютер современным и улучшает вентиляцию.
        </p>
      </div>

      <div class="card">
        <h3>Монитор</h3>
        <p>
          Игровые мониторы имеют высокую герцовку 144Hz, 240Hz и минимальное время отклика.
        </p>
      </div>

      <div class="card">
        <h3>Клавиатура</h3>
        <p>
          Механические клавиатуры популярны среди геймеров благодаря быстрому отклику и RGB подсветке.
        </p>
      </div>

      <div class="card">
        <h3>Компьютерная мышь</h3>
        <p>
          Игровые мышки имеют высокую точность DPI и дополнительные программируемые кнопки.
        </p>
      </div>
    </div>
  </section>

  <section id="gallery">
    <h2 class="title">Галерея Комплектующих ПК</h2>

    <div class="gallery">
      <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=1200&auto=format&fit=crop" alt="Gaming PC">
      <img src="https://images.unsplash.com/photo-1591799264318-7e6ef8ddb7ea?q=80&w=1200&auto=format&fit=crop" alt="GPU">
      <img src="https://images.unsplash.com/photo-1587202372634-32705e3bf49c?q=80&w=1200&auto=format&fit=crop" alt="Motherboard">
      <img src="https://images.unsplash.com/photo-1587831990711-23ca6441447b?q=80&w=1200&auto=format&fit=crop" alt="RAM">
      <img src="https://images.unsplash.com/photo-1562976540-1502c2145186?q=80&w=1200&auto=format&fit=crop" alt="SSD">
      <img src="https://images.unsplash.com/photo-1591488320449-011701bb6704?q=80&w=1200&auto=format&fit=crop" alt="Cooling">
      <img src="https://images.unsplash.com/photo-1541807084-5c52b6b3adef?q=80&w=1200&auto=format&fit=crop" alt="Monitor">
      <img src="https://images.unsplash.com/photo-1527443224154-c4a3942d3acf?q=80&w=1200&auto=format&fit=crop" alt="Keyboard">
      <img src="https://images.unsplash.com/photo-1612287230202-1ff1d85d1bdf?q=80&w=1200&auto=format&fit=crop" alt="Gaming Setup">
    </div>
  </section>

  <section id="info">
    <h2 class="title">Большая Энциклопедия ПК</h2>

    <div class="cards">
      <div class="card">
        <h3>Как собрать компьютер?</h3>
        <p>
          Для сборки ПК нужно выбрать процессор, материнскую плату, видеокарту, память, SSD, блок питания и корпус. Все компоненты должны быть совместимы.
        </p>
      </div>

      <div class="card">
        <h3>Лучшие процессоры 2026</h3>
        <p>
          Intel Core Ultra и AMD Ryzen 9000 обеспечивают высокую производительность для игр и профессиональных задач.
        </p>
      </div>

      <div class="card">
        <h3>Игровые видеокарты RTX</h3>
        <p>
          RTX видеокарты поддерживают нейросети, генерацию кадров и ультра графику в современных играх.
        </p>
      </div>

      <div class="card">
        <h3>Что такое FPS?</h3>
        <p>
          FPS — количество кадров в секунду. Чем выше FPS, тем плавнее работает игра.
        </p>
      </div>

      <div class="card">
        <h3>Что такое герцовка?</h3>
        <p>
          Герцовка монитора показывает количество обновлений экрана в секунду. 144Hz и 240Hz делают изображение плавным.
        </p>
      </div>

      <div class="card">
        <h3>Для чего нужен SSD?</h3>
        <p>
          SSD ускоряет загрузку Windows и игр. NVMe SSD намного быстрее обычных SATA накопителей.
        </p>
      </div>

      <div class="card">
        <h3>Охлаждение ПК</h3>
        <p>
          Хорошее охлаждение продлевает срок службы компонентов и снижает температуру процессора.
        </p>
      </div>

      <div class="card">
        <h3>RGB Подсветка</h3>
        <p>
          RGB используется в вентиляторах, клавиатурах и корпусах для красивого внешнего вида игрового ПК.
        </p>
      </div>

      <div class="card">
        <h3>Киберспорт</h3>
        <p>
          Профессиональные игроки используют мощные компьютеры с высокой частотой кадров и быстрыми мониторами.
        </p>
      </div>

      <div class="card">
        <h3>Компьютеры будущего</h3>
        <p>
          В будущем компьютеры станут еще мощнее благодаря квантовым технологиям и искусственному интеллекту.
        </p>
      </div>
    </div>
  </section>

  <section id="stats">
    <h2 class="title">Статистика</h2>

    <div class="stats">
      <div class="stat-box">
        <h2 id="count1">0</h2>
        <p>Игровых ПК</p>
      </div>

      <div class="stat-box">
        <h2 id="count2">0</h2>
        <p>Мощных GPU</p>
      </div>

      <div class="stat-box">
        <h2 id="count3">0</h2>
        <p>Пользователей</p>
      </div>
    </div>
  </section>

  <footer>
    © 2026 TechWorld — Большой сайт про компьютеры и технологии
  </footer>
    © 2026 TechWorld — Сайт про компьютеры и технологии
  </footer>

  <div class="scroll-top" id="scrollTop">↑</div>

  <script>

    document.addEventListener('DOMContentLoaded', () => {

    let clickCount = 0;
    let secretCode = '';
    let matrixMode = false;

    // TECH MODE
    document.addEventListener('keydown', (e) => {
      if (e.key.toLowerCase() === 't') {
        document.body.style.filter = 'hue-rotate(120deg)';

        setTimeout(() => {
          document.body.style.filter = 'none';
        }, 3000);

        alert('Пасхалка найдена: Tech Mode активирован!');
      }
    });

    // GAMER MODE
    document.querySelector('.logo').addEventListener('click', () => {
      clickCount++;

      if (clickCount >= 5) {
        document.body.style.background = 'black';
        alert('Секретный Gamer Mode активирован 🎮');
        clickCount = 0;
      }
    });

    // NEON MODE
    document.addEventListener('dblclick', () => {
      const colors = ['#00d9ff', '#7c3aed', '#22c55e', '#ff004c'];
      const random = colors[Math.floor(Math.random() * colors.length)];

      document.querySelectorAll('.card').forEach(card => {
        card.style.boxShadow = `0 0 30px ${random}`;
      });
    });

    // MATRIX MODE
    document.addEventListener('keydown', (e) => {
      secretCode += e.key.toLowerCase();

      if (secretCode.includes('matrix')) {
        matrixMode = !matrixMode;

        if (matrixMode) {
          document.body.style.background = 'black';

          document.querySelectorAll('*').forEach(el => {
            el.style.color = '#00ff00';
          });

          alert('MATRIX MODE ACTIVATED');
        } else {
          location.reload();
        }

        secretCode = '';
      }
    });

    // ЛЕТАЮЩИЙ ПК
    document.addEventListener('keydown', (e) => {
      if (e.key.toLowerCase() === 'p') {
        const cpu = document.createElement('div');

        cpu.innerHTML = '🖥️';
        cpu.style.position = 'fixed';
        cpu.style.fontSize = '70px';
        cpu.style.left = '-100px';
        cpu.style.top = Math.random() * 500 + 'px';
        cpu.style.zIndex = '9999';
        cpu.style.transition = '5s linear';

        document.body.appendChild(cpu);

        setTimeout(() => {
          cpu.style.left = '120%';
        }, 100);

        setTimeout(() => {
          cpu.remove();
        }, 6000);
      }
    });

    // RAINBOW MODE
    document.addEventListener('keydown', (e) => {
      if (e.key.toLowerCase() === 'r') {
        document.querySelectorAll('.card').forEach(card => {
          card.style.animation = 'rainbow 2s linear infinite';
        });

        alert('Rainbow Mode 🌈');
      }
    });

    // FPS BOOST
    document.addEventListener('keydown', (e) => {
      if (e.key.toLowerCase() === 'f') {
        const fps = document.createElement('div');

        fps.innerHTML = 'FPS BOOST +999';
        fps.style.position = 'fixed';
        fps.style.top = '20px';
        fps.style.right = '20px';
        fps.style.padding = '15px 25px';
        fps.style.background = '#00ff00';
        fps.style.color = 'black';
        fps.style.fontWeight = 'bold';
        fps.style.borderRadius = '12px';
        fps.style.zIndex = '99999';

        document.body.appendChild(fps);

        setTimeout(() => {
          fps.remove();
        }, 3000);
      }
    });

    });

    function showMessage() {
      const section = document.getElementById('components');

      section.scrollIntoView({
        behavior: 'smooth'
      });

      const btn = document.querySelector('.btn');
      btn.innerText = 'Загрузка технологий...';

      setTimeout(() => {
        btn.innerText = 'Технологии загружены ✓';
      }, 1500);
    }

    function animateCounter(id, target, speed) {
      let element = document.getElementById(id);
      let count = 0;

      let interval = setInterval(() => {
        count += Math.ceil(target / speed);

        if (count >= target) {
          count = target;
          clearInterval(interval);
        }

        element.innerText = count + '+';
      }, 20);
    }

    animateCounter('count1', 5000, 100);
    animateCounter('count2', 12000, 120);
    animateCounter('count3', 500000, 150);

    const scrollTopBtn = document.getElementById('scrollTop');

    window.addEventListener('scroll', () => {
      if (window.scrollY > 300) {
        scrollTopBtn.classList.add('show');
      } else {
        scrollTopBtn.classList.remove('show');
      }
    });

    scrollTopBtn.addEventListener('click', () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });
  </script>

</body>
</html>
