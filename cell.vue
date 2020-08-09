<template>
  <rect  v-on:click="push()" @mouseover="hover()" width="100" height="100" v-bind:x="100*x" :y="100*y" stroke="black" :fill="pallet[v]" fill-opacity=0.5></rect>
</template>

<script>
export default {
    
    props:['x','y','v','idx'],
    data: function(){
	return {
	    pallet: ["gray","yellow"],
	}
    },
    methods:{
	push: function(){
	    this.$emit("toggle", this.idx);
	},
	hover: function(){
	    this.$emit("hover", this.idx);
	}
    }

}
</script>
