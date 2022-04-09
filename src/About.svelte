<script lang="ts">
  import src from "./assets/theanonymouse.png";

  export let name: string;
</script>

<img {src} alt="{name} profile" />
<h1>Hello from {name}!</h1>
<p>Welcome to my website!</p>

<style lang="scss">
  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
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