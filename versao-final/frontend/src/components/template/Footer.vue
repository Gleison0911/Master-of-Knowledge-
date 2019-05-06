<template>
    <footer class="footer">
        <span>  <strong> Master of Knowledge </strong> © INDRA todos os direitos reservados. </span>
    </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style>
    .footer {
        grid-area: footer;
        background-color: #000;
        color: #fff;

        display: flex;
        align-items: center;
        justify-content: flex-end;
        padding-right: 1%;
        
    }
</style>
