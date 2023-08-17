<template>
    <div>
        <a :href="url">
            <span>{{ type }}</span>
            <img src="../assets/link.png" />
        </a>
    </div>
</template>

<script>
export default { 
    name: "PartnerLink",
    props: {
        type: {
            type: String, 
            default: ""
        },

        url: {
            type: String,
            default: ""
        }
    }
};
</script>

<style scoped>
div {
    color: black;
}
a {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 5px;
    font-size: 16px;
    text-transform: uppercase;
}

img {
    height: 16px;
    width: auto;
}
</style>