

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

<h1>Helix</h1>
<h3>Portfolio</h3>


<div class="portfolioBlock">
    <img src="/Globe.jpg" alt="globe"  />
    <p>At a time of exponential innovation in biotechnology, a focus on leveraging genomics at the scale of populations made Helix a vital repository of data and information during the COVID-19 pandemic.</p>

    <p>As Helix refined its approach to messaging and other aspects of their brand, the technology they used for publishing content was fragmented and tough to use. Aleph engaged in an ambitious effort to shape a new visual presence around their existing identity, and to deliver a stable-but-malleable content platform to meet a diverse set of requirements with enterprise-level confidence.</p>
    
    <p>This migration presented us with a few major challenges from the word “go”. We were tasked with refining the online presentation of Helix’s identity and messaging through a comprehensive design process. In addition, we needed to conceptualize and build a tech platform that would modernize their publishing workflows while deftly handling several years of legacy content.</p>
    
    <p>Aleph delivered on a purposeful project plan, including the migration of content from multiple legacy platforms, a broad approach to content strategy and management, and a complete interactive design system featuring well-documented processes, usage and development recommendations. We’re proud to support Helix in their mission to innovate with population genomics, and excited to see what’s next.</p>
    

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