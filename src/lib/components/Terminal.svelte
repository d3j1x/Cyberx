<script>
// @ts-nocheck

    // @ts-ignore
    let commands = [];
    let input = '';
    
    // @ts-ignore
    function processCommand() {
        const command = input.trim();
        if (command === 'clear') {
            commands = [];
        } else {
            const response = executeCommand(command);
            // @ts-ignore
            commands = [...commands, { type: 'input', text: '> ' + command }, { type: 'response', text: response }];
        }
        input = '';
    }
    
    // @ts-ignore
    function executeCommand(command) {
        // Implement your command processing logic here
        if (command === 'help') {
            return 'Available commands: help, clear';
        } else {
            return 'Command not recognized. Type "help" for available commands.';
        }
    }
</script>


<!-- <div class="terminal">
    {#each commands as item (item.text)}
        <p class="{item.type}">{item.text}</p>
    {/each}
    <div class="terminal-input">
        <span>&gt;</span>
        <input type="text" bind:value={input} on:keydown={(e) => e.key === 'Enter' && processCommand()} autofocus />
    </div>
</div> -->

<div class="terminal">
    <div class="terminal-header">
        <span class="button red"></span>
        <span class="button yellow"></span>
        <span class="button green"></span>
    </div>
    <div class="terminal-body">
        <p class="font-bold">W E L C O M E</p>
        <p>Type 'help' to see available commands.</p>
    </div>
    
    {#each commands as item (item.text)}
        <p class="{item.type}">{item.text}</p>
    {/each}
    <div class="terminal-input">

        
        <span>&gt;</span>
        <!-- svelte-ignore a11y-autofocus -->
        <input type="text" bind:value={input} on:keydown={(e) => e.key === 'Enter' && processCommand()} autofocus />
    </div> 
    
</div>

<style>

/* .terminal {
        background-color: black;
        border-radius: 10px;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
        width: 400px;
        color: #00ff00;
        font-family: 'Courier New', monospace;
        overflow: hidden;
    } */
    

    .terminal {
    background-color: black;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
    width: 400px;
    color: #00ff00;
    overflow: hidden;
    }
    
    .terminal-header {
    background-color: #222;
    display: flex;
    justify-content: flex-end;
    padding: 5px;
    }

    .response {
        color: #00ff00;
        margin: 0;
        margin-left: 1em;
    }
    
    .terminal-input {
        display: flex;
        align-items: center;
        background-color: #222;
        padding: 5px 10px;
    }
    
    .terminal-input span {
        color: #00ff00;
        margin-right: 5px;
    }
    
    .terminal-input input {
        background-color: #222;
        color: #00ff00;
        border: none;
        outline: none;
    } 


    



.button {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    margin: 0 3px;
}

.red {
    background-color: #ff5f56;
}

.yellow {
    background-color: #ffbd2e;
}

.green {
    background-color: #27c93f;
}

.terminal-body {
    padding: 10px;
}

.terminal-input {
    display: flex;
    align-items: center;
    background-color: #222;
    padding: 5px 10px;
}

.terminal-input span {
    color: #00ff00;
    margin-right: 5px;
}

.terminal-input input {
    background-color: #222;
    color: #00ff00;
    border: none;
    outline: none;
}
</style>