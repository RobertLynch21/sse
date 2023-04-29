<!-- Projects.svelte -->
<script>
  import { push } from 'svelte-spa-router';
  
  const navigateToCategory = (path) => {
    push(path);
  };
</script>

<!-- Projects.svelte -->
<section>
  <h2>Projects</h2>
  <div class="projects-container">
    <div class="project-category">
      <img
        src="/media/baltimore.jpg"
        alt="Solar Carport Projects"
        class="project-image"
        on:click={() => navigateToCategory('/solarCarportProjects')}
      />
      <h3 class="project-title">Solar Carport Projects</h3>
    </div>
    <div class="project-category">
      <img
        src="/media/prov-ri.jpg"
        alt="Solar Field Projects"
        class="project-image"
        on:click={() => navigateToCategory('/solar-field-projects')}
      />
      <h3 class="project-title">Solar Field Projects</h3>
    </div>
  </div>
</section>


<style>
  .projects-container {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 20px;
  }

  .project-category {
    text-align: center;
    cursor: pointer;
  }

  .project-image {
    width: 100%;
    max-width: 300px;
    border-radius: 5px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    object-fit: cover;
  }

  .project-title {
    margin-top: 10px;
    font-weight: 600;
  }
</style>

