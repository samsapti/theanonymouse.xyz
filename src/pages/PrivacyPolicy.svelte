<div id="content">
  <h1>Privacy Policy</h1>
  <p class="note">
    <em>
      This privacy policy applies to this website, as well as any of the public
      services mention in the
      <a href="#about">about page</a>.
    </em>
  </p>
  <div class="section">
    <h2>Data collection and retention</h2>
    <p>
      Absolutely no data is collected. Even the logs on the webserver are
      discarded, meaning no IP addresses, no timestamps, no nothing.
    </p>
    <p>
      Regarding SearX, keep in mind that it is a metasearch engine (meaning it
      sends your search query to other search engines and gets results from
      them), so I am not responsible for what the upstream search engines store
      in terms of search queries, timestamps, etc.
    </p>
  </div>
  <div class="section">
    <h2>Embedded content and third party tracking</h2>
    <p>There is no embedded content on this website.</p>
    <p>
      On SearX, search results are filtered and sanitized for tracking content
      with a piece of software called
      <a href="https://github.com/asciimoo/morty">Morty</a>. In short, I use the
      default settings in the
      <a href="https://github.com/searx/searx-docker">SearX Docker setup</a>,
      which are optimized for privacy.
    </p>
  </div>
  <div class="section">
    <h2>Cookies, analytics, etc.</h2>
    <p>None of that is used here. After all, I am here to promote privacy.</p>
  </div>
  <div class="section">
    <h2>Changes to this privacy policy</h2>
    <p>
      I reserve the right to update this privacy policy as needed, at any given
      time. By browsing my website and using my services, you agree with the
      version of this privacy policy at that given time. As I store no
      information about the users of this site and my services, I am also unable
      to notify you directly of any changes. The date at the bottom will always
      reflect the last date this privacy policy was updated.
    </p>
  </div>
  <p class="note">
    <em>This privacy policy was last updated on April 15, 2022.</em>
  </p>
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

  .note {
    margin: 20px 0;
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

  p {
    font-size: 1em;
  }

  .section {
    line-height: 1.5;
    width: 80vw;
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
      padding: 0;
    }

    h1 {
      font-size: 10vw;
    }

    p {
      font-size: 3vw;
    }

    .section h2 {
      font-size: 6vw;
    }
  }
</style>
