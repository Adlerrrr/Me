<template>
    <div class="container">
        <div class="subcontainer">
            <Title />
            <Carreer />
        </div>

    </div>

</template>

<script>
import Title from './Title.vue'
import Carreer from './Carreer.vue'


export default {
    name: 'Resume',
    components: {
        Title,
        Carreer
    },
    data() {
        return {

        }
    }
}
</script>

<style scoped>
div .container {
    background-color: rgb(46, 46, 46);
    max-width: 1024px;
    margin: 32px auto;
    border-radius: 32px;

}
.subcontainer{
    display: flex;
    justify-content: space-around;
}

</style>