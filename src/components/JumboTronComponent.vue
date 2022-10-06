<template>
  <div id="jumbotron">
    <section>
        <img class="bg-image" src="../assets/img/jumbo.jpg" alt="jumbotron background">
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
    </section>
  </div>
</template>

<script>
import NexGenComponent from './NexGenComponent.vue';
import {navLinks} from '../data/jumbotronData.js';
import GreenBtnComponent from './GreenBtnComponent.vue';
import {greenBtnName} from '../data/greenBtnData.js';

export default {
    name: "JumboTronComponent",
    components: { NexGenComponent, GreenBtnComponent },
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
    }
            
</style>
        
        
