
<script lang="ts">
    import TooltipButtom from "./../buttons/toottipButtom.vue"
    export default {
        name:"CreateTaskForm",
        components:{
            TooltipButtom
        }
    }
</script>


<template>
            <div class=" w-25 bg-body-secondary shadow p-4 h-auto" style="border: .75px dashed gray;">
                <h5>Descrição</h5>
                <h6>Insira aqui sua Descrição</h6>
                <input type="text" class=" w-100 bg-body-tertiary rounded border-secondary text-center" placeholder="Insira aqui sua descrição">
                <p class=" text-secondary">Ex:Limpar a casa, levar o lixo para fora e etc</p>
                <h6>Insira aqui sua Descrição</h6>
                <input type="text" class=" w-100 bg-body-tertiary rounded border-secondary text-center" placeholder="Insira aqui sua descrição">
                <p class=" text-secondary">Ex:Limpar a casa, levar o lixo para fora e etc</p>
                <h6>Insira aqui sua Descrição</h6>
                <input type="text" class=" w-100 bg-body-tertiary rounded border-secondary text-center" placeholder="Insira aqui sua descrição">
                <p class=" text-secondary inputDescription">Ex:Limpar a casa, levar o lixo para fora e etc</p>
                <tooltipButtom MainText="Criar tarefa" Alt="Clique aqui para criar uma tarefa" class="w-100 mt-5" />
            </div>
</template>




<style scoped>
    .inputDescription{
        font-size: 15px;
    }


</style>