<script>
 
  import "../app.css";
  import Footer from "../components/Footer.svelte"
  import Header from "../components/Header.svelte"
  import AOS from 'aos';
  import 'aos/dist/aos.css';

  // initialize AOS after the component mounts
  import { onMount } from 'svelte';
  onMount(() => {
    AOS.init({
      duration: 1000,
      once: true
    });
  });

</script>

<div class="relative flex flex-col  mx-auto w-full tet-sm sm:text-base min-h-screen" >
   
    <Header/>
    <slot/>
    <Footer/>

</div>