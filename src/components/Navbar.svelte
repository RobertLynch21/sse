<script>
    import { currentPage } from "../store";
    
    const navigate = (page) => {
      currentPage.set(page);
      history.pushState({}, "", `/${page}`);
    };
  </script>
  
  <nav>
    <a href="/" on:click|preventDefault={() => navigate("home")}>Home</a>
    <a href="/about" on:click|preventDefault={() => navigate("about")}>About</a>
    <a href="/projects" on:click|preventDefault={() => navigate("projects")}>Projects</a>
    <a href="/contact" on:click|preventDefault={() => navigate("contact")}>Contact</a>
  </nav>
  