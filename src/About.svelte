<script lang="ts">
  import src from "./assets/theanonymouse.png";

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
      Test test test test test test test test test test test test test test test test test test test test test test test test test test
       test test test test test test test test test test test test test test test test test test test test test test
    </p>
  </div>
</div>

<style lang="scss">
  @import "./colors.scss";

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
  }

  h1 {
    color: $orange;
    font-size: 3rem;
    margin: 3rem auto;
    max-width: 14rem;
  }

  h2 {
    color: $darkorange;
    font-size: 2rem;
    max-width: 75%;
  }

  p {
    max-width: 14rem;
    line-height: 1.15;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
