<template>
  <div id="header" class="flex"> 
    <!-- Contacts and JumboTron -->
    <section id="contacts" class="flex">
        <div>
            <font-awesome-icon icon="fa-solid fa-clock" />
            <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
        </div>
        <div class="flex">
            <div class="contact-phone">
                <font-awesome-icon icon="fa-solid fa-solid fa-phone" />
                +1 (305) 1234-5678
            </div>
            <div class="contact-mail">
                <font-awesome-icon icon="fa-solid fa-envelope" />
                hello@examples.com
            </div>
            <div class="social-icons">
                <font-awesome-icon icon="fa-brands fa-facebook-f" class="icon"/>
                <font-awesome-icon icon="fa-brands fa-twitter" class="icon"/>
                <font-awesome-icon icon="fa-brands fa-linkedin-in" class="icon"/>
            </div>
        </div>
    </section>
    <section id="jumbotron">

    </section>
  </div>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style scoped lang="scss">
    @import '../style/global_variables.scss';

    #contacts {
        color: $header-font-color;
        width: 100%;
        height: 5vh;
        padding: 1rem;
        background-color: $header-bg;
        justify-content: space-around;
        span {
            margin-left: .5rem;
        }
    }
    .contact-mail {
        margin: 0 2rem;
    }
    .social-icons {
        .icon {
            padding: 0 1rem;
        }
    }
</style>
       
        