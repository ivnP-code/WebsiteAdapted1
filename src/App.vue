<template>
<div>
 <Nav />
    <FirstBlock />
    <Blogs />
    <Rows />
    <InfoFooter />
</div>  
</template>

<style>
*{
    padding: 0;
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;

}
html, body {
  overflow-x: hidden;
}

</style>

<script>
import Nav from './components/nav.vue';
import FirstBlock from './components/firstblock.vue';
import Blogs from './components/blogs.vue';
import Rows from './components/rows.vue';
import InfoFooter from './components/infofooter.vue';

export default {
    components:{
        Nav,
        FirstBlock,
        Blogs,
        Rows,
        InfoFooter
      }
}
</script>
