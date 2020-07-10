<template>
    <div>
        {{id}}: {{name}}
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