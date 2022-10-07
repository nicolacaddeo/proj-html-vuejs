<template>
  <div id="jumbotron">
    <section>
        <img class="bg-image" src="../assets/img/jumbo.jpg" alt="jumbotron background">
        <!-- ? Nav Component -->
       <nav class="flex space-around align-center">
            <div>
                <NexGenComponent />
            </div>
            <div id="links" class="flex align-center">
                <ul class="flex">
                    <li v-for="link in navLinks" :key="link.id">
                        <a :href="link.url">{{ link.name }}</a>
                    </li>
                </ul>
                <GreenBtnComponent :buttonName = greenBtnName.getInTouch />
            </div>
       </nav>
       <!-- ? //Nav Component -->
    </section>
    <section id="logistics">
        <!-- *TODO: bg-green to h1 -->
        <h1>Logistics that goes further.</h1>
        <p>For 20 years working with the most innovative in the field of transport.</p>
        <div>
            <GreenBtnComponent :buttonName = greenBtnName.getInTouch />
            <TransparentBtnComponent :buttonName = greenBtnName.readMore />
        </div>
    </section>
</div>
</template>

<script>
import NexGenComponent from './subcomponents/NexGenComponent.vue';
import {navLinks} from '../data/jumbotronData.js';
import GreenBtnComponent from './subcomponents/GreenBtnComponent.vue';
import {greenBtnName} from '../data/greenBtnData.js';
import TransparentBtnComponent from './subcomponents/TransparentBtnComponent.vue';

export default {
    name: "JumboTronComponent",
    components: { NexGenComponent, GreenBtnComponent, TransparentBtnComponent },
    data() {
        return {
            navLinks,
            greenBtnName
        }
    }
}
</script>

<style scoped lang="scss">
    @import '@/style/global_variables.scss';

    #jumbotron {
        height: 90vh;
        background-position: center;
        position: relative;
        section{
            position: relative;
            .bg-image {
                position: absolute;
                z-index: -1;
                filter: brightness(50%);
                width: 100%;
                height: 90vh;
            }
            nav {
                padding: 2rem;
                #links{
                    ul {
                        list-style-type: none;
                        li {
                            padding: 0 1rem;
                            color: $header-links-color;
                            text-transform: uppercase;
                            font-weight: 600;
                            cursor: pointer;
                            a {
                                text-decoration: none;
                                color: inherit;
                            }
                        }
                    }
                }
            }
        }
        #logistics {
            width: 22vw;
            position: absolute;
            left: 55%;
            bottom: 25%;
            h1 {
                color: #fff;
                font-size: 4rem;
                line-height: 4.5rem;
            }
            p {
                color: $header-font-color;
                padding-top: 1.5rem;
                font-size: 1.5rem;
                line-height: 2rem;
            }
            div {
                padding-top: 2rem;
                * {
                    display: inline-block;
                    margin-right: 1.5rem;
                }
            }
        }
    }
            
</style>
           
            
                
        
        
