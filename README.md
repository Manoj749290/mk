<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body {
      line-height: 1.6;
      background: #f9f9f9;
      color: #333;
    }
    /* Navbar */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #333;
      color: #fff;
      padding: 1rem;
    }
    .navbar .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }
    .nav-links {
      display: flex;
      list-style: none;
    }
    .nav-links li {
      margin-left: 15px;
    }
    .nav-links a {
      text-decoration: none;
      color: #fff;
      font-weight: bold;
    }
    /* Hero */
    .hero {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 80vh;
      background: #444;
      color: white;
      text-align: center;
    }
    .hero .btn {
      margin-top: 15px;
      background: #fff;
      color: #333;
      padding: 10px 20px;
      border-radius: 5px;
      text-decoration: none;
    }
    /* Sections */
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    .about-content, .project-grid, .quiz-container, .container {
      margin-top: 20px;
    }
    /* Projects */
    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .project-card {
      background: white;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
      text-align: center;
    }
    /* Quiz App */
    .quiz-container {
      background: white;
      padding: 20px;
      border-radius: 10px;
      width: 90%;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
    .quiz-container ul {
      list-style: none;
      margin-bottom: 20px;
    }
    .quiz-container li {
      margin: 10px 0;
    }
    .quiz-container button {
      background: #333;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .quiz-container button:hover {
      background: #555;
    }
    .result {
      font-size: 18px;
      font-weight: bold;
      text-align: center;
    }
    /* Blog */
    .post {
      background: white;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 8px;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
    }
    .post h2 {
      margin: 0 0 10px;
    }
    .post small {
      color: gray;
      font-size: 12px;
    }
    /* Contact */
    form {
      display: flex;
      flex-direction: column;
      max-width: 500px;
      margin: auto;
    }
    form input, form textarea {
      margin: 10px 0;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    form button {
      padding: 10px;
      border: none;
      background: #333;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
    form button:hover {
      background: #555;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #333;
      color: white;
      margin-top: 30px;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">MyPortfolio</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Hello, I'm <span>Mr. Your Name</span></h1>
      <p>I am a student passionate about web development.</p>
      <a href="#projects" class="btn">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="about-content">
      <p>I am enthusiastic about technology and design. I love building interactive, user-friendly web applications and exploring new tools in the tech world.</p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Project 1</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Project 2</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Project 3</h3><p>Personal blog with CMS.</p></div>
    </div>
  </section>

  <!-- Quiz App -->
  <section id="quiz">
    <h2>Quiz App</h2>
    <div class="quiz-container" id="quizContainer">
      <h2 id="question">Question text</h2>
      <ul>
        <li><label><input type="radio" name="answer" class="answer" id="a"> <span id="a_text">Answer A</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="b"> <span id="b_text">Answer B</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="c"> <span id="c_text">Answer C</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="d"> <span id="d_text">Answer D</span></label></li>
      </ul>
      <button id="submit">Submit</button>
      <div class="result" id="result"></div>
    </div>
  </section>

  <!-- Blog -->
  <section id="blog">
    <h2>My Blog</h2>
    <div class="container" id="postsContainer"></div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" name="user_name" placeholder="Your Name" required>
      <input type="email" name="user_email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MR__ YOGA | All rights reserved</p>
  </footer>

  <!-- Scripts -->
  <script>
    // Quiz Script
    const quizData = [
      { question: "What does HTML stand for?", a: "Hyper Text Markup Language", b: "High Text Markup Language", c: "Hyperlinks and Text Markup Language", d: "Home Tool Markup Language", correct: "a" },
      { question: "Which language is used for styling web pages?", a: "HTML", b: "JQuery", c: "CSS", d: "XML", correct: "c" },
      { question: "Which is not a JavaScript Framework?", a: "React", b: "Angular", c: "Vue", d: "Django", correct: "d" },
      { question: "Which is used for database?", a: "PHP", b: "MySQL", c: "HTML", d: "CSS", correct: "b" }
    ];
    const quiz = document.getElementById("quizContainer");
    const answerEls = document.querySelectorAll(".answer");
    const questionEl = document.getElementById("question");
    const a_text = document.getElementById("a_text");
    const b_text = document.getElementById("b_text");
    const c_text = document.getElementById("c_text");
    const d_text = document.getElementById("d_text");
    const submitBtn = document.getElementById("submit");
    const resultEl = document.getElementById("result");
    let currentQuiz = 0;
    let score = 0;
    loadQuiz();
    function loadQuiz() {
      deselectAnswers();
      const currentQuizData = quizData[currentQuiz];
      questionEl.innerText = currentQuizData.question;
      a_text.innerText = currentQuizData.a;
      b_text.innerText = currentQuizData.b;
      c_text.innerText = currentQuizData.c;
      d_text.innerText = currentQuizData.d;
    }
    function getSelected() {
      let answer = undefined;
      answerEls.forEach((answerEl) => { if (answerEl.checked) { answer = answerEl.id; } });
      return answer;
    }
    function deselectAnswers() { answerEls.forEach((el) => el.checked = false); }
    submitBtn.addEventListener("click", () => {
      const answer = getSelected();
      if (answer) {
        if (answer === quizData[currentQuiz].correct) score++;
        currentQuiz++;
        if (currentQuiz < quizData.length) loadQuiz();
        else {
          quiz.innerHTML = `<h2 class="result">You answered correctly ${score}/${quizData.length} questions.</h2>
          <button onclick="location.reload()">Restart</button>`;
        }
      }
    });

    // Blog Script
    function loadPosts() {
      const postsContainer = document.getElementById("postsContainer");
      const posts = JSON.parse(localStorage.getItem("blogPosts")) || [
        { title: "First Blog Post", content: "This is a sample blog post stored in localStorage.", date: new Date() }
      ];
      postsContainer.innerHTML = "";
      posts.reverse().forEach(post => {
        const postEl = document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML = `
          <h2>${post.title}</h2>
          <small>${new Date(post.date).toLocaleString()}</small>
          <p>${post.content}</p>
        `;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>
