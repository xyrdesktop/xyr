      }
      #starfield {
        position# Hi, I'm KATX

> **Lathe & Shaper IRL**  
> **Code & Editing in the Matrix**  
> Lathe pro. Code geek. #TechMeetsMetal

---

<div align="center">
  <a href="mailto:katxmandu@duck.com">
    <img src="https://img.shields.io/badge/email-rojanthapa27%40gmail.com-blue?logo=gmail" alt="Email"/>
  </a>
  <a href="https://twitter.com/rojanthapa27">
    <img src="https://img.shields.io/badge/twitter-@rojanthapa27-1da1f2?logo=twitter" alt="Twitter"/>
  </a>
  <a href="https://github.com/xyrdesktop">
    <img src="https://img.shields.io/badge/github-xyrdesktop-333?logo=github" alt="GitHub"/>
  </a>
  <a href="https://nso.group/@xyrdesktop">
    <img src="https://img.shields.io/badge/mastodon-xyrdesktop-6364ff?logo=mastodon" alt="Mastodon"/>
  </a>
  <a href="https://www.linkedin.com/in/rojanthapa">
    <img src="https://img.shields.io/badge/linkedin-rojanthapa-blue?logo=linkedin" alt="LinkedIn"/>
  </a>
</div>

---

> _"... he was wise, but was not. As a result, I became hateful to him and to many of those present; and so, as I went away, I thought to myself, ‘I am wiser than this man: neither of us probably knows anything worthwhile, but he thinks he knows something when he does not, whereas when I do not know, neither do I think I know; so I am likely to be wiser than he to this small extent, that I do not think I know what I do not know.’"_

---

<div align="center">

© 1998-2025 — Some rights reserved.

</div>

 absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1; /* Ensures starfield is behind other content */
      }
      .fa-brands {
        font-size: 64px;
        width: 64px;
        text-align: center;
        text-decoration: none;
        margin: 5px 2px;
        border-radius: 50%;
      }
      .fa-brands:hover {
        opacity: 0.7;
      }
      #footer {
        position: absolute;
        bottom: 10px;
        width: 100%;
        text-align: center;
        font-size: 14px;
        color: #ecf0f1;
        z-index: 10; /* Ensure footer is above starfield */
      }

      /* Media Queries for responsiveness */
      @media (max-width: 1200px) {
        #title {
          font-size: 60px;
        }
        h2 {
          font-size: 16px;
        }
        #supersmall {
          font-size: 12px;
          max-width: 80%;
        }
        .fa-brands {
          font-size: 50px;
          width: 50px;
        }
      }

      @media (max-width: 800px) {
        #title {
          font-size: 50px;
        }
        h2 {
          font-size: 14px;
        }
        #supersmall {
          font-size: 12px;
          max-width: 90%;
        }
        .fa-brands {
          font-size: 40px;
          width: 40px;
        }
      }

      @media (max-width: 600px) {
        #overlay {
          margin-left: 10%;
          margin-top: 5%;
        }
        #title {
          font-size: 40px;
        }
        h2 {
          font-size: 12px;
        }
        #supersmall {
          font-size: 10px;
          max-width: 100%;
        }
        .fa-brands {
          font-size: 30px;
          width: 30px;
        }
      }

    </style>
  </head>
  <body>
    <div id="container">
      <canvas id="starfield"></canvas>
      <div id="overlay">
        <h1 id="title">Hi, I'm KATX.</h1>
        <h2>Lathe & Shaper IRL, Code & Editing in the Matrix,</h2>
        <h2>Lathe pro. Code geek. #TechMeetsMetal.</h2>
        <h2><i class="fa-sharp fa-solid fa-envelope"></i> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e39b9a9187869088978c93a387968088cd808c8e">[email&#160;protected]</a></h2>
        <a href="https://twitter.com/rojanthapa27" class="fa-brands fa-twitter"></a>
        <a href="https://github.com/xyrdesktop" class="fa-brands fa-github"></a>
        <a rel="me" href="https://nso.group/@xyrdesktop" class="fa-brands fa-mastodon"></a>
        <a href="https://www.linkedin.com/in/rojanthapa" class="fa-brands fa-linkedin"></a>
        <div id="supersmall"><p style="margin: 0px;">"... he was wise, but was not. As a result, I became hateful to him and to many of those present; and so, as I went away, I thought to myself, ‘I am wiser than this man; for neither of us really knows anything fine and good, but this man thinks he knows something when he does not, whereas I, as I do not know anything, do not think I do either. I seem, then, in just this little thing to be wiser than this man at any rate, that what I do not know I do not think I know either.’ From him I went to another of those who were reputed"<br><small>— Plato, Apology</small></p></div>
      </div>
    </div>
    <!-- Footer with copyright notice -->
    <div id="footer">
      © 1998-2025. Some rights reserved.
    </div>
    <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script>
    <script type="text/javascript">
      const canvas = document.getElementById('starfield');
      const ctx = canvas.getContext("2d");

      var body = document.body,
          html = document.documentElement;

      var height = Math.max(body.scrollHeight, body.offsetHeight,
                           html.clientHeight, html.scrollHeight, html.offsetHeight);

      canvas.width = window.innerWidth;
      canvas.height = height;

      function random(min, max) {
        return min + Math.random() * (max + 1 - min);
      }

      window.addEventListener('resize', function() {
        height = Math.max(body.scrollHeight, body.offsetHeight, html.clientHeight, html.scrollHeight, html.offsetHeight);
        canvas.width = window.innerWidth;
        canvas.height = height;
        generateStars();
      });

      function generateStars() {
        const pagesize = canvas.width * canvas.height;
        const stars = pagesize / 2000;

        ctx.clearRect(0, 0, canvas.width, canvas.height); // Clear canvas before redrawing
        
        for (let i = 0; i < stars; i++) {
          let x = random(2, canvas.width - 2);
          let y = random(2, canvas.height - 2);
          let alpha = random(0.5, 1);
          let size = random(1, 2);
          ctx.fillStyle = '#ffffff';
          ctx.globalAlpha = alpha;
          ctx.fillRect(x, y, size, size);
        }
      }

      generateStars();
    </script>
  </body>
</html>
