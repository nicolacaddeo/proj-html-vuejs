<template>
  <div id="jumbotron">
    <section>
        <img class="bg-image" src="../assets/img/jumbo.jpg" alt="jumbotron background">
       <nav class="flex space-around" >
            <div>
                <NexGenComponent />
            </div>
            <div id="links">
                <ul class="flex">
                    <li v-for="link in navLinks" :key="link.id">
                        <a :href="link.url">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
       </nav>
    </section>
  </div>
</template>

<script>
import NexGenComponent from './NexGenComponent.vue';
import {navLinks} from '../data/jumbotronData.js';

export default {
    name: "JumboTronComponent",
    components: { NexGenComponent },
    data() {
        return {
            navLinks
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
        
        
