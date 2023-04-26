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
  
  <Navbar />
  <svelte:component this="{CurrentComponent}" />
  