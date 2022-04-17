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
          <a href="https://ruby.social/@theanonymousexyz">
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
    <p>
      If you want to contact me securely, either use email with PGP encryption
      or Matrix. If you use Matrix, please verify my sessions:
    </p>
    <ul>
      <li>
        <span>
          SchildiChat Desktop (Linux) - <code>LVHNZUZIRO</code>
        </span>
      </li>
      <li>
        <span>
          SchildiChat Android - <code>WWSKTPLQCN</code>
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
    display: block;
    width: 50%;
    max-width: 250px;
    margin: 50px 0 auto auto;
    margin-right: 0;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  p,
  code,
  span {
    font-size: 1em;
  }

  code {
    background-color: $accent3;
    border-radius: 3px;
    font-family: "Fira Code", "Roboto Mono", Consolas, monospace;
    padding: 0 3px;
  }

  .section {
    line-height: 1.5;
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
