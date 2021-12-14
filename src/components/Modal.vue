<template>
    <div class="backdrop" @click="closeModal">
        <div class="modal">
            <h1>{{header}}</h1>
            <p>{{text}}</p>
            <!-- <a href="">{{btn}}</a> -->
        </div>
    </div>
</template>

<script>
export default {
    props: ['header', 'text', 'btn'],
    data(){
        return {
        showModal: false
        }
    },
    methods: {
        closeModal(){
            //this.showModal = !this.showModal
            this.$emit('close')
        }
    }
}
</script>

<style>
.backdrop {
    background-color: rgba(0,0,0,.5);
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    bottom: 0;
}
.modal {
    background-color: #fff;
    max-width: 550px;
    margin: 100px auto;
    padding: 20px;
    border-radius: 5px;
}
</style>