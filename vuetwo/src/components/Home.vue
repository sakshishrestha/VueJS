<template>
    <div>
        <h1>Home Component</h1>
        <h2>{{ data }}</h2>
        <!--v-on click event in vuejs-->
        <button v-on:click="hello('hello call')">Call Hello Function</button> 
        <!--v-if v-else conditional rendering-->
        <h1 v-if="show">Conditional Rendering If block </h1>
        <h1 v-else>Conditional Rendering Else block</h1>
        <button v-on:click="display">Toogle ELement</button>
    </div>
</template>
<script>
export default {
    name:'Home',
    props:{
        data:String
    },data(){
        return {show:true}
    },methods:{
        hello(data){
            alert(data)
        },
        display(){
            this.show=!this.show
        }
    }
}
</script>