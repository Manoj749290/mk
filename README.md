<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <title>Student Multi-Project Website</title>
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif;}
    body {line-height: 1.6; background: #f9f9f9; color: #333;}

    header {background: #333; color: #fff; padding: 1rem; text-align: center;}
    nav {display: flex; justify-content: center; background: #444; flex-wrap: wrap;}
    nav a {color: white; padding: 1rem; text-decoration: none; text-align: center;}
    nav a:hover {background: #666;}

    section {padding: 2rem; max-width: 1000px; margin: auto;}
    h2 {margin-bottom: 1rem; text-align: center;}

    /* Portfolio */
    .hero {text-align: center; padding: 3rem; background: #eee;}
    .hero h1 span {color: darkblue;}
    .about-content {display: flex; flex-wrap: wrap; align-items: center; gap: 1rem;}
    .about-content img {max-width: 200px; border-radius: 8px;}
    .project-grid {display: grid; grid-template-columns: repeat(auto-fit,minmax(200px,1fr)); gap: 1rem;}
    .project-card {background: white; padding: 1rem; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); text-align: center;}

    /* Quiz */
    .quiz-container {background: white; padding: 20px; border-radius: 10px; max-width: 500px; margin: auto; box-shadow: 0 0 10px rgba(0,0,0,0.2);}
    .quiz-container ul {list-style: none; margin: 1rem 0;}
    .quiz-container li {margin: 10px 0;}
    .quiz-container button {background: #333; color: white; padding: 10px 15px; border: none; border-radius: 5px; cursor: pointer;}
    .quiz-container button:hover {background: #555;}
    .result {font-size: 18px; font-weight: bold; text-align: center;}

    /* Blog */
    .post {background: white; padding: 15px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1);}

    /* Responsive layout demo */
    .container {display: grid; grid-template-columns: 3fr 1fr; gap: 1rem;}
    .content,.sidebar {padding: 1rem; border-radius: 8px;}
    .content {background: #f4f4f4;}
    .sidebar {background: #e2e2e2;}
    @media(max-width:768px){.container{grid-template-columns:1fr;}}

    footer {text-align: center; background: #333; color: white; padding: 1rem; margin-top: 1rem;}
  </style>
</head>
<body>

  <header>
    <h1>Student Multi-Project Website</h1>
    <p>Portfolio | Quiz | Blog | Responsive Layout</p>
  </header>

  <nav>
    <a href="#home">Portfolio</a>
    <a href="#quiz">Quiz</a>
    <a href="#blog">Blog</a>
    <a href="#layout">Responsive Layout</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- Portfolio Section -->
  <section id="home" class="hero">
    <h1>Hello, I'm <span>MR__MANOJ KUMAR</span></h1>
    <p>I am the student</p>
    <a href="#projects">View My Work</a>
  </section>

  <section id="about" class="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG-20250904-WA0018.jpg" alt="Profile Photo">
      <p>I am a student enthusiastic about technology and design. I love building interactive, user-friendly web applications and exploring new tools in the tech world.</p>
    </div>
  </section>

  <section id="projects" class="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Project 1</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Project 2</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Project 3</h3><p>Personal blog with CMS.</p></div>
    </div>
  </section>

  <!-- Quiz Section -->
  <section id="quiz">
    <h2>Simple Quiz App</h2>
    <div class="quiz-container" id="quizBox">
      <h3 id="question">Question text</h3>
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

  <!-- Blog Section -->
  <section id="blog">
    <h2>My Blog</h2>
    <div class="container" id="postsContainer"></div>
  </section>

  <!-- Responsive Layout Section -->
  <section id="layout">
    <h2>Responsive Layout Demo</h2>
    <div class="container">
      <div class="content">
        <h3>Main Content</h3>
        <p>This is the main content area. Resize the window to see the responsive effect.</p>
      </div>
      <div class="sidebar">
        <h3>Sidebar</h3>
        <p>This is a sidebar with some extra information or links.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" id="name" name="user_name" placeholder="Your Name" required>
      <input type="email" id="email" name="user_email" placeholder="Your Email" required>
      <textarea id="message" name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <footer>
    <p>&copy; 2025 MR__MANOJ KUMAR| All Rights Reserved</p>
  </footer>

  <!-- Scripts -->
  <script>
    // Quiz Script
    const quizData = [
      {question:"Who is making the Web standards?",a:"Google",b:"Mozilla",c:"The World Wide Web Consortium",d:"Microsoft",correct:"c"},
      {question:"Choose the correct HTML element for the largest heading:",a:"<heading>",b:"<h6>",c:"<head>",d:"<h1>",correct:"d"},
      {question:"What is the correct HTML element for inserting a line break?",a:"<break>",b:"<lb>",c:"<br>",d:"<b>",correct:"c"},
      {question:"Which is used for database?",a:"PHP",b:"MySQL",c:"HTML",d:"CSS",correct:"b"}
    ];
    const questionEl=document.getElementById("question"),a_text=document.getElementById("a_text"),b_text=document.getElementById("b_text"),c_text=document.getElementById("c_text"),d_text=document.getElementById("d_text"),submitBtn=document.getElementById("submit"),resultEl=document.getElementById("result");
    const answerEls=document.querySelectorAll(".answer");let currentQuiz=0,score=0;loadQuiz();
    function loadQuiz(){deselectAnswers();const q=quizData[currentQuiz];questionEl.innerText=q.question;a_text.innerText=q.a;b_text.innerText=q.b;c_text.innerText=q.c;d_text.innerText=q.d;}
    function deselectAnswers(){answerEls.forEach(el=>el.checked=false);}
    function getSelected(){let ans;answerEls.forEach(el=>{if(el.checked){ans=el.id;}});return ans;}
    submitBtn.addEventListener("click",()=>{const ans=getSelected();if(ans){if(ans===quizData[currentQuiz].correct){score++;}currentQuiz++;if(currentQuiz<quizData.length){loadQuiz();}else{document.getElementById("quizBox").innerHTML=`<h3 class="result">You answered correctly ${score}/${quizData.length} questions.</h3><button onclick="location.reload()">Restart</button>`;}}});

    // Blog script
    function loadPosts() {
      const postsContainer=document.getElementById("postsContainer");
      const posts=[{title:"First Blog Post",content:"This is a sample blog post.",date:new Date()}];
      postsContainer.innerHTML="";
      posts.reverse().forEach(post=>{
        const el=document.createElement("div");
        el.classList.add("post");
        el.innerHTML=`<h3>${post.title}</h3><small>${new Date(post.date).toLocaleString()}</small><p>${post.content}</p>`;
        postsContainer.appendChild(el);
      });
    }
    loadPosts();
  </script>

</body>
</html>
