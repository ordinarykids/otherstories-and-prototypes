

<script>
    import {onMount} from 'svelte';
    import { useChat } from 'ai/svelte'
    import SvelteMarkdown from 'svelte-markdown'
    const { input, handleSubmit, messages } = useChat()

    let messegeCounter = messages.length;

    let formattedMessages;

    //iterate of messages one by one and format them with svelte-markdown
    

    // import { Configuration, OpenAIApi } from 'openai';

    // let response;

    // onMount(async () => {
    // const configuration = new Configuration({
    //     apiKey: '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',
    // });
    // const openai = new OpenAIApi(configuration);

    // let response = await openai.createCompletion({
    //     model: "text-davinci-003",
    //     prompt: "Hello world", 
    //     max_tokens: 100
    // });

    // response = response.data.choices[0].text;
    // });
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