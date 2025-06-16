# 👋 Hi, I'm wastedswl — Fullstack Dev & AI Engineer

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=wastedswl&show_icons=true&theme=radical&count_private=true" alt="wastedswl's GitHub Stats" />
</p>

---

## 🔥 About Me

- 🚀 Fullstack developer (JS/TS, Node.js, React)
- 🎮 GameDev enthusiast — люблю создавать интерактивные игры и визуализации
- 🤖 AI Engineer — внедряю нейросети и автоматизацию в проекты
- 🌱 Сейчас изучаю продвинутый React, WebGL и машинное обучение
- 📫 How to reach me: [email@example.com](mailto:email@example.com) | [LinkedIn](https://linkedin.com/in/wastedswl)

---

## 🐍 Contribution Snake

<p align="center">
  <img src="https://github.com/wastedswl/wastedswl/blob/output/github-contribution-grid-snake.svg" alt="snake animation" />
</p>

---

## 🎮 Мини-игра: Классическая змейка в SVG (Прямо здесь!)

<p align="center">
  <svg id="snake-game" width="320" height="320" viewBox="0 0 320 320" style="border: 2px solid #58a6ff; background: #0d1117; cursor: pointer;">
    <style>
      .snake-body { fill: #58a6ff; }
      .food { fill: #ff4757; }
    </style>
    <rect width="320" height="320" fill="#0d1117"/>
  </svg>
</p>

<script>
  (() => {
    const svg = document.getElementById('snake-game');
    if (!svg) return;
    const size = 20;
    const width = 16;
    const height = 16;
    let snake = [{x:8, y:8}];
    let dir = {x:1, y:0};
    let food = {x:Math.floor(Math.random()*width), y:Math.floor(Math.random()*height)};
    let running = true;

    function draw() {
      while(svg.firstChild) svg.removeChild(svg.firstChild);
      // background
      let bg = document.createElementNS("http://www.w3.org/2000/svg","rect");
      bg.setAttribute("width", "320");
      bg.setAttribute("height", "320");
      bg.setAttribute("fill", "#0d1117");
      svg.appendChild(bg);

      // food
      let f = document.createElementNS("http://www.w3.org/2000/svg","rect");
      f.setAttribute("x", food.x * size);
      f.setAttribute("y", food.y * size);
      f.setAttribute("width", size);
      f.setAttribute("height", size);
      f.setAttribute("class", "food");
      svg.appendChild(f);

      // snake
      snake.forEach(part => {
        let s = document.createElementNS("http://www.w3.org/2000/svg","rect");
        s.setAttribute("x", part.x * size);
        s.setAttribute("y", part.y * size);
        s.setAttribute("width", size);
        s.setAttribute("height", size);
        s.setAttribute("class", "snake-body");
        svg.appendChild(s);
      });
    }

    function update() {
      if (!running) return;
      const head = {...snake[0]};
      head.x += dir.x;
      head.y += dir.y;

      if(head.x < 0 || head.x >= width || head.y < 0 || head.y >= height) {
        running = false; alert('Game Over! Hit the wall. Refresh to restart.');
        return;
      }
      if(snake.some((s,i) => i!==0 && s.x===head.x && s.y===head.y)) {
        running = false; alert('Game Over! Snake bit itself. Refresh to restart.');
        return;
      }

      snake.unshift(head);

      if(head.x === food.x && head.y === food.y) {
        food = {x:Math.floor(Math.random()*width), y:Math.floor(Math.random()*height)};
      } else {
        snake.pop();
      }
    }

    function changeDir(e) {
      if(!running) return;
      switch(e.key) {
        case "ArrowUp": if(dir.y!==1){dir={x:0,y:-1}} break;
        case "ArrowDown": if(dir.y!==-1){dir={x:0,y:1}} break;
        case "ArrowLeft": if(dir.x!==1){dir={x:-1,y:0}} break;
        case "ArrowRight": if(dir.x!==-1){dir={x:1,y:0}} break;
      }
    }

    document.addEventListener('keydown', changeDir);

    function loop() {
      update();
      draw();
      if(running) setTimeout(loop, 150);
    }

    loop();
  })();
</script>

---

## 🤖 AI Projects & Experiments

- [AI Chatbot](https://github.com/wastedswl/ai-chatbot) — Node.js + React chatbot with GPT integration
- [Game AI](https://github.com/wastedswl/game-ai) — AI-powered NPC behavior for games
- [ML Visualizer](https://github.com/wastedswl/ml-visualizer) — Interactive machine learning demos in React

---

## 📈 GitHub Activity & Stats

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=wastedswl&theme=react-dark&area=true" alt="Activity Graph" />
</p>

---

## 🛠 Tech Stack

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=for-the-badge" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white&style=for-the-badge" />
<img src="https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black&style=for-the-badge" />
<img src="https://img.shields.io/badge/WebGL-FFFFFF?logo=opengl&logoColor=black&style=for-the-badge" />
<img src="https://img.shields.io/badge/GitHub-A0A0A0?logo=github&logoColor=white&style=for-the-badge" />

---

## 📫 Get in Touch

<p align="center">
  <a href="mailto:email@example.com"><img src="https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white&style=for-the-badge" /></a>
  <a href="https://linkedin.com/in/wastedswl"><img src="https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white&style=for-the-badge" /></a>
  <a href="https://twitter.com/wastedswl"><img src="https://img.shields.io/badge/Twitter-1DA1F2?logo=twitter&logoColor=white&style=for-the-badge" /></a>
</p>
