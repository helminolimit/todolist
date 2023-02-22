<template>
    <header>
        <h1>{{title}}</h1>
        <Button text="Add Listing" color="green" />
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
            default: 'THis is default'
        }
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
