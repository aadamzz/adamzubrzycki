<script>
  let windowWidth = window.innerWidth;

  window.addEventListener("resize", () => {
    windowWidth = window.innerWidth;
  });
</script>

<style lang="scss">
  #projects {
    margin-bottom: 50px;
  }

  .projects-title {
    text-align: center;
    font-size: 42px;
    font-family: var(--main-font);
    margin-bottom: 40px;
    letter-spacing: 3px;
  }

  .projects-grid {
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    width: 80%;
    min-height: 700px;
    justify-content: center;
    border: 3px solid black;
    border-radius: 20px;
    overflow: hidden;
  }

  .project {
    display: grid;
    grid-template-columns: repeat(1fr);
    grid-template-rows: repeat(2, 1fr);
    align-items: center;
    justify-content: center;
    transition: 0.3s;
    flex-direction: column;
  }

  .project:hover {
    background-color: #0d0d0d;
    color: white;
  }

  .first,
  .second {
    grid-row: 1 / 2;
    border-bottom: 2px solid black;
  }

  .first,
  .third {
    border-right: 2px solid black;
  }

  .third,
  .forth {
    grid-row: 2 / 4;
  }

  .project-name {
    font-family: var(--main-font);
    text-align: center;
    font-size: 24px;
    margin-bottom: 20px;
    letter-spacing: 2px;
    line-height: 1.5;
  }

  .project-description {
    font-size: 18px;
    font-family: var(--main-font);
    text-align: center;
    line-height: 1.5;
    padding: 0 10px;
  }

  .wrapper-a {
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  .more-details {
    font-family: var(--main-font);
    font-size: 16px;
    position: relative;

    &:before {
      content: "";
      width: 100%;
      height: 2px;
      background-color: white;
      position: absolute;
      bottom: 0;
      transition: 0.3s;
    }

    &:hover:before {
      background-color: #f5ed51;
    }
  }

  .wrapper-b {
    display: flex;
    width: 100%;
    justify-content: space-evenly;
  }

  .links {
    position: relative;
    letter-spacing: 2px;

    &:before {
      content: "";
      height: 2px;
      width: 100%;
      position: absolute;
      bottom: 0;
      background-color: #f5ed51;
    }
  }

  @media (max-width: 800px) {
    .projects-grid {
      grid-template-rows: repeat(4, 1fr);
      grid-template-columns: 1fr;
    }
    .project:not(.forth) {
      grid-column: 1 / 2;
      border: none;
      border-bottom: 2px solid black;
    }
    .first {
      grid-row: 1 / 2;
    }
    .second {
      grid-row: 2 / 3;
    }
    .third {
      grid-row: 3 / 4;
    }
    .forth {
      grid-row: 4 / -1;
    }
    .project-name {
      font-size: 22px;
    }

    .project-description {
      font-size: 16px;
    }

    .more-details {
      font-size: 14px;
    }
    .projects-title {
      font-size: 32px;
    }
    .project-name {
      margin: 20px;
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
</style>

<main id="projects">
  <h5 class="projects-title"><span class="underline">My projects</span></h5>
  <section class="projects-grid">
    <article class="project first">
      <div class="wrapper-a">
        <h4 class="project-name">Recipe App - PWA</h4>
        <p class="project-description">
          Simple app that allows you to add your favorite recipe. Made using
          MERN stack and Progressive Web App. New Features comming soon.
        </p>
      </div>
      <div class="wrapper-b">
        <a href="https://github.com/aadamzz/" class="more-details">Github</a>
        <a
          href="https://dazzling-perlman-f5479e.netlify.app/"
          class="more-details">Live</a>
      </div>
    </article>
    <article class="project second">
      <div class="wrapper-a">
        <h4 class="project-name">NASA API</h4>
        <p class="project-description">
          Made using vanilla JavaScript as an exercise ogranized during the
          course by
          <a class="links" href="https://coderslab.pl/pl/">CodersLab</a>. App
          allows you to search for NASA photos. Web appearance designed by
          myself.
        </p>
      </div>
      <div class="wrapper-b">
        <a
          href="https://github.com/aadamzz/NASA-API-Challange"
          class="more-details">Github</a>
        <a
          href="https://nasa-api-challange.vercel.app/"
          class="more-details">Live</a>
      </div>
    </article>
    <article class="project third">
      <div class="wrapper-a">
        {#if windowWidth > 420}
          <h4 class="project-name">Coding challange - React</h4>
        {:else}
          <h4 class="project-name">Coding challange React</h4>
        {/if}
        <p class="project-description">
          Coding challange invented by
          <a
            class="links"
            href="https://www.frontendmentor.io/challenges/rest-countries-api-with-color-theme-switcher-5cacc469fec04111f7b848ca">Frontend
            mentor</a>
          made using React. App allows you to search for information about
          countries.
        </p>
      </div>
      <div class="wrapper-b">
        <a
          href="https://github.com/aadamzz/coding-challange-react"
          class="more-details">Github</a>
        <!-- <a href="#" class="more-details">Live</a> -->
      </div>
    </article>
    <article class="project forth">
      <div class="wrapper-a">
        <h4 class="project-name">Restaurant template</h4>
        <p class="project-description">
          Restaurant website designed by myself.
        </p>
      </div>
      <div class="wrapper-b">
        <a
          href="https://github.com/aadamzz/restaurant-template"
          class="more-details">Github</a>
        <a
          href="https://wizardly-dubinsky-115ada.netlify.app/"
          class="more-details">Live</a>
      </div>
    </article>
  </section>
</main>
