

<script>
    import {onMount} from 'svelte';
    import { useChat } from 'ai/svelte';

    const { input, handleSubmit, messages } = useChat()


    let currentPath;
      onMount(() => {
        currentPath = window.location.pathname;

      });



</script>



<h1>Day 3</h1>

<h3>HYPOTHESIS</h3>
<p>By becoming apart of the morning habits of users, our AI can help coach users into making better decisions around both finances and living in general.  </p>

<p>In the seamless tapestry of daily life, morning routines stand out as a cornerstone of productivity and mindset. We posit an intriguing hypothesis: by weaving our Artificial Intelligence (AI) into the very fabric of these morning rituals, we can significantly elevate the decision-making prowess of our users. This integration goes beyond mere financial advisement; it seeks to harmonize with the holistic aspects of living, fostering a symbiotic relationship where AI becomes an invisible yet impactful mentor.</p>  

<p>Through this strategic insertion into the day's inception, our AI endeavors to become a catalyst for nuanced improvements in life choices, guiding users towards not only financial acumen but also a more enriched living experience. This visionary approach holds the promise of transforming ordinary mornings into extraordinary opportunities for growth and self-improvement.</p>

<h2 class="padding-top-128" >useChat</h2>

<section class="h-64">
 
    <ul>
        {#each $messages as message}
            <li>{message.role}: {message.content}</li>
        {/each}
    </ul>
    <form on:submit={handleSubmit}>
        <input class="bg-teal-200" bind:value={$input} />
        <button type="submit">Send</button>
    </form>
</section>

<style>


    h1 {
        width: 100%;
    }
</style>