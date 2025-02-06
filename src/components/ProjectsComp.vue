<template>
    <div>
        <slot name="Pimage"></slot>
        <slot name="Pname"></slot>
        <slot name="description"></slot>
        <slot name="github"></slot>
        <slot name="live"></slot>
    </div>
</template>
<script> 
export default {
    
}
</script>
<style>
    /* Projects */

.projectsHead{
  padding: 10px;
}

.projects{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  text-decoration: none;
}

#proj-card{
  background-color: rgb(0, 0, 0);
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 18rem; 
  height: 26rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border-radius: 10px;
}

.project-image{
  width: 288px;
  height: 230px;
}

.project-btn1{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-right: 15px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-left: 15px;
}

.project-btn2 a{
  text-decoration: none;
  color: #2c3e50;
}

  /* media queries */

  /* 840px */

  @media only screen and (max-width:840px){
  .projectsHead{
    padding: 30px;
  }
  .projects{
    display:grid;
    grid-template-columns:repeat(2,1fr);
  }
  
  #proj-card{
  margin-left: 60px;
}
}

  /* 400px */

@media only screen and (max-width:400px){
  .projects{
    display:grid;
    grid-template-columns:repeat(1,1fr);
    text-decoration: none;
    place-content: center;
    margin-right: 100px;
  }

  #proj-card{
  background-color: white;
  box-shadow: black 5px 5px 5px , -1px -1px 2px;
  width: 16rem; 
  height: 26rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border-radius: 10px;
}

.project-image{
  width: 240px;
  height: 200px;
  padding-top: 10px;
}

.project-btn1{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-right: 15px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  padding: 10px;
  border-radius: 50px;
  background-color: #ccd8c1;
  margin-left: 15px;
}

.project-btn2 a{
  text-decoration: none;
  color: #2c3e50;
}
}
</style>