

<script>
    import { useChat } from 'ai/svelte'

    const { input, handleSubmit, messages } = useChat()
</script>


<h1>Day 2</h1>

<h3>Improve Chat</h3>



<section class="bg-cyan-100 h-64">
 
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