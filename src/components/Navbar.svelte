
<section>
  <div class="wrapper">
    <div class="discover-btn">DISCOVER</div>

    <div class="link-wrapper">
      <a href="/#about">ABOUT ME</a>
      <a href="/#">FLY HOME</a>
      <a href="/#projects">PROJECTS</a>
    </div>
  </div>
</section>

<style lang="scss">
  @import "src/_variables";
  section {
    display: flex;
    justify-content: center;
  }
  .wrapper {
    position: fixed;
    height: fit-content;
    width: fit-content;
    bottom: 1.25em;

    &:hover {
      .link-wrapper {
        height: 2.5em;
        width: auto;
        opacity: 1;
        transform: scale(1.1, 1.1);
      }
      .discover-btn {
        width: 0;
        height: 0;
        opacity: 0;
        transform: scale(1.1, 1.1);
      }
    }
  }
  .discover-btn {
    border-radius: 9999px;
    display: block;
    width: 12em;
    height: 2.5em;
    opacity: 1;
    overflow: hidden;
    background: $space-white;
    color: $space-black;
    display: flex;
    justify-content: center;
    font-family: $display;
    align-items: center;
    transition: opacity 0.9s ease-out, transform 0.5s linear;
    transition-delay: 50ms;

  }
  .link-wrapper {
    grid-template-columns: repeat(3, minmax(0, 1fr));
    background: $space-white;
    border-radius: 9999px;
    align-items: center;
    display: grid;
    height: 0;
    width: 0;
    opacity: 0;
    overflow: hidden;
    transition: opacity 0.4s ease, transform 0.4s ease-out;
    transition-delay: 50ms;
  }
  a {
    font-family: $display;
    color: $space-black;
    margin: 0 0.25em 0 0.25em;
    padding: 0 1.25em 0 1.25em;
    line-height: 1.75em;

    &:hover {
      color: $launch-red;
      transition-property: color;
      transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
      transition-duration: 150ms;
    }
  }
</style>
