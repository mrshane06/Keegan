<template>
    <div>
        <slot name="about"></slot>
        <slot name="me"></slot>
    </div>
</template>
<script>
export default {
    
}
</script>
<style>
    #about_info{
    display: flex;
  }
  /* about */
  .aboutHead{
    padding-left: 40px;
    padding-top: 5px;
    padding-bottom: 5px;
  }
  #me{
    width: 240px;
    height: 300px;
    margin-left: 30px;
  }
  .aboutText{
  width: 330px;
  padding: 17px;
  font-size: 15px;
  place-items: center;
  margin: auto;
  margin-left: 30px;
  }
  /* skills */
  .whoop{
    padding-top: 30px;
  }
  .bottom{
    margin-top: 35px;
    display: grid;
    width: 1000px;
    margin-left: 80px;
    grid-template-columns: repeat(7 ,1fr);
  }
  .bottom2{
    margin-top: 35px;
    display: grid;
    width: 1000px;
    margin-left: 150px;
    grid-template-columns: repeat(6 ,1fr);
  }
  #skill{
    border-radius: 20px;
    width: 105px;
    height:100px;
    transition: 1s;
  }

  #skill:hover{
    transform: rotate(10deg);
}

  /* badges */

  #achieve{
    border-radius: 10px;
    width: 105px;
    height:100px;
    transition: 1s;
  }

  #achieve:hover{
    transform: rotate(10deg);
  }

  .bottom3{
    margin-top: 35px;
    display: grid;
    width: 800px;
    margin-left: 230px;
    grid-template-columns: repeat(5 ,1fr);
  }

  /* media queries */


  /* 840px */

  @media only screen and (max-width:840px){
  #about_info{
    display: block;
  }
  /* about */
  .aboutHead{
    padding: 15px;
  }
  #me{
    margin-left: 0px;
  }
  .aboutText{
    width: 450px;
    padding: 17px;
    font-size: 18px;
    place-items: center;
    margin: auto;
    margin-left: 165px;
  }
  /* skills */
  .whoop{
    padding-top: 0px;
  }
  .bottom{
    margin-top: 35px;
    display: grid;
    width: 800px;
    margin-left: 20px;
    grid-template-columns: repeat(5 ,1fr);
  }
  .bottom2{
    margin-top: 35px;
    display: grid;
    width:800px;
    margin-left: 20px;
    grid-template-columns: repeat(5 ,1fr);
  }
  .bottom3{
    margin-top: 35px;
    display: grid;
    width: 800px;
    margin-left: 20px;
    grid-template-columns: repeat(4 ,1fr);
  }
}

  /* 400px */

@media only screen and (max-width:400px){
  #about_info{
    display: block;
  }
  /* about */
  .aboutHead{
    padding-left: 0px;
  }
  #me{
    margin-left: 0px;
  }
  .aboutText{
    width: 330px;
    padding: 17px;
    font-size: 14px;
    place-items: center;
    margin: auto;
    margin-left: 5px;
  }
  /* skills */
  .whoop{
    padding-top: 0px;
  }
  .bottom{
    margin-top: 35px;
    display: grid;
    width: 300px;
    margin-left: 35px;
    grid-template-columns: repeat(2 ,1fr);
  }
  .bottom2{
    margin-top: 35px;
    display: grid;
    width: 300px;
    margin-left: 35px;
    grid-template-columns: repeat(2 ,1fr);
  }
  .bottom3{
    margin-top: 35px;
    display: grid;
    width: 300px;
    margin-left: 35px;
    grid-template-columns: repeat(2 ,1fr);
  }
}

/* 360px */

@media only screen and (max-width:360px){
  /* about */
  .aboutText{
    width: 300px;
  }
  /* skills */
  .whoop{
    padding-top: 0px;
  }
  .bottom{
    margin-left: 20px;
  }
  .bottom2{
    margin-left: 25px;
  }
  .bottom3{
    margin-left: 25px;
  }
}

/* 320px */

@media only screen and (max-width:320px){
  /* about */
  .aboutText{
    width: 280px;
    margin-left: 0px;
  }
  /* skills */
  .bottom{
    margin-left: 5px;
  }
  .bottom2{
    margin-left: 5px;
  }
  .bottom3{
    margin-left: 5px;
  }
}
</style>