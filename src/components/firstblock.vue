<template>
    <div class="blockwrap1">
  <div class="textblock"> 
    <div class="sidetext1">Работа мечты компания Google</div>
    <div class="sidetext2">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eos dolore perferendis accusantium id pariatur neque impedit, ipsum aspernatur, sapiente est molestiae temporibus sit modi itaque, hic mollitia! Alias quisquam, minus quaerat voluptas consequatur tempora iure est, adipisci modi eveniet cupiditate!</div>
  <button class="Readmore">ЧИТАТЬ ДАЛЕЕ</button>
</div>
  <img src="/images/keyboards.jpg" class="sidepicture">
</div>
</template>
<style scoped>
.blockwrap1 {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  margin: 20px;
  padding: 25px;
  border-radius: 8px;
  color: rgb(0, 0, 0);
  margin-left: 40px;
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
  font-size: 48px;
  font-weight: 900;
  max-width: 550px;
}
.sidetext2{
  font-size: 36px;
}
.Readmore{
max-width: 200px;
border: solid rgb(92, 184, 214) 2px;
background-color: white;
color: rgb(92, 184, 214);
font-weight: 700;
padding: 10px;
margin-top: 20px;
cursor: pointer;
border-radius: 8px;
 transition-duration: 1s;
}
.Readmore:hover{
  transition-duration: 1s;
  background-color: rgb(206, 213, 225);
}
@media (max-width: 1260px) {
  .blockwrap1 {
    flex-direction: column;
    padding: 15px;
    margin: 15px;
  }
  .sidepicture {
    max-height: none;
    margin-right: 0;
    margin-top: 20px;
  }
  .sidetext1 {
    font-size: 36px;
    max-width: 100%;
  }
  .sidetext2 {
    font-size: 24px;
  }
}
@media (max-width: 786px) {
  .sidepicture{
    max-width: 450px;
    max-height: 250px;
  }
}

@media (max-width: 480px) {
  .sidetext1 {
    font-size: 28px;
  }
  .sidetext2 {
    font-size: 18px;
  }
  .Readmore {
    padding: 8px;
    font-size: 14px;
  }
}
</style>
<script>
export default{
      name: 'FirstBlock'
}
</script>