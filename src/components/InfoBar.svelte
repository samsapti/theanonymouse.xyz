<script lang="ts">
  import github from "../assets/github-logo.svg";
  import license from "../assets/cc-logo.svg";
</script>

<div>
  <span>
    Source code is available on
    <a
      target="_blank"
      href="https://github.com/theanonymousexyz/theanonymouse.xyz"
    >
      GitHub
      <img src={github} alt="GitHub logo" />
    </a>
  </span>
  <span>
    Licensed under
    <a target="_blank" href="https://creativecommons.org/licenses/by-nc-sa/4.0">
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

  div {
    background-color: $primary;
    display: flex;
    justify-content: center;
  }

  span {
    color: $white;
    font-size: 1rem;
    margin: 0.5em;

    a {
      text-decoration: none;
      color: $accent3;
    }

    img {
      height: 1em;
    }
  }
</style>
