<template>
    <section>
        <div class="parking-box">
            <img :src="parking.imageURL" alt="">
                <h3>{{parking.address}}</h3>
                <p>{{parking.price}}$</p>
                <p>distance:?</p>
                <div class="flex space-around">
                    <p>{{parking.amenities.isCovered}}</p>
                    <p>{{parking.amenities.isForDisable}}</p>
                    <p>{{parking.amenities.isPaved}}</p>
                </div>
                <div class="flex justify-content-c">
                    <button class="btn btn-details">Details</button>
                    <button @click.prevent="$router.push('/reserve')">Reserve</button>
                </div>
            </div>
    </section>
</template>

<script>

export default {
    props:{
        parking:Object,

    },
}
</script>

<style scoped>

.parking-box{
    border: 1px solid gray;
}
.flex{
    display: flex;
}

.space-around{
    justify-content: space-around;
}

.justify-content-c{
    justify-content: center
}

button{
    cursor: pointer;
}
img{
    width: 200px;
}
</style>
