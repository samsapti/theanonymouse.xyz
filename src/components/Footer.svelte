<script lang="ts">
  import github from "../assets/github-logo.svg";
  import license from "../assets/cc-logo.svg";
</script>

<div id="content">
  <span>
    Source code is available on
    <a href="https://github.com/theanonymousexyz/theanonymouse.xyz">
      GitHub
      <img src={github} alt="GitHub logo" />
    </a>
  </span>
  <span>
    Licensed under
    <a href="https://creativecommons.org/licenses/by-nc-sa/4.0">
      CC BY-NC-SA 4.0
      <img
        src={license}
        alt="Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International"
      />
    </a>
  </span>
</div>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  #content {
    background-color: $primary;
    display: flex;
    justify-content: center;
  }

  span {
    color: $white;
    font-size: 0.8rem;
    text-align: center;
    margin: 0.5em;
  }

  a {
    text-decoration: none;
    color: $accent3;
  }

  img {
    height: 1em;
  }

  @media (max-width: 480px) {
    #content {
      flex-direction: column;
      align-items: center;
    }

    span {
      margin: 0.2em;
      font-size: 2.5vw;
    }
  }
</style>
