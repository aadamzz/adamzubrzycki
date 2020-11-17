<script>
  let active = false;

  const toggleActive = () => {
    active = !active;
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
      margin-left: 70px;
      font-family: var(--contact-me-font);
      font-weight: bold;
      width: 100%;
      position: absolute;
      top: 50%;
      left: 50%;
      z-index: 10;

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

  .hamburger-icon_color {
    background: white;
  }

  .hamburger-icon-container {
    position: relative;
    cursor: pointer;
    width: 35px;
    height: 70px;
    margin-right: 20px;
    z-index: 10;
  }
  .hamburger-icon {
    transform: translateY(-50%);
  }
  .hamburger-icon,
  .hamburger-icon:before,
  .hamburger-icon:after {
    content: "";
    position: absolute;
    height: 4px;
    width: 100%;
    background: black;
    transition: all 0.2s ease;
  }

  .hamburger-icon {
    top: 50%;
  }

  .hamburger-icon:before {
    top: -200%;
  }

  .hamburger-icon:after {
    top: 200%;
  }

  .hamburger-active .hamburger-icon {
    transform: rotate(45deg) translate(-3px, -3px);
  }

  .hamburger-active .hamburger-icon:before,
  .hamburger-active .hamburger-icon:after {
    top: 0;
  }

  .hamburger-active .hamburger-icon:before {
    transform: rotate(90deg);
  }

  #navigation {
    position: absolute;
    height: 45vh;
    top: 75px;
    width: 100%;
    z-index: 1;
  }

  .navigation-list {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: column;
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%23000000' fill-opacity='0.05'%3E%3Cpath opacity='.5' d='M96 95h4v1h-4v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4h-9v4h-1v-4H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15v-9H0v-1h15V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h9V0h1v15h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9h4v1h-4v9zm-1 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm9-10v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-10 0v-9h-9v9h9zm-9-10h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9zm10 0h9v-9h-9v9z'/%3E%3Cpath d='M6 5V0H5v5H0v1h5v94h1V6h94V5H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");

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
</style>

<header id="header">
  <div class="contact-me_container">
    <h1><a class="email" href="mailto:az.zubrzycki99@gmail.com">mail me</a></h1>
  </div>
  <div
    on:click={() => toggleActive()}
    id="hamburger"
    class="hamburger-icon-container"
    class:hamburger-active={active}>
    <span class="hamburger-icon" />
  </div>
  {#if active}
    <nav id="navigation">
      <ul class="navigation-list">
        <li><a href="#about">About me</a></li>
        <li><a href="#stack">Technologies</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#footer">Contact</a></li>
      </ul>
    </nav>
  {/if}
</header>
