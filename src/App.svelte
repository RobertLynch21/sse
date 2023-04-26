<script>
	import { onMount } from "svelte";
	import { currentPage } from "./store";
	import Home from "./components/Home.svelte";
	import About from "./components/About.svelte";
	import Projects from "./components/Projects.svelte";
	import Contact from "./components/Contact.svelte";
	import Navbar from "./components/Navbar.svelte";
  
	let CurrentComponent;
  
	onMount(() => {
	  $currentPage = window.location.pathname.slice(1) || "home";
	  updateComponent();
	});
  
	const updateComponent = () => {
	  switch ($currentPage) {
		case "home":
		  CurrentComponent = Home;
		  break;
		case "about":
		  CurrentComponent = About;
		  break;
		case "projects":
		  CurrentComponent = Projects;
		  break;
		case "contact":
		  CurrentComponent = Contact;
		  break;
		default:
		  CurrentComponent = Home;
	  }
	};
  
	currentPage.subscribe(() => {
	  updateComponent();
	});
  </script>

<header>
	<div class="logo-container">
	  <img src="media/logo.png" alt="Company Logo" class="logo" />
	</div>
	<div class="header-text">
	  <h1 class="company-title">S.S.E. ENTERPRISES LLC.</h1>
	  <h2 class="company-subtitle">Your Renewable Energy Partner</h2>
	</div>
  </header>
  <div class="page-container">
  <Navbar />
  <div class="content-wrap">
  <svelte:component this="{CurrentComponent}" />
</div>
</div>
  <footer>
	<p>&copy; 2023 S.S.E. Enterprise, LLC. All rights reserved.</p>
  </footer>
  
  <style>
	.page-container {
	  display: flex;
	  flex-direction: column;
	  min-height: 100vh;
	}
  
	.content-wrap {
	  flex: 1;
	}
  
	footer {
	  background-color: #1d1e22;
	  padding: 20px;
	  text-align: center;
	  font-size: 0.9rem;
	  color: #ffffff;
	  border-top: 1px solid rgba(255, 255, 255, 0.1);
	}
  </style>
  