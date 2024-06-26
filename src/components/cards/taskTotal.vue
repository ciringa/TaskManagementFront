<template>
    
    <div class=" bg-body-secondary MainBox w-25 m-3 p-3 shadow" style="border:1px dashed gray">
        <div class="flex-row w-100 d-flex justify-content-center align-items-center">
            <div class=" w-50"> 
                <h3 class="">Total:</h3>
            </div>
            <div class=" w-50 justify-content-end d-flex p-2"> 
                <h3 class="text-danger">{{value}}</h3>
            </div>
        </div>
        <p class=" text-secondary">{{Description}}</p>
    </div>
    
</template>


<script lang="ts">

export default {
    name:"taskCompletionTotal",
    props:{
        value:Number,
        Description:String
    }
}
</script>


<style scoped>

</style>