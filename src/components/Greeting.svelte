<script>
  import "animate.css";
</script>

<section id="">
  <div>
    <h1>
      Greetings. I'm <span>Isaac Wong</span>.
    </h1>
    <h2>This is my little galaxy.</h2>
  </div>

  <div class="img-wrapper">
    <img draggable="false" src="/placeholder.jpg" alt="dog" />
  </div>
</section>

<style lang="scss">
  @import "src/variables";
  section {
    width: 100vw;
    height: 100vh;
  }
  img {
    height: 24rem;
    position: absolute;
    top: 18rem;
    border-radius: 9999px;
    border: 1rem solid $space-white;
  }
  span {
    color: transparent;
    background-clip: text;
    background-image: linear-gradient(
      to left,
      #492e9f,
      #5133b0,
      #5938c2,
      #613dd4,
      #6942e6,
      #7f48e6,
      #924fe6,
      #a256e6,
      #b564d6,
      #bf75c8,
      #c387be,
      #c19ab7
    );
  }
  h2 {
    text-align: center;
    font-family: $display;
    font-size: 1.5rem;
  }
  .img-wrapper {
    display: flex;
    justify-content: center;
  }
</style>
