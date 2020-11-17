<script>
  import Hamburger from "./Hamburger.svelte";
  let mail = false;

  let windowWidth = window.innerWidth;

  window.addEventListener("resize", () => {
    windowWidth = window.innerWidth;
  });

  const showMail = () => {
    mail = true;
  };
</script>

<style lang="scss">
  #header {
    width: 100%;
    height: 75px;
    display: flex;
    position: relative;
  }

  .contact-me_container {
    flex-grow: 1;
    height: 100%;
    display: flex;
    align-items: center;
    position: relative;

    a {
      outline: none;
    }

    h1 {
      font-size: 40px;
      margin-left: 170px;
      font-family: var(--contact-me-font);
      font-weight: bold;
      width: 100%;
      position: absolute;
      top: 50%;
      left: 50%;

      transform: translate(-50%, -50%);

      &:focus {
        outline: 1px dotted;
      }
    }
    .email {
      font-size: 28px;
      text-decoration: underline;
    }
  }

  #navigation {
    flex-grow: 1;
    height: 100%;

    .navigation-list {
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }

  .navigation-list {
    li {
      font-size: 20px;
      margin: 0 10px;
      position: relative;
      font-family: "Kumbh Sans", sans-serif;

      &:before {
        transition: 0.3s;
        content: "";
        height: 1px;
        width: 0;
        height: 2px;
        position: absolute;
        bottom: 9px;
        background-color: black;
        cursor: pointer;
      }

      &:hover:before {
        content: "";
        width: 100%;
        height: 2px;
        position: absolute;
        background-color: white;
        bottom: 9px;
      }
    }
  }

  @media (max-width: 950px) {
    #navigation {
      flex-grow: 0;
      padding-right: 20px;
    }
  }
</style>

{#if windowWidth >= 880}
  <header id="header">
    <div class="contact-me_container">
      <a href="#contact">
        <h1 on:click={() => showMail()}>
          {#if !mail}
            mail me
          {:else if mail}
            <a
              class="email"
              href="mailto:az.zubrzycki99@gmail.com">az.zubrzycki99@gmail.com</a>
          {/if}
        </h1>
      </a>
    </div>
    <nav id="navigation">
      <ul class="navigation-list">
        <li><a href="#about">About me</a></li>
        <li><a href="#stack">Technologies</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#footer">Contact</a></li>
      </ul>
    </nav>
  </header>
{:else}
  <Hamburger {mail} on:click={() => showMail()} />
{/if}
