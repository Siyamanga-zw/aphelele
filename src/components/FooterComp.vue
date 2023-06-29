<template>
    <div class="container-fluid" id="footer">
<div class="row">
    <p class="lead">Copyright &copy; {{currentyear}}</p>
</div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                currentyear:new Date().getFullYear()
            }
        }
    }
</script>

<style scoped>

</style>