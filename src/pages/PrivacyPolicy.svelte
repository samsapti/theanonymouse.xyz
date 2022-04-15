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
      discarded immediately, meaning no IP addresses, no timestamps, no nothing.
    </p>
    <p>
      The hosting provider of this website is
      <a href="https://www.hetzner.com/">Hetzner Online GmbH</a>. According to
      their privacy policy, they do not store any log data about what is sent
      and received to/from the server hosting this site. The only thing that
      displayed to the server administrator (me) is general metrics, such as
      overall time-based usage of memory, processing power, network bandwidth,
      etc. This is strictly non-identifiable information. Please refer to their
      privacy policy if this concerns you.
    </p>
    <p>
      Furthermore, this website and the public services are hosted in Germany.
      This means that all data regarding the site and services are stored inside
      the EU with an EU-based hosting provider. Therefore, the
      <a href="https://www.nsa.gov/Signals-Intelligence/FISA/">
        Foreign Intelligence Surveillance Act (FISA)
      </a>
      does not apply to this website and the public services.
    </p>
    <p>
      Regarding SearX, keep in mind that it is a metasearch engine (meaning it
      sends your search query to other search engines and gets results from
      them), so I am not responsible for what the upstream search engines store
      in terms of search queries, timestamps, etc. You can see the enabled
      search engines in the settings, and optionally change them. Please refer
      to their individual privacy policies.
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
    <p>None of that is used here.</p>
    <p>
      The only exception is that your color theme preference is stored in your
      browser's local storage if you change it from the default. This might
      confusingly be shown to you as "Cookies" in your browser, but it is not.
      It should also be mentioned, that this is not required for the website to
      function, but it is required to persist your color theme preference.
    </p>
    <p>
      SearX might also store some cookies, but only if you change the settings
      from the default. These are strictly used to store settings, and are also
      not required. SearX settings can also be stored in a custom URL if you
      prefer.
    </p>
  </div>
  <div class="section">
    <h2>Changes to this privacy policy</h2>
    <p>
      I reserve the right to update this privacy policy as needed, at any given
      time. By browsing my website and using my services, you agree with the
      version of this privacy policy at that given time. The date at the bottom
      will always reflect the last date this privacy policy was updated.
    </p>
    <p>
      If this privacy policy changes substantially, I will put a clear banner on
      the front page for a period of at least 30 days.
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
