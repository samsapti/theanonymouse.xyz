<script lang="ts">
  import src from "../assets/not-fd.svg";
</script>

<div id="content">
  <h1>Contact information</h1>
  <div class="section">
    <h2>Primary contact methods</h2>
    <p>Feel free to use any of the below contact methods:</p>
    <ul>
      <li>
        <span>
          Email:
          <a href="mailto:hello@theanonymouse.xyz">hello@theanonymouse.xyz</a>
        </span>
        <ul>
          <li>
            <span>
              PGP key:
              <a href="/pgp.asc">Here</a>,
              <a href="https://github.com/theanonymousexyz/pgp-public-key">
                here
              </a>
              or on your preferred keyserver
            </span>
          </li>
        </ul>
      </li>
      <li>
        <span>
          Mastodon:
          <a rel="me" href="https://ruby.social/@theanonymousexyz">
            @theanonymousexyz@ruby.social
          </a>
        </span>
      </li>
      <li>
        <span>
          Matrix:
          <a href="https://matrix.to/#/@4n0nym0u53:tchncs.de">
            @4n0nym0u53:tchncs.de
          </a>
        </span>
      </li>
    </ul>
  </div>
  <div class="section">
    <h2>Social media</h2>
    <p>I don't use that sh*t.</p>
    <a href="https://www.fsf.org/fb">
      <img {src} alt="Not f'd — you won't find me on Facebook" />
    </a>
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

  a {
    color: $accent3;
    text-decoration: none;
    padding: 0;
    margin: 0;
  }

  img {
    max-width: 80vw;
    margin: 0;
    padding: 0;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  p,
  span {
    font-size: 1em;
  }

  .section {
    line-height: 1.5;
    width: fit-content;
    max-width: 720px;

    h2 {
      color: $accent2;
      font-size: 2rem;
      margin: 1rem auto;
    }
  }

  // Responsive
  @media (max-width: 480px) {
    #content {
      padding: 0 5%;
    }

    img {
      width: 80vw;
      max-width: 720px;
    }

    h1 {
      font-size: 10vw;
    }

    p,
    span {
      font-size: 3vw;
    }

    .section {
      width: 80vw;

      h2 {
        font-size: 6vw;
      }
    }
  }
</style>
