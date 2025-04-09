<template>
<div class="post-card"> 
    <h3>Título</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur vehicula, nisi a efficitur suscipit, ligula metus dapibus magna, in volutpat nulla ipsum id ex. Vestibulum accumsan sit amet turpis non dictum. Phasellus cursus, tortor ac elementum gravida, ipsum purus mollis odio, sit amet aliquam arcu lorem vel ipsum. Fusce convallis purus id mi scelerisque, et dapibus orci auctor. Ut pretium dui ut nisl hendrerit, ut dignissim leo tincidunt. Integer sed nulla ut turpis tincidunt pretium. Fusce nec urna a urna cursus fermentum. Nulla sit amet cursus enim, ac maximus ex. Vivamus feugiat, eros ac dictum egestas, velit purus convallis lorem, eget euismod ligula libero a velit. Donec et sapien nec augue mollis facilisis at sit amet augue. Fusce a
    </p>
    <PostButton/>
</div>

</template>

<script setup>
import PostButton from './PostButton.vue'
</script>

<style>
.post-card{
border-radius: 15px;
padding: 10px;
margin: 5px;
border: 1px solid #ccc;

}
</style>