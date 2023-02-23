<template>
    <header>
        <h1>{{title}}</h1>
        <Button 
        @btn-click="$emit('toggle-add-task')" 
        :text="showAddTask ? 'Close' : 'Add List'" 
        :color="showAddTask ? 'red' : 'green'" 
        />
        <!--<Button text="Update Listing" color="blue" />
        <Button text="Delete Listing" color="red" />-->
    </header>
</template>

<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: {
            type: String,
            default: 'THis is default',
        },
        showAddTask: Boolean
    },
    components: {
        Button
    }
}

</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>
