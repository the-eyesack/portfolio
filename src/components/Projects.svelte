<script>
  let projects = [
    {
      name: "The Gradeulator",
      gitHub: "https://github.com/the-eyesack/thegradeulator",
      link: "https://thegradeulator.vercel.app/",
      technologies: ["React", "TailwindCSS"],
      description:
        "Built for the 2022 Congressional App Challenge, this app provided a manual solution to a lack of a grade book.",
    },
    {
      name: "Steel Hawks Website",
      gitHub: "https://github.com/steelhawks/website-2023",
      link: "https://steelhawks.net",
      technologies: ["React", "TailwindCSS"],
      description: "Website for FRC 2601, built in React.",
    },
    {
      name: "Gridsite",
      gitHub: "https://github.com/steelhawks/gridsite",
      link: "https://github.com/steelhawks/gridsite",
      technologies: ["React", "NextJS", "Sass"],
      description:
        "Website to view data of grids for the 2023 FRC game, Charged Up!",
    },
    {
      name: "????",
      gitHub: "https://github.com/the-eyesack",
      link: "localhost:3000",
      technologies: ["???", "???"],
      description: "Who knows what the future holds?",
    },
  ];
</script>

<section id="projects">
  <h1>Projects</h1>
  <div class="projects-wrapper">
    <div class="projects-grid">
      {#each projects as project}
        <div class="project-container">
          <a href={project.link}>{project.name}</a>
          <p>{project.description}</p>
          <a class="github-icon" href={project.gitHub}><i class="fa-brands fa-github fa-xl" /></a>
        </div>
      {/each}
    </div>
  </div>
</section>

<style lang="scss">
  @import "src/variables";
  section {
    width: 100vw;
    height: 100vh;
  }
  .projects-wrapper {
    display: flex;
    justify-content: center;
  }
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }
  .project-container {
    font-weight: 700;
    border: 0.25rem solid $launch-red;
    text-align: center;
    margin: 0.25rem 2rem 1rem;
    width: 24rem;
    height: 12rem;
    border-radius: 1rem;
    position: relative;

    a {
      font-size: 1.25em;
      font-family: $display;
      text-decoration: none;
      color: $space-white;
    }

    .github-icon {
      position: absolute;
      bottom: 15px;
      right: 10px;
    }

  }

</style>
