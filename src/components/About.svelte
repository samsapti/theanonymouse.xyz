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
    <ul>
      <li>Software Development student</li>
      <li>Privacy & Security Advocate</li>
    </ul>
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
