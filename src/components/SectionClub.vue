<template>

<div class="club">
  <div class="cardwhite row">
    <b-card class="cardtext">
      <b-card no-body class="overflow-hidden" style="max-width: 740px;">
        <b-card-body title="Horizontal Card">
          <b-card-text>
            <div class="col mb-4"><h2> LUXURY Familly : le club qui apporte satisfaction à tout vos besoins !</h2></div>
            <div class="col"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc, ut auctor lectus . 
              At enim aucacilisis eget. Condimenpellentesque risus, tincidunt. 
              Pro morbi tempor, curabitur neque quam convallis.</p>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc, ut auctor lectus . 
              At enim aucacilisis eget.</p>
            </div>
            <b-button class="button1" href="#">Devenir membre</b-button>
          </b-card-text>
        </b-card-body>
      </b-card>
    </b-card>
    
  </div>
</div>


</template>


<style scoped>
.club{
background-color: #001E00;
height: 700px;
width: 100%;
margin: 0%;
padding: 0%;
display: flex;
align-items: center;
justify-content: end;
}

.cardwhite{
background-color: #ffffff;
border-radius: 100px 0px 0px 100px;
border: #000000 solid 5px;
box-shadow: #000000 2px 2px 40px 2px;
width: 65%;
height: 600px;
display: flex;
align-items: center;
justify-content: center;
flex-direction: row;
}

.cardwhite:hover{
box-shadow: #fbe5d0 2px 2px 40px 2px;
border:none;
}

.cardtext{
box-shadow: #f6d4b5 1px 1px 20px 1px;
width: 45%;
height: 87%;
border-radius:70px;
display: flex;
align-items: center;
padding-left: 60px;
padding-right: 60px;
text-align: justify;
color: #001E00;
z-index: 125;
transform: translateX(40px);
}

p{
  font-size: 16px;
}

.button1{
    background-color:#D79D66 ;
    color: white;
    padding: 5px 15px 8px 15px;
    border-radius: 15px;
}


/* carousel */
.carousel {
  width: 55%;
  height: 200px;
  margin: 0;
  display: grid;
  grid-template-rows: 500px 100px;
  grid-template-columns: 1fr 30px 30px 30px 30px 30px 1fr;
  align-items: flex-start;
  justify-items: center;
  position: relative;
  top: -150px;
  left: -780px;

}

main#carousel {
  grid-row: 1 / 2;
  grid-column: 1 / 8;
  width: 100vw;
  height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  transform-style: preserve-3d;
  perspective: 600px;
  --items: 5;
  --middle: 3;
  --position: 1;
  pointer-events: none;
}

div.item {
  position: absolute;
  width: 300px;
  height: 400px;
  background-color: coral;
  --r: calc(var(--position) - var(--offset));
  --abs: max(calc(var(--r) * -1), var(--r));
  transition: all 0.25s linear;
  transform: rotateY(calc(-10deg * var(--r)))
    translateX(calc(-300px * var(--r)));
  z-index: calc((var(--position) - var(--abs)));
}

div.item:nth-of-type(1) {
  --offset: 1;
  background-color: #90f1ef;
}
div.item:nth-of-type(2) {
  --offset: 2;
  background-color: #ff70a6;
}
div.item:nth-of-type(3) {
  --offset: 3;
  background-color: #ff9770;
}
div.item:nth-of-type(4) {
  --offset: 4;
  background-color: #ffd670;
}
div.item:nth-of-type(5) {
  --offset: 5;
  background-color: #e9ff70;
}

input:nth-of-type(1) {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}
input:nth-of-type(1):checked ~ main#carousel {
  --position: 1;
}

input:nth-of-type(2) {
  grid-column: 3 / 4;
  grid-row: 2 / 3;
}
input:nth-of-type(2):checked ~ main#carousel {
  --position: 2;
}

input:nth-of-type(3) {
  grid-column: 4 /5;
  grid-row: 2 / 3;
}
input:nth-of-type(3):checked ~ main#carousel {
  --position: 3;
}

input:nth-of-type(4) {
  grid-column: 5 / 6;
  grid-row: 2 / 3;
}
input:nth-of-type(4):checked ~ main#carousel {
  --position: 4;
}

input:nth-of-type(5) {
  grid-column: 6 / 7;
  grid-row: 2 / 3;
}
input:nth-of-type(5):checked ~ main#carousel {
  --position: 5;
}

</style>



