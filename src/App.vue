<template>
<div>
 <Nav />
    <FirstBlock />
    <Blogs />
</div>  
</template>

<style>
.nav {
  margin: 20px 60px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  padding: 25px;
  background-color: rgb(250, 250, 250);
  border: 1px solid black;
  border-radius: 8px;
  border-bottom: 2px solid black;
}

.nav-left, .nav-center, .nav-right {
  display: flex;
  align-items: center;
}

.nav-center {
  justify-content: center;
  width: 500px;
}

.logo {
  font-weight: bold;
  font-size: 20px;
}
.blogname {
  font-weight: bold;
  font-size: 22px;
}

.buttontop {
  padding: 15px;
  color: rgb(35, 35, 35);
  background-color: aliceblue;
  border-radius: 5px;
  border: 1px solid silver;
  font-size: 18px;
  margin-left: 10px;
  transition-duration: 1s;
}
.buttontop:hover{
  background-color: darkgray;
  transition-duration: 1s;
}

input {
  margin-left: 440px;
  width: 300px;
  padding: 15px;
  background-color: aliceblue;
  border: 1px solid silver;
  border-radius: 5px;
  font-size: 18px;
}
input:active{
  border:#00bbff;
}
.pic{
height: 100px;
width: 100px;
border-radius: 50%;
transition-duration: 1s;
}
.pic:hover{
  transform: rotateZ(180deg);
}
.blockwrap1 {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  margin: 20px;
  padding: 25px;
  background-color: rgb(109, 31, 31);
  border: 1px solid rgb(0, 0, 0);
  border-radius: 8px;
  border-bottom: 2px solid black;
  color: white;
}

.textblock {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.sidepicture{
max-width: 900px;
max-height: 500px;
border: 4px solid white;
margin-right: 50px;
}
.sidetext1{
  font-size: 76px;
}
.sidetext2{
  font-size: 36px;
}
.red{
  padding: 15px;
  color: rgb(255, 255, 255);
  background-color: rgb(187, 39, 39);
  border-radius: 5px;
  font-size: 18px;
  width: 200px;
  border: solid 1px rgb(187, 39, 39);
  margin-top: 20px;
  transition-duration: 1s;
}
.red:hover{
  background-color: rgb(117, 17, 17);
   border: solid 1px rgb(117, 17, 17);
  transition-duration: 1s;
}
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
  padding: 20px;
  align-items: start;
}

.blog{
  background-color: aliceblue;
  border-radius: 5px;
  border: solid 1px silver;
  font-size: 18px;
}
.blog img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.readmore{
  background-color: rgb(237, 198, 27);
  border-radius: 5px;
  padding: 10px;
  border: 1px yellow solid;
  margin: 10px 20px;
  font-weight: bold;
  transition-duration: 1s;
}
.readmore2{
  background-color: aliceblue;
    transition-duration: 1s;
}
.readmore:hover{
  background-color: darkgoldenrod;
}
.readmore2:hover{
  background-color: darkgray;
}

.blogblue {
  grid-row: 2;
  background-color: #00bbff;
  padding: 20px;
  border-radius: 5px;
  min-height: 60%; 
  color: white;
  font-size: 18px;
}


.blogblue img{
  max-width: 600px;
  max-height: 200px;
  border: solid 6px white;
}
.readmore2 {
  background-color: rgb(243, 243, 243);
  border: rgb(255, 255, 255) 1px solid;
  border-radius: 5px;
  padding: 10px;
  margin: 10px 20px;
  color: rgb(0, 0, 0);
  font-weight: bold;

}
.bottom{
  margin-top: 40px;
  display: flex;
  justify-content: center;
  border: 1px solid silver;
  font-size: 24px;
  font-weight: bold;
  padding: 25px;
}
.textblog{
    padding: 0px 20px;
}
h3{
    padding: 0px 20px;
}
*{
    margin: 0;
    padding: 0;
}
@media (max-width: 1500px){
.grid-container{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  padding: 20px;
  align-items: start;
}
.blogblue {
  grid-row: 1;
  background-color: #00bbff;
  padding: 20px;
  border-radius: 5px;
  color: white;
  font-size: 18px;
}
.blockwrap1 {
  display: flex;
  flex-direction: column;
}
}
@media (max-width: 1300px){
.nav {
  margin: 20px 60px;
  display: flex;
  align-items: center;
}

.nav-left, .nav-center, .nav-right {
  display: flex;
  align-items: center;
}

.nav-center {
  flex: 1 1 auto;
  min-width: 200px;
  max-width: 500px;
  justify-content: center;
  margin: 10px;
}
.nav-center input {
  width: 100%;
  max-width: 300px;
}
}
@media (max-width: 1100px){
.sidepicture{
  max-width: 400px;
  max-height: 500px;
}
}
@media (max-width: 768px){
  .grid-container{
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  padding: 20px;
  align-items: start;
}
@media (max-width: 510px){
.sidepicture{
  max-height: 200px;
  max-width: 200px;
}
}
}
</style>

<script>
import Nav from './components/nav.vue';
import FirstBlock from './components/firstblock.vue';
import Blogs from './components/blogs.vue';

export default {
    components:{
        Nav,
        FirstBlock,
        Blogs
      }
}
</script>
