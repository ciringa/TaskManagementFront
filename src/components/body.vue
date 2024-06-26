<script lang="ts">
    import taskGeneralCard from "./cards/taskContent.vue"
    import CreateTaskForm from "./cards/CreateTask.vue"
    import taskCompletionTotal from "./cards/taskTotal.vue"
    import ImageDisplayCard from "./cards/blankImageDisplayCard.vue"
    export default {
        name:"Body",
        props:{
            Bound:String
        },
        components:{
            taskGeneralCard,
            CreateTaskForm,
            taskCompletionTotal,
            ImageDisplayCard
        }
    }
</script>

<template>
    <div width="100%" class="d-flex  justify-content-center align-items-center m-4 p-2 flex-column row-gap-5 ">



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

        <div class=" w-75 h-auto p-3 d-flex justify-content-center align-itens-center flex-row gap-5 flex-wrap">
            <ImageDisplayCard Author="John Doe" Text="An work spree over the weekend" :Tags="new Array(['Work','Payment'])" />
            <ImageDisplayCard Author="Steven Yean" Text="An job oportunity nearest to you" :Tags="new Array(['Work','Job'])" />
            <ImageDisplayCard Author="Alina Mandson" Text="A Online Gym with Trained personel" :Tags="new Array(['Exercise','Comunnity'])" />
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

