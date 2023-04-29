<script>
  let projects = [
    {
      name: "Portfolio",
      gitHub: "https://github.com/the-eyesack/portfolio",
      link: "https://theeyesack.vercel.app",
      technologies: ["Astro", "Svelte", "Sass"],
      description:
              "This website; a place where I can show off me and all my projects!",
    },
    {
      name: "Gridsite",
      gitHub: "",
      link: "https://gridsite.vercel.app",
      technologies: ["React", "NextJS", "Sass"],
      description:
        "Website to view data of grids for the 2023 FRC game, Charged Up!",
    },
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
      gitHub: "",
      link: "https://steelhawks.net",
      technologies: ["React", "TailwindCSS"],
      description: `Website for FIRST Robotics Competition team 2601.`,
    },
  ];
</script>

<section id="projects">
  <h1>Projects</h1>
  <div class="projects-wrapper">
    <div class="projects-grid">
      {#each projects as project}
        <div class="project-container">
          <h3>{project.name}</h3>
          <p class="project-description">{project.description}</p>

          <div class="bottom-info">
            <p class="project-technologies">{
                    project.technologies.map((tech)=> {return (" " + tech)})
            }</p>
            <div class="project-links">
              {#if project.gitHub !== ""}<a href={project.gitHub}><i class="fa-brands fa-github fa-2x" /></a>{/if}
              {#if project.link !== ""}<a href={project.link}><i class="fa-solid fa-earth-americas fa-2x" /></a>{/if}
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
  <p class="bottom-text">Something awesome coming... Just you wait.</p>
</section>

<style lang="scss">
  @import "src/variables";
  section {
    width: 100vw;
    height: 100vh;
  }

  .projects-wrapper {
    height: 50vh;

    @media (min-width: 1080px) and (max-width: 4000px) {
      height: 100vh;
    }
    overflow: scroll;
    -ms-overflow-style: none;  /* IE and Edge */
    scrollbar-width: none;  /* Firefox */

    &::-webkit-scrollbar {
      display: none;
    }
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, 26em);
    justify-content: center;


  }
  .project-container {
    border: 0.25rem solid $launch-red;
    text-align: center;
    margin-bottom: 0.5em;
    width: 24rem;
    height: 12rem;
    border-radius: 1rem;
    display: flex;
    flex-direction: column;

    p {
      margin-left: 0.5rem;
      margin-right: 0.5rem;
      margin-bottom: auto;
    }
    h3 {
      font-size: 1.25em;
      margin: 0.25em 0 0 0;
      font-family: $display;
      text-decoration: none;
      color: $space-white;
    }
  }

  .bottom-info {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin: auto 0.5em 0.5em 0.5em;

    p {
      margin: 0;
    }
    a {
      color: $light-purple;
      margin: 0 0.1em 0 0.1em;
      &:hover {
        color: $dark-purple
      }
    }
  }

  .bottom-text {
    display: block;
    text-align: center;
  }
</style>
