<template>
    <div>
        <b-col>
            <b-card 
                :title="name" 
                img-src="https://cdn.pixabay.com/photo/2020/11/08/09/41/deer-5723225_960_720.jpg" 
                :img-alt="name" 
                tag="article" 
                style="max-width:20rem"
                class="mb-2"
                :footer="tijd"
                >


                <b-card-text>hier komt json</b-card-text>
                <b-button v-b-tooltip.hover :title="name" variant="primary">meer informatie</b-button>
            </b-card>
        </b-col>
    </div>
</template>
<script>
export default {
    props: ['name', 'tijd']
}
</script>

<style lang="scss" scoped>
.card-footer{
        background-color: #EE7B00!important;
        color:white;
}
</style>