<template>
    <div>
        <h1>
          <slot name="Pimage"></slot>
          <slot name="Pname"></slot>
          <slot name="description"></slot>
          <slot name="github"></slot>
          <slot name="live"></slot>
        </h1>
    </div>
</template>
<script>
export default {
  props:['cover']
}
</script>
<style >

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
  border: 2px solid white;
  box-shadow: black 3px 3px 3px , -3px -3px 3px black;
  width: 18.5rem;
  height: 28rem;
  margin-bottom: 50px;
  margin-left: 100px;
  border-radius: 10px;
}


#proj-card:hover {
  transform: scale(1.05);
  transition: 0.3s ease-out;
}

.project-image{
  width: 288px;
  height: 230px;
}

.project-text{
  width: 270px;
  margin-left: 10px;
}

.project-btn1{
  margin-right: 5px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  margin-left: 5px;
}

.project-btn2 a{
  text-decoration:none;
  color: #2c3e50;
}

  /* media queries */

  /* 840px */

  /* @media only screen and (max-width:840px){
  .projectsHead{
    padding: 30px;
  }
  .projects{
    display:grid;
    grid-template-columns:repeat(2,1fr);
  }
  .project-btn1{
    margin-right: 0px;
  }
  .project-btn2{
    margin-left: 0px;
  }
} */

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
    background-color: rgb(0, 0, 0);
    border: 2px solid white;
    box-shadow: black 3px 3px 3px , -3px -3px 3px black;
    width: 18.5rem;
    height: 32rem;
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
  margin-right: 15px;
}

.project-btn1 a{
  text-decoration:none;
  color: #2c3e50;
}

.project-btn2{
  margin-left: 15px;
}

.project-btn2 a{
  text-decoration: none;
  color: #2c3e50;
}
}
</style>