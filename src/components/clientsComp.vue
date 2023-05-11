<script>

import star from '@/assets/clients/star.png'

export default {
    props: {
        imagePath: String,
        title: String,
        name: String
    },
    data() {
        return {
            'star': star
        }
    }

}

</script>


<template>
    <section>
        <main id="content">

            <p>{{ title }}</p>

            <div>
                <img :src="imagePath" alt="" id="personal">
                <div id="star">
                    <div v-for="x in 5">
                        <img :src="star" alt="">
                    </div>
                </div>
                <p class="sub">{{ name }}</p>


            </div>
        </main>
    </section>
</template>


<style scoped>
section {
    display: flex;
    justify-content: center;

    margin-top: 50px;
    margin-bottom: 50px;
}

@media (max-width: 600px) {
    section {
        margin-top: 10px;
        margin-bottom: 10px;
    }
}

section:hover {
    opacity: 0.8;
    box-shadow: 10px 10px 20px rgb(228, 228, 228);
}

#content {
    padding-top: 20px;
    padding-left: 20px;
    padding-right: 40px;
    padding-bottom: 20px;

    height: 400px;
    width: 330px;
    color: black;
    background-color: #F3F3F3;

    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    text-align: center;

}

#content p {
    font-weight: 500;
    font-size: 1.2rem;
    text-align: left;
}

#content .sub {
    font-weight: 400;
    font-size: 1rem;
}

#personal {
    height: 60px;
}

#star {
    width: 100%;
    display: flex;
    justify-content: center;

}

#star img {
    margin: 5px;
    height: 15px;
}
</style>