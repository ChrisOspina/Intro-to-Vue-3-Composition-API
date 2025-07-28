<script setup>
defineProps({
    reviews:{
        type: Array,
        required: true
    }
})
</script>

<template>
    <div class="review-container">
        <h3>Reviews:</h3>
        <ul>
            <li v-for="(review,index) in reviews" :key="index">
                <span>{{ review.name }} gave this {{ review.rating }} stars</span>
                <br/>
                <span>"{{ review.content }}"</span>
                <span v-if="review.recommendation = 'yes'">I reccomend this product</span>
                <span v-else>I do not reccomend this product</span>
            </li>
        </ul>
    </div>
</template>