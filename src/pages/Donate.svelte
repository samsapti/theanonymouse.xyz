<script lang="ts">
  import src from "../assets/xmr-qr.png";
</script>

<div id="content">
  <h1>Donations</h1>
  <p class="note">
    <em>
      If you want to support me, I will happily accept anything sent through the
      below donation methods.
    </em>
  </p>
  <div class="section">
    <h2>Monero (XMR)</h2>
    <p>My XMR address is:</p>
    <pre>
      86Z9Y7L17CEccLuTzjD1GG49TWLpdDs8dhm49GFwLzppb6iaqPmV6gp1sqJXybBnuRhPDAmt6Mn9rGFVzonBASsQCb7BxaV
    </pre>
    <p>OpenAlias is also an option:</p>
    <pre>
      xmr.donate.theanonymouse.xyz
    </pre>
    <p>You can also scan this QR code:</p>
    <img {src} alt="XMR address embedded in a QR code" />
  </div>
</div>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  #content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0;
    padding: 0;
  }

  .section {
    line-height: 1.5;
    width: 80vw;
    max-width: 720px;
  }

  img {
    display: block;
    max-width: 250px;
    width: 50%;
    margin: 25px auto;
    border-radius: 12px;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  p {
    font-size: 1em;
  }

  pre {
    background-color: $black;
    color: $white;
    white-space: pre-line;
    white-space: nowrap;
    overflow-x: auto;
    border-radius: 5px;
    padding: 12px;
    margin: 8px 0;
    font-family: "Fira Code", "Roboto Mono", Consolas, monospace;
  }

  h2 {
    color: $accent2;
    font-size: 2rem;
    margin: 1rem auto;
  }

  ::-webkit-scrollbar {
    height: 5px;
  }

  ::-webkit-scrollbar-track {
    background: $black;
  }

  ::-webkit-scrollbar-thumb {
    background: $primary;
    border-radius: 2px;
  }

  ::-webkit-scrollbar-thumb:hover {
    background: $accent3;
  }

  // Responsive
  @media (max-width: 480px) {
    #content {
      padding: 0 5%;
    }

    .section {
      width: 80vw;
    }

    h1 {
      font-size: 10vw;
    }

    h2 {
      font-size: 6vw;
    }

    p,
    pre {
      font-size: 3vw;
    }
  }
</style>
