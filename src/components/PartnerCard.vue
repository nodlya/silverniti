<template>
    <div class="card">
        <img alt="Image" :src="imageLink">
        <div class="right-section">
            <p>{{ partnerName }}</p>
            <partner-link />
        </div>
    </div>
</template>

<script>
import PartnerLink from './PartnerLink.vue';

export default {
    name: "PartnerCard",
    components: {
        PartnerLink
    },

    props: {
        partnerName: {
            type: String,
            default: ""
        },

        partnerLogoName: {
            type: String,
            default: "0"
        },

        partnerLinkList: {
            type: Array,
            default: new Array
        }
    },

    computed: {
        imageLink() {
            return `/src/assets/partners_logo/${this.partnerLogoName}`;
        }
    }

};
</script>

<style scoped>
.card {
    display: flex;
    background-color: #F7F7F7;
    padding: 8px;
}

.right-section {
    margin-left: 8px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-end;
    padding: 4px;
    color: black;
}

img {
    width: auto;
    height: 64px;
}

.bottom-section {
    padding: 10px;

}
</style>