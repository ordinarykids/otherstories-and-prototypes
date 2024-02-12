

<script>
    import {onMount} from 'svelte';
    import { useChat } from 'ai/svelte';
    import { FineTuningJobsPage } from 'openai/resources/fine-tuning/jobs';

    const { input, handleSubmit, messages } = useChat()


    let currentPath;
      onMount(() => {
        currentPath = window.location.pathname;

      });



</script>

<h1>TouchDesign Test</h1>
<h3>Portfolio</h3>


<div class="portfolioBlock">
    <p>These are some of my first experiments with real time procedural desing. Basically coding with nodes. </p>

    <iframe width="1765" height="956" src="https://www.youtube.com/embed/mrWvp8dhwEA" title="stylegan2 x op art patterns moires   latent walks 09 15 2020 1080p 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>




    <ul>
        <li><a href="https://helix-glober.vercel.app/" target="_blank">Flyover Idea 01</a></li>
        <li><a href="https://helix-glober.vercel.app/Helix24.html" target="_blank">Flyover Idea 24</a></li>
        <li><a href="https://helix-glober.vercel.app/Helix07.html" target="_blank">Map Test</a></li>
        <li><a href="https://p5js-wheat.vercel.app/" target="_blank">Early Block Idea</a></li>
        

        
    </ul>
    


</div>





<style>
    h1 {
        font-weight: 900;
    }
    p {
        font-family: 'IBM Plex Mono', monospace;
        padding-top: 16px;
        padding-bottom: 16px;
        font-weight: 200;
        font-size: 14px;
    }
.portfolioBlock {
    padding-bottom: 64px;
}

a {
    text-decoration: underline;
}
</style>