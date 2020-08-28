<template>
    <div>
        <a class="card-href" :href="url" target="_blank">
            <div class="project-card-outer">
                <div class="project" v-if="leftAligned">
                    <img :src="image" />
                    <div class="image-mobile-overlay">
                        <h2>{{id}}: {{name}}</h2>
                        <v-btn :href="url" target="_blank" rounded class="btn project-btn">See project</v-btn>
                    </div>
                    <div class="project-description">
                        <h2>{{id}}: {{name}}</h2>
                        <p>{{description}}</p>
                        <v-btn :href="url" target="_blank" rounded class="btn project-btn">See project</v-btn>
                    </div>
                </div>
                <div class="project" v-else>
                    <div class="project-description">
                        <h2>{{id}}: {{name}}</h2>
                        <p>{{description}}</p>
                        <v-btn :href="url" target="_blank" rounded class="btn project-btn">See project</v-btn>
                    </div>
                    <img :src="image" />
                    <div class="image-mobile-overlay">
                        <h2>{{id}}: {{name}}</h2>
                        <v-btn :href="url" target="_blank" rounded class="btn project-btn">See project</v-btn>
                    </div>
                </div>             
            </div>
        </a>
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
.card-href {
    text-decoration: none;
    color: none;
}

.project-card-outer {
    width: 70vw;
    height: 300px;
    border-radius: 10px;
    background: #333;
    margin: 40px;
    display: flex;
    cursor: pointer;
}

.project {
    color: #fff;
    display: flex;
    width: 100%;
}

.image-mobile-overlay {
    display: none;
}

.project img {
    width: 65%;
    object-fit: cover;
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

@media (max-width: 900px) {
    .project-description h2 {
        font-size: 28px;
    }

    .project-description p {
        font-size: 14px;
    }
}

@media (max-width: 790px) {
    .project {
        border: .5px solid rgb(189, 82, 82); 
        border-radius: 5px;
    }
    .project-description {
        display: none;
    }

    .project img {
        width: 100%;
    }

    .image-mobile-overlay {
        display: block;
        position: absolute;
        width: 69.5vw;
        padding: 30px;
        text-align: center;
        margin-top: 70px;
        background: rgba(0, 0, 0, 0.85); 
        border-radius: 5px;
    }

    .image-mobile-overlay h2 {
        font-size: 28px;
    }

    .image-mobile-overlay p {
        font-size: 14px;
    }
}
</style>