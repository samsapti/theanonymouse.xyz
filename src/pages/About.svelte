<script lang="ts">
  import src from "../assets/profile.png";
</script>

<div id="content">
  <div id="profile">
    <img {src} alt="the_4n0nym0u53 profile" />
    <h1>Hello from the_4n0nym0u53!</h1>
  </div>
  <div class="section">
    <h2>Who am I?</h2>
    <p>
      I'm a Software Development student from Denmark and a Privacy & Security
      advocate. I fight for online privacy, and I support open source,
      privacy-enhancing projects and software, and other tools to help people
      evade surveillance capitalism on the internet.
    </p>
  </div>
  <div class="section">
    <h2>What do I do?</h2>
    <p>
      I develop primarily Free/Libre & Open Source Software (FLOSS), and I also
      frequently contribute to other FLOSS projects. You can see what I'm
      currently working on over on my
      <a href="https://github.com/theanonymousexyz">GitHub profile</a>.
    </p>
  </div>
  <div class="section">
    <h2>Services I offer</h2>
    <p>I have the following services available for public usage:</p>
    <ul>
      <li>
        <span>
          <a href="https://searx.theanonymouse.xyz">SearX</a>
          - a privacy preserving metasearch engine
        </span>
      </li>
      <li>
        <span>
          A Tor obfs4 bridge which you can get access to by
          <a href="#contact">contacting me</a>
          (use one of the direct contact methods)
        </span>
      </li>
      <li>
        <span>
          A
          <a href="https://mirror.theanonymouse.xyz/artix-linux/">mirror</a>
          for Artix Linux repository packages (it is in their mirrorlist)
        </span>
      </li>
    </ul>
    <p>
      <em>More services coming soon</em>
    </p>
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

  #profile {
    text-align: center;
    margin: 0;
    padding: 0;
  }

  a {
    color: $accent3;
    text-decoration: none;
  }

  img {
    max-width: 14rem;
    border-radius: 50%;
    background-color: $secondary;
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

    img {
      width: 40vw;
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
