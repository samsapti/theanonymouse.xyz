<script lang="ts">
  import src from "../assets/profile.png";

  export let name: string;
</script>

<div id="content">
  <div id="profile">
    <img {src} alt="{name} profile" />
    <h1>Hello from {name}!</h1>
  </div>
  <div id="about-me">
    <h2>Who am I?</h2>
    <p>
      I'm a Software Development student from Denmark and a Privacy & Security
      advocate. I fight for online privacy, and I support open source,
      privacy-enhancing projects and software, and other tools to help people
      evade surveillance capitalism on the internet.
    </p>
    <p>
      I develop primarily Free/Libre & Open Source Software (FLOSS), and I also
      frequently contribute to other FLOSS. You can see what I'm currently
      working on over on my
      <a href="https://github.com/theanonymousexyz">GitHub profile</a>.
    </p>
    <p>
      For contact info, see the <a href="#contact">contact</a> page.
    </p>
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

  h2 {
    color: $accent2;
    font-size: 2rem;
    max-width: 75%;
  }

  #about-me {
    line-height: 1.5;
  }
</style>
