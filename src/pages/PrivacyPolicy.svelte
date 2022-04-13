<div id="content">
  <h1>Privacy Policy</h1>
  <div class="section">
    <h2>On this website</h2>
    <h3>What data is collected?</h3>
    <p>Absolutely nothing.</p>
    <h3>For how long is it kept?</h3>
    <p>No data is kept.</p>
    <h3>What about embedded content?</h3>
    <span>
      Currently only one image is sourced from
      <a href="https://fsf.org">fsf.org</a>. Please read their privacy policy if
      this is something that concerns you.
    </span>
  </div>
  <div class="section">
    <h2>SearX</h2>
    <h3>What data is collected?</h3>
    <p>Absolutely nothing.</p>
    <h3>For how long is it kept?</h3>
    <p>No data is kept.</p>
    <h3>What about embedded content?</h3>
    <p>There is no embedded content.</p>
  </div>
</div>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  #content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 15%;
  }

  a {
    color: $accent3;
    text-decoration: none;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  .section {
    line-height: 1.5;

    h2 {
      color: $accent2;
      font-size: 2rem;
      margin: 1rem auto;
    }

    p,
    span {
      font-size: 1em;
    }
  }

  // Responsive
  @media (max-width: 480px) {
    #content {
      padding: 0 5%;
    }

    h1 {
      font-size: 10vw;
    }

    .section {
      width: 80vw;
      
      h2 {
        font-size: 6vw;
      }

      p,
      span {
        font-size: 3vw;
      }
    }
  }
</style>
