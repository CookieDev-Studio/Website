<template>
    <div>
        <div class="project-card-outer">
            <div class="project" v-if="leftAligned">
                <img :src="image" />
                <div class="project-description">
                    <h2>{{id}}: {{name}}</h2>
                    <p>{{description}}</p>
                    <v-btn :href="url" rounded class="btn project-btn">See project</v-btn>
                </div>
            </div>
            <div class="project" v-else>
                <div class="project-description">
                    <h2>{{id}}: {{name}}</h2>
                    <p>{{description}}</p>
                    <v-btn :href="url" rounded class="btn project-btn">See project</v-btn>
                </div>
                <img :src="image" />
            </div>             
        </div>
    </div>
</template>

<script>
export default {
    components: {},
    props: {
        id: Number,
        name: String,
        description: String,
        leftAligned: Boolean,
        url: String,
        image: String
    }
}
</script>

<style scoped>
.project-card-outer {
    width: 70vw;
    height: 300px;
    border-radius: 10px;
    background: #333;
    margin: 40px;
    display: flex;
}

.project {
    color: #fff;
    display: flex;
    width: 100%;
}

.project img {
    width: 65%;
}

.project-description {
    width: 35%;
    padding: 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.project-description h2 {
    font-size: 34px;
    font-weight: bold;
    margin-bottom: 5px;
    color: #ccc;
}

.project-description p {
    font-size: 16px;
    color: #eaba8e;
}

.project-btn {
    background-color: #a5844c !important;
    color: #fff;
}
</style>