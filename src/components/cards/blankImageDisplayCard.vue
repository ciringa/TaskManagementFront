<template>
    <div class="card bg-body-secondary shadow">
      <div class="card-image"></div>
        <div class=" d-flex flex-row"> 
          <a class="category text-danger" style="text-decoration:none">{{Tags.toString()}}</a>
        </div>
      <div class="heading "> {{Text}}
        <div class="author text-secondary"> By <span class="name text-primary">{{Author}}</span> 4 days ago</div>
    </div>
</div>
</template>


<script>
export default {
    name:"ImageDisplayCard",
    props:{
      Author:String,
      Title:String,
      Text:String,
      Tags:Array,
      ImageUrl:String
    }
}
</script>


<style scoped>
.card {
  width: 350px;
  padding: .4em;
  border-radius: 6px;
  border: 1px dashed gray;
}

.card-image {
  background-color: rgb(162, 162, 162);
  width: 100%;
  height: 230px;
  border-radius: 6px 6px 0 0;
}

.category {
  text-transform: uppercase;
  font-size: 0.7em;
  font-weight: 600;
  padding: 10px 7px 0;
}

.category:hover {
  cursor: pointer;
}

.heading {
  font-weight: 600;
  padding: 7px;
}

.heading:hover {
  cursor: pointer;
}

.author {
  font-weight: 400;
  font-size: 15px;
  padding-top: 20px;
}

.name {
  font-weight: 600;
}

.name:hover {
  cursor: pointer;
}
</style>