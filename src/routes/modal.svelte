<script>
    /**
     * is the modal open?
     */
    export let isOpen = false;
    $: isOpen;
</script>

<!-- um gatilho qualquer para o modal -->


{#if isOpen}
    <div class="modal">
        <div class="backdrop" on:click={() => (isOpen = !isOpen)} />
        <div class="content-wrapper">
           <slot/>
            <div class="footer" onclick={() => (isOpen = !isOpen)}>
                <div class="modalButton" on:click={() => (isOpen = !isOpen)}>
                    <button name="btn-close"class="btn btn-outline-light btn-lg"> Finalizar </button>
                </div>
            </div>
        </div>
    </div>
{/if}

<style>
    div.modal {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    div.backdrop {
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.9);
    }
    div.content-wrapper {
        display: flex;
        flex-flow: row wrap;
        justify-content: flex-end;
        align-items: flex-start;
        z-index: 10;
        max-width: 70vw;
        border-radius: 0.3rem;
        background-color: #212529;
        /* overflow: hidden; */
        border-radius: 20px;
        width: 30%;
        height: 95%;
    }
    div.footer {
        width: 100%;
        display: flex;
        flex-flow: row nowrap;
        justify-content: flex-end; 
        align-items: center; 
    }
    button[name=btn-close]{
        display: flex;
        align-items: center;
    }
</style>