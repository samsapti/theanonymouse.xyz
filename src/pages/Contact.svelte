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
        Email:
        <a rel="noopener noreferrer" href="mailto:hello@theanonymouse.xyz">
          hello@theanonymouse.xyz
        </a>
        <ul>
          <li>
            PGP key:
            <a href="/pgp.asc">Here</a>,
            <a
              rel="noopener noreferrer"
              href="https://github.com/theanonymousexyz/pgp-public-key"
            >
              here
            </a>
            or on your preferred keyserver
          </li>
          <li>
            PGP key fingerprint:
            <pre>FFFD8602E0E9E6D9E30EEBEEDFD39F412054CB84</pre>
          </li>
        </ul>
      </li>
      <li>
        Mastodon:
        <a
          rel="noopener noreferrer"
          href="https://ruby.social/@theanonymousexyz"
        >
          @theanonymousexyz@ruby.social
        </a>
      </li>
      <li>
        Matrix:
        <a
          rel="noopener noreferrer"
          href="https://matrix.to/#/@4n0nym0u53:tchncs.de"
        >
          @4n0nym0u53:tchncs.de
        </a>
      </li>
    </ul>
    <p>
      If you want to contact me securely, either use email with PGP encryption
      or Matrix. If you use Matrix, please verify my sessions:
    </p>
    <ul>
      <li>
        SchildiChat Desktop (Linux)
        <pre>
          Session ID: LVHNZUZIRO<br />
          Session key: tZfo CYjt chF6 IC5C uWjT drw3 4ytQ Eo+g 7F2p 5w5X MME
        </pre>
      </li>
      <li>
        SchildiChat Android
        <pre>
          Session ID: WWSKTPLQCN<br />
          Session key: kUE3 YP5b BgTS 2PaX 0AAH NxTU nrA0 x0+8 fDqq 9/vq IX4
        </pre>
      </li>
    </ul>
  </div>
  <div class="section">
    <h2>Social media</h2>
    <p>I don't use that sh*t.</p>
    <a rel="noopener noreferrer" href="https://www.fsf.org/fb">
      <img {src} alt="Not f'd — you won't find me on Facebook" />
    </a>
  </div>
  <div class="section">
    <h2>Community</h2>
    <p>
      Feel free to join my Matrix community, where you can chat with other
      people about everything privacy, security, FLOSS, or anything else in the
      off-topic room.
    </p>
    <ul>
      <li>
        Matrix space:
        <a
          rel="noopener noreferrer"
          href="https://matrix.to/#/#theanonymousexyz-privacy-space:tchncs.de"
        >
          #theanonymousexyz-privacy-space:tchncs.de
        </a>
      </li>
      <li>
        On-topic room:
        <a
          rel="noopener noreferrer"
          href="https://matrix.to/#/#theanonymousexyz-privacy-general:tchncs.de"
        >
          #theanonymousexyz-privacy-general:tchncs.de
        </a>
      </li>
      <li>
        Off-topic room:
        <a
          rel="noopener noreferrer"
          href="https://matrix.to/#/#theanonymousexyz-privacy-chat:tchncs.de"
        >
          #theanonymousexyz-privacy-chat:tchncs.de
        </a>
      </li>
    </ul>
  </div>
  <div class="section">
    <h2>How I protect my accounts</h2>
    <p>I take the following steps in order to protect my online accounts:</p>
    <ul>
      <li>
        All my accounts are protected by a randomly generated passphrase, that
        is usually 64 characters long, depending on whether the service supports
        that length.
      </li>
      <li>
        All my accounts are protected with 2FA if they support it. A FIDO U2F
        certified security key is used if supported by the service, otherwise
        TOTP is used.
      </li>
      <li>
        All my account credentials are stored in a password manager, that is
        protected by a strong passphrase and 2FA.
      </li>
    </ul>
  </div>
  <div class="section">
    <h2>How I protect my PGP key</h2>
    <p>I take the following steps in order to protect my private PGP key:</p>
    <ul>
      <li>
        My master key is stored on a hardware-encrypted storage medium, which is
        kept in a fireproof safe. The key itself is protected by a strong
        passphrase.
      </li>
      <li>
        My subkeys are stored on an OpenPGP smartcard that I always carry with
        me.
      </li>
      <li>
        My master key is never exposed to the internet. It is only ever accessed
        on an air gapped laptop, with no form of internet connectivity, no
        persistent storage medium, using a persistence-free live USB running
        <a rel="noopener noreferrer" href="https://tails.boum.org">Tails</a>.
      </li>
      <li>
        My subkeys are set to expire after at most 6 months, after which they
        are extended for another 6 months.
      </li>
      <li>
        My master key is set to expire after at most 2 years, after which it is
        extended for another 2 years.
      </li>
      <li>
        If my PGP keys are not extended before they expire, you should assume
        they have been compromised.
      </li>
      <li>
        If my PGP keys gets compromised, and I am able to, I will revoke them.
      </li>
      <li>
        My subkeys being compromised does not necessarily mean that my master
        key is compromised, as they are stored separately. If only the subkeys
        get compromised, I will only revoke those.
      </li>
      <li>
        I store a revocation certificate for the master key in a separate safe
        place, in case it is compromised.
      </li>
    </ul>
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
    margin: auto 0 25px auto;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 2rem auto;
  }

  p,
  li {
    font-size: 1em;
  }

  li {
    margin: 0.5em auto;
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

    li,
    p,
    pre {
      font-size: 3vw;
    }
  }
</style>
