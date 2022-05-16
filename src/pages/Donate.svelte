<script lang="ts">
  import xmr from "../assets/xmr-qr.png";
  import btc from "../assets/btc-qr.png";
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
    <h3>Full wallet address</h3>
    <pre>
      86Z9Y7L17CEccLuTzjD1GG49TWLpdDs8dhm49GFwLzppb6iaqPmV6gp1sqJXybBnuRhPDAmt6Mn9rGFVzonBASsQCb7BxaV
    </pre>
    <h3>OpenAlias</h3>
    <pre>
      xmr.donate.theanonymouse.xyz
    </pre>
    <h3>QR code</h3>
    <img src={xmr} alt="XMR address embedded in a QR code" />
  </div>
  <div class="section">
    <h2>Bitcoin (BTC)</h2>
    <h3>Full wallet address</h3>
    <pre>
      bc1q4vwx8kdf7rg7p4yt33ly6kp5cec6nw8ed8xmsc
    </pre>
    <h3>OpenAlias</h3>
    <pre>
      btc.donate.theanonymouse.xyz
    </pre>
    <h3>QR code</h3>
    <img src={btc} alt="BTC address embedded in a QR code" />
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
    margin: 20px auto 50px;
    border-radius: 12px;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  h2 {
    color: $accent2;
    font-size: 2rem;
    margin: 1rem auto;
  }

  h3 {
    font-size: 1.5rem;
    margin: 0.5rem auto;
  }

  p {
    font-size: 1em;
  }

  pre {
    background-color: $black;
    color: $secondary;
    white-space: pre-line;
    white-space: nowrap;
    overflow-x: auto;
    border-radius: 5px;
    padding: 12px;
    margin: 8px 0;
    font-family: "Fira Code", "Roboto Mono", Consolas, monospace;
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

    h3 {
      font-size: 4vw;
    }

    p,
    pre {
      font-size: 3vw;
    }
  }
</style>
