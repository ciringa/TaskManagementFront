<script lang="ts">
    import taskGeneralCard from "./cards/taskContent.vue"
    import CreateTaskForm from "./cards/CreateTask.vue"
    import taskCompletionTotal from "./cards/taskTotal.vue"

    export default {
        name:"Body",
        props:{
            Bound:String
        },
        components:{
            taskGeneralCard,
            CreateTaskForm,
            taskCompletionTotal
        }
    }
</script>

<template>
    <div width="100%" class="d-flex  justify-content-center align-items-center m-4 p-2 flex-column ">
        <div class=" w-75 h-auto p-3 d-flex flex-row gap-5" >
            <CreateTaskForm />
            
            <div class=" w-75 bg-body-secondary shadow p-4 flex-column gap-3" style="border: .75px dashed gray;"> 
                <taskGeneralCard :Date="new Date()" :Description="new String('lavar e enxugar as roupas que deixei na maquina de lavar')"  :title="new String('lavar as roupas')"/>
                <task-general-card :Date="new Date()" Description="lavar o carro utilizando veja" title="lavar o carro"/>
                <task-general-card :Date="new Date()" Description="lavar o carro utilizando veja" title="lavar o carro"/>
                <task-general-card :Date="new Date()" Description="lavar o carro utilizando veja" title="lavar o carro"/>
            </div>
        </div>

        <div class=" d-flex justify-content-start align-items-center flex-row w-75 mt-5">
            <taskCompletionTotal :value="new Number(12)" Description="A quantidade total de tarefas concluídas na conta" />
            <taskCompletionTotal :value="new Number(15)" Description="A Media global de tarefas concluídas, continue avançando" />
            <taskCompletionTotal :value="new Number(18)" Description="A Quantidade de tarefas concluídas essa semana" />
            <taskCompletionTotal :value="new Number(23)" Description="Sua posição no ranking global, consiga mais pontos para subir" />
        </div>
    </div>
</template>


<style scoped>
    input{
        height: 70px;
        font-size: 20px;
        outline: none;
        border: none;
    }


    .Content{
        border-left: 6px solid green;
    }
</style>>

