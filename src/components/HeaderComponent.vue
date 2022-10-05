<template>
  <div id="header" class="flex"> 
    <!-- Contacts Info -->
    <section id="contacts" class="flex">
        <div>
            <font-awesome-icon icon="fa-solid fa-clock" />
            <span>
                Open Hours: {{ openHours.openDay }} - {{ openHours.closingDay }} - {{ openHours.openingTime }} - {{ openHours.closingTime }}
            </span>
        </div>
        <div class="flex">
            <div class="contact-phone">
                <font-awesome-icon icon="fa-solid fa-solid fa-phone" />
                {{ phoneNumber }}
            </div>
            <div class="contact-mail">
                <font-awesome-icon icon="fa-solid fa-envelope" />
                {{ email }}
            </div>
            <div class="social-icons">
                <font-awesome-icon icon="fa-brands fa-facebook-f" class="icon"/>
                <font-awesome-icon icon="fa-brands fa-twitter" class="icon"/>
                <font-awesome-icon icon="fa-brands fa-linkedin-in" class="icon"/>
            </div>
        </div>
    </section>
  </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return{
            phoneNumber: '+1 (305) 1234-5678',
            email: 'hello@examples.com',
            openHours: {
                openDay: 'Mon',
                closingDay: 'Sat',
                openingTime: '9:00',
                closingTime: '18:00'
            }
        }
    }
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
       
        