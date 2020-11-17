<script>
</script>

<style lang="scss">
  #about {
    min-height: 70vh;
    position: relative;
    z-index: 10;
  }

  .about-title {
    text-align: center;
    font-size: 42px;
    font-family: var(--main-font);
    letter-spacing: 2px;
  }

  .description-container {
    column-count: 2;
    margin-top: 105px;
    padding: 0 50px;
  }

  p {
    font-size: 18px;
    text-align: left;
    font-family: var(--main-font);
    line-height: 3;
  }

  .coders-link {
    position: relative;

    &:before {
      content: "";
      height: 2px;
      width: 100%;
      position: absolute;
      bottom: 0;
      background-color: #f5ed51;
    }
  }

  @media (max-width: 660px) {
    .about-title {
      font-size: 34px;
    }

    .description-container {
      column-count: 1;
    }

    p {
      font-size: 15px;
      text-align: center;
    }
  }

  .underline {
    position: relative;

    &::before {
      content: "";
      position: absolute;
      bottom: 0;
      height: 50%;
      width: 100%;
      background-color: #6494aa;
      z-index: -1;
    }
  }

  @media (max-width: 600px) {
    .description-container {
      margin-top: 40px;
    }
  }
</style>

<section id="about">
  <h3 class="about-title"><span class="underline">About me</span></h3>
  <div class="description-container">
    <p>
      I'm 21 years old student living in Poland. I've always been curious about
      coding but I took the first step 3 years ago and started to learn basics
      of C++. As a beginner I wanted to see effects of my works so I decided to
      find out how are websites made. As I decided so I did. I turned on the
      tutorial on YouTube and started learning. In mid-2019 I realized that
      programming interests me more and more and gives me a lot of satisfaction
      so I decided to start a 8 months course at
      <a
        class="coders-link"
        href="https://coderslab.pl/pl/kurs/javascript-developer-react/o-kursie">CodersLab</a>.
      This course, despite a huge dose of knowledge, gave me further motivation
      and desire to learn web development. After completing the course, I mainly
      focused on learning React and the basics of back-end technologies.
    </p>
  </div>
</section>
