

<script>
    import {onMount} from 'svelte';
    import { useChat } from 'ai/svelte'
    import SvelteMarkdown from 'svelte-markdown'
    const { input, handleSubmit, messages } = useChat()

    let messegeCounter = messages.length;

    let formattedMessages;


</script>


<h1>Day 1</h1>
<div class="flex flex-col h-[500px] max-h-[500px] border border-gray-300 rounded-lg overflow-hidden">

    <div class="bg-gray-200 p-4">
        <h3 class="text-lg font-semibold">Morning Chat</h3>
    </div>


    <div class="flex-1 p-4 overflow-y-auto">
        <!-- Repeat messages -->
        {#each $messages as message}
            <div class="p-2 my-2 bg-gray-100 rounded-md {message.role}">{message.role}: {message.content}</div>
        {/each}

    </div>


    <div class="bg-gray-200 p-4">
        <form on:submit={handleSubmit}>
            <input class="bg-teal-200" bind:value={$input}> 
            <button type="submit">Send</button>
        </form>

       
    </div>
</div>

<style>
.user {
    background-color: #cfcfcf;
}

</style>