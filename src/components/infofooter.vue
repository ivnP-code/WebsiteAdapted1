<template>
<div class="Topline">ИНФОРМАЦИЯ</div>
<div class="wrapthings">
 <div class="box1">
  <div class="icon-text">
    <img class="corpo" src="/images/client.png">
    <div class="text-block">
    <div class="bigtext">Множество клиентов</div>
    <div class="smalltext">Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet consectetur adipisicing elit Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, fuga.</div>
    </div>
  </div>
</div>
<div class="box1">
  <div class="icon-text">
    <img class="corpo" src="/images/youtube.png">
    <div class="text-block">
    <div class="bigtext">Большая аудитория на Youtube</div>
    <div class="smalltext">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate, cupiditate.Lorem ipsum dolor sit amet consectetur adipisicing elit Lorem ipsum dolor sit amet, consectetur adipisicing elit. Enim, fuga.</div>
    </div>
  </div>
</div>

</div>

</template>

<style scoped>
.Topline{
  padding-bottom: 20px;
  border-bottom: 4px solid rgb(22, 108, 206);
  font-weight: 700;
  font-size: 24px;
    margin-left: 80px;
    margin-right: 80px;
}
img{
  width: 50px;
  height: 50px;
}
.wrapthings{
 display: grid;     
 grid-template-columns: repeat(2, 1fr); 
 justify-content: center;
 margin: 40px;
 margin-left: 80px;
}
.bigtext{
      font-size: 24px;
      font-weight: 900;
      display: flex;
      justify-content: center;
}
.smalltext{
      font-size: 18px;
      color: gray;
}
.icon-text {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  margin-top: 20px;
}
.text-block {
  flex: 1;
}
.corpo{
  margin-top: 20px;
}
@media (max-width: 786px) {
.wrapthings{
 grid-template-columns: repeat(1, 1fr); 
}
}
</style>
<script>
export default {
  name: 'Nav',
}
</script>