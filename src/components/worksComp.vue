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
    <main>
        {{ imagePath }}
        {{ Title }}
        {{ subTitle }}
    </main>
</template>

<style scoped>
main {
    color: red;
}
</style>