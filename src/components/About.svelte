<script></script>

<section id="about">
    <h1>About Me</h1>
    <p class="blurb">
        Hi there! I am a current high schooler based in NYC with a passion for computer science and engineering,
        <br> creating things to both entertain and assist my community. Currently a board member on my school's robotics team,
        <br> assisting the next generation in discovering the beauty of STEM.
    </p>

    <h3>GET IN TOUCH!</h3>
    <div class="link-container">
    <div class="links">
        <a class="resume" href="/resume.pdf" target="_blank">Resume</a>
        <div>
            <a class="icons" href="mailto: 47isaacw@gmail.com" target="_blank"><i class="fa-solid fa-envelope fa-3x" /></a>
            <a class="icons" href="https://github.com/the-eyesack" target="_blank"><i class="fa-brands fa-github fa-3x" /></a>
        </div>
    </div>
    </div>

</section>
<style lang="scss">
  @import "src/variables";
    section {
      width: 100vw;
      height: 100vh;
    }
  h3 {
    text-align: center;
    margin: 2em 0 0.5em 0;
    font-size: x-large;
    font-family: $display
  }
  .link-container {
    display: flex;
    justify-content: center;
  }
  .links {
    display: inline-block;
    margin: 0 0.5em 0.5em 0.5em;
    padding: 0.5em 2.5em 0.5em 2.5em;
    border: 0.25rem solid $launch-red;
    border-radius: 1rem;
    div {
      display: flex;
      justify-content: center;
    }
    .resume {
      text-align: center;
      display: block;
      font-size: 1.2rem;
      font-family: $display
    }
    a {
      color: white;
      margin: 0 0.5em 0.5em 0.5em;


      &:hover {
        color: $dark-purple
      }
    }
  }

  .blurb {
    display: block;
    text-align: center;
    font-size: larger;
    margin-left: 5em;
    margin-right: 5em;
  }
</style>