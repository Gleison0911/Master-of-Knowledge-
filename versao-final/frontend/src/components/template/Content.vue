<template>
    <div class="content">
        <router-view></router-view>
       
    </div>
</template>

<script>
export default {
    name: 'Content'   
}
</script>

<style>
    .content {
        grid-area: content;
        background-color: (#fafafa, #a8a8a8);
        padding: 20px;
    }   

    .img{
        grid-area: content;
        

    }
</style>
