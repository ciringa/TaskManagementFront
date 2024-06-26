<script>
    export default{
        name:"Header",
        data(){
            return{
                valor:""
            }
      }
    }
</script>


<template>
    <div class="randomDiv bg-dark-subtle text-black d-flex flex-row shadow">
        <div class="DividedContentElement gap-2 ">
            <h1><strong class="text-danger">Welcome</strong> Home</h1>
        </div>
        <div class="DividedContentElement justify-content-lg-end d-flex gap-5">
            <a class="bg-danger p-3 rounded-1 text-light fw-bolder" style="--bs-bg-opacity: 1;text-decoration: none;cursor: pointer;">LogOut</a>
            <a class="bg-danger p-3 rounded-1 text-light fw-bolder" style="--bs-bg-opacity: 1;text-decoration: none;cursor: pointer;">Github</a>
            <a class="bg-danger p-3 rounded-1 text-white  fw-bolder" style="--bs-bg-opacity: 1;text-decoration: none;cursor: pointer;">Api Docs</a>
        </div>
    </div>
</template>


<style scoped>
    .randomDiv {
        color: white;
        background-color:rgb(31, 31, 31) ;
        justify-content: center;
        align-items: center;
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 2%;
    }
    .headerAnchor{
        font-size: 25px;
        cursor: pointer;
        text-decoration: none;
    }
    .DividedContentElement{
        width: 50%;
    }

    
</style>