<script>
    export default {
    props: {
        symbol: String,
        name: String,
        PN: String,
        AR: String,
    }
  }
</script>

<template>
    <td class="Cell">
        <div class="N">{{ PN }}</div>
        <div class="Symbol">{{ symbol }}</div>
        <div class="Name">{{ name }}</div>
        <div class="N">{{ AR }}</div>
    </td>
</template>

<style>
    .Cell {
        border: 2px solid #6272a4;
        padding-left: 0.6rem;
        padding-right: 0.6rem;
        border-radius: 10px;
        min-width: 3.6rem;
    }

    .N {
        font-size: 0.8rem;
        color: #8be9fd;
    }

    .Symbol {
        font-size: 1.3rem;
        color: #f8f8f2;
    }

    .Name {
        font-size: 0.7rem;
        color: #f8f8f2;
    }
</style>