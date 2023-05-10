<script>

export default {
    props: {
        imagePath: String,
        Title: String,
        subTitle: String
    }
}

</script>


<template>
    <section>
        <main id="card">
            <img :src="imagePath" alt="">
            <p>{{ Title }}</p>
            <p class="sub">{{ subTitle }}</p>
        </main>
    </section>
    <br>
</template>

<style scoped>
main img {
    height: 330px;
}

p {
    font-weight: 600;
    font-size: 1.5rem;
}

.sub {
    font-weight: 400;
    font-size: 1rem;
}
</style>