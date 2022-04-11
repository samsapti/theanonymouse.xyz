<script lang="ts">
  import src from "../assets/profile.png";

  export let name: string;
</script>

<div id="content">
  <div id="profile">
    <img {src} alt="{name} profile" />
    <h1>Hello from {name}!</h1>
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
    </ul>
    <em>More services coming soon</em>
  </div>
</div>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  #content {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 60%;
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
    height: 16rem;
    width: 16rem;
    border-radius: 50%;
    background-color: $secondary;
  }

  h1 {
    color: $accent1;
    font-size: 3rem;
    margin: 3rem auto;
  }

  .section {
    line-height: 1.5;

    h2 {
      color: $accent2;
      font-size: 2rem;
      margin: 1rem auto;
    }
  }
</style>
