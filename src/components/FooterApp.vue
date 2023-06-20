<script>
export default {
    data() {
        return {
            sections: [
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-digital-comics.png'
                },
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-merchandise.png'
                },
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-digital-comics.png'
                },
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-digital-comics.png'
                },
                {
                    sectionName:'DIGITAL COMICS',
                    sectionImage: 'buy-comics-digital-comics.png'
                },
            ]
        }
    },
}
</script>
<template lang="">
    <div>
        <div class="comntainer">
            <div class="blue-section">
                <ul>
                    <li v-for="(section, index) in sections" :key="index">
                        <img :src="'./assets/img/' +  section.sectionImage" alt="">
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/varables' as *;
    .blue-section{
        background-color: $color_primary;
    }
</style>