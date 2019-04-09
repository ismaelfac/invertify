<template>
    <v-flex class="content">
        <v-flex class="slider-home" v-if="isSlider">
            <slider></slider>
        </v-flex>
        <v-layout row wrap>
            <v-flex xs12 v-if="isSearchProperty">
                <v-card dark color="#95c41f">
                <v-card-text>{{lorem}}</v-card-text>
                </v-card>
            </v-flex>
            <v-container>
                <v-layout align-center justify-center row fill-height>
                    <v-flex xs6>
                        <div class="section-title mb-30">
                            <h3>INVERSIONES &</h3>
                            <h2>PROYECTOS</h2>
                        </div>
                        <div class="about-sheltek-info">
                            <p><span data-placement="top" data-toggle="tooltip" data-original-title="The name you can trust" class="tooltip-content">Sheltek</span> is the best theme for  elit, sed do eiusmod tempor dolor sit amet, conse ctetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et lorna aliquatd minim veniam, quis nostrud exercitation oris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolo.</p>
                            <div class="author-quote">
                                <p>Lorem is a dummy text do eiusmod tempor dolor sit amet, onsectetur adip iscing elit, sed do eiusmod tempor incididunt ut labore et lorna aliqua Ut enim onsectetur </p>
                                <p>Lorem is a dummy text do eiusmod tempor dolor sit amet, onsectetur adip iscing elit, sed do eiusmod tempor incididunt ut labore et lorna aliqua Ut enim onsectetur </p>
                            </div>
                        </div>
                    </v-flex>
                    <v-flex xs6>
                        <div class="about-image">
                            <a href="about.html"><img src="https://devitems.com/html/sheltek-preview/sheltek/images/about/2.jpg" alt=""></a>
                        </div>
                    </v-flex>
                </v-layout>
            </v-container>
            <v-flex xs6 offset-xs1>
                <properties-home></properties-home>
            </v-flex>
            <v-flex xs4>
                <classifield-home></classifield-home>
            </v-flex>
            <v-flex xs10 offset-xs1>
                
                
            </v-flex>
        </v-layout>  
    </v-flex>
</template>
<script>
import Slider from '../../components/shared/slider/Slider'
import PropertiesHome from '../../components/shared/properties/PropertiesHome'
import ClassifieldHome from '../../components/shared/classifields/ClassifieldsHome'
export default {
    name: 'Content',
    components: {
        Slider,
        PropertiesHome,
        ClassifieldHome
    },
    data: () => ({
        isSlider: true,
        isSearchProperty: true,
        lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`
    })
}
</script>
<style lang="scss" scoped>

</style>

