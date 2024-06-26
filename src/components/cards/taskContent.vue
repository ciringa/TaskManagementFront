
<script lang="ts">
    export default {
        name:"taskGeneralCard",
        props:{
            title:String,
            Description:String,
            Date:Date,
            concluded:Boolean
        }
    }
</script>

<template>
    <div class=" w-100 p-2 Content rounded flex-column d-flex bg-body-tertiary " >
        <h2>{{title}}</h2>
        <div class=" w-100 flex-row d-flex">
            <div class=" w-50">
                <h6>{{Description}}</h6>
            </div>
                <div class=" w-50 justify-content-end d-flex">
                    <div class="  flex-column d-flex justify-content-end align-items-end">
                        <h6>{{Date}}</h6>
                        <button class="rounded border bg-danger text-white w-25" >Delete Task</button>
                    </div>
                </div>
            </div>
    </div>
</template>


<style scoped>
    .Content{
        margin-top: 2%;
        border-left: 10px solid rgb(116, 220, 116);
    }

</style>

