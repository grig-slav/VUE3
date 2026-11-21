<template>
    <div class="modal">
        <header>
            <slot name="title"></slot>
        </header>
        <main>
            <slot name="default"></slot>
        </main>
        <footer>
            <slot name="actions"></slot>
        </footer>
    </div>
</template>
<style scoped>
.modal{
    border: 1px solid black;
    border-radius: 10px;
    padding: 20px;
}
</style>