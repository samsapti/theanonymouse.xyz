<script lang="ts">
  import profile from "../assets/profile.png";
  import club512kb from "../assets/512kb-blue.svg";
</script>

<div id="content">
  <div id="profile">
    <img src={profile} alt="the_4n0nym0u53 profile" />
    <h1>Hello from the_4n0nym0u53!</h1>
  </div>
  <div class="section">
    <h2>Who I am</h2>
    <p>
      I am a Software Development student from Denmark and a privacy & security
      advocate. I fight for online privacy, and I support privacy enhancing
      projects and tools that help people stand against surveillance capitalism
      on the internet.
    </p>
  </div>
  <div class="section">
    <h2>What I do</h2>
    <p>
      I develop primarily Free/Libre & Open Source Software (FLOSS), and I also
      frequently contribute to other FLOSS projects. You can see what I'm
      currently working on over on my
      <a rel="noopener noreferrer" href="https://github.com/theanonymousexyz"
        >GitHub profile</a
      >.
    </p>
  </div>
  <div class="section">
    <h2>Public services</h2>
    <p>I have the following services available for public usage:</p>
    <ul>
      <li>
        <span>
          <a rel="noopener noreferrer" href="https://searx.theanonymouse.xyz"
            >SearX</a
          > - a privacy preserving metasearch engine
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
          <a
            rel="noopener noreferrer"
            href="https://mirror.theanonymouse.xyz/artix-linux/">mirror</a
          > for Artix Linux repository packages (it is in their mirrorlist)
        </span>
      </li>
    </ul>
    <p>
      <em>More services coming soon</em>
    </p>
  </div>
  <div id="club512kb" class="section">
    <a rel="noopener noreferrer" href="https://512kb.club/#512">
      <img src={club512kb} alt="512KB Club - Blue Team" />
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

  #profile {
    text-align: center;
    margin: 0;
    padding: 0;
  }

  #club512kb {
    text-align: center;
    margin: 50px auto auto;

    img {
      border-radius: 0;
      margin: 0;
      padding: 0;
    }
  }

  .section {
    line-height: 1.5;
    width: 80vw;
    max-width: 720px;
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

  h2 {
    color: $accent2;
    font-size: 2rem;
    margin: 1rem auto;
  }

  p,
  li {
    font-size: 1em;
  }

  li {
    margin: 0.5em auto;
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

    h2 {
      font-size: 6vw;
    }

    p,
    li {
      font-size: 3vw;
    }
  }
</style>
