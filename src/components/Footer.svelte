<script>
</script>

<style lang="scss">
  #footer {
    height: 100px;
    margin: 0 30px;
    position: relative;
    font-family: var(--main-font);
    display: flex;
    padding: 10px 0;
  }

  .footer-social_media-list {
    display: flex;
    flex-grow: 1;
    height: 100%;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
  }

  .footer-contact-list {
    display: flex;
    flex-grow: 1;
    height: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  ul {
    background-color: black;
    color: white;

    li {
      font-size: 16px;
    }
  }

  a {
    transition: color 0.2s;
  }

  a:hover {
    color: #f5ed51;
  }

  .mail:hover {
    color: #6494aa;
  }

  @media (max-width: 660px) {
    #footer {
      margin: 0;
      padding: 0 10px;
    }

    li {
      font-size: 14px;
    }
  }
</style>

<footer id="footer">
  <ul class="footer-social_media-list">
    <li><a href="https://github.com/aadamzz">Github</a></li>
    <li>
      <a
        href="https://www.linkedin.com/in/adam-zubrzycki-3766801a7/">LinkedIn</a>
    </li>
    <li>
      <a href="https://www.messenger.com/t/adam.zubrzycki.5">Messenger</a>
    </li>
  </ul>
  <ul class="footer-contact-list">
    <li><a class="mail" href="mailto:az.zubrzycki99@gmail.com">Mail me</a></li>
  </ul>
</footer>
