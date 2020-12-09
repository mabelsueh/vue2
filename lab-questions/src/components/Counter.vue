<template>
<div>
    <h2>{{count}}</h2>
    <button @click="increase">Increase by 1</button>
    <button @click="decrease">Decrease by 1</button>
</div>
</template>

<script>
export default {
    data: function() {
        return {count: 0}
    },
    methods: {
        increase: function (){
            this.count +=1;
        },
        decrease: function(){
            this.count -=1;
        }
    }
    
}
</script>