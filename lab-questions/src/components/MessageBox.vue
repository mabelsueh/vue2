// you need a template (view)
// can only accept ONE parent element (need to put more than one div all in one big div)
<template>
<div>
    <div>
        <!-- <h1 style="backgroundColor:pink">{{message}}</h1> -->
        <!-- use js syntax in v-bind -->
        <h1 v-bind:style="{'backgroundColor': bgcolor}">{{message}}</h1>
    </div>
    <div>
        Two
    </div>    
</div>
</template>


// you need a script (model & controller)
<script>
export default {
    data: function() {
        return{
            'messages': "The quick brown fox jumps over the lazy dog."
        }
    },
    props:['message', 'bgcolor']
}
</script>


// you need a style (styler)

// scoped limits the styling to the particular .vue app
<style scoped>
    div {
    background-color: blue;
    }

</style>