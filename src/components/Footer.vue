<template>
    <div>  
        <footer v-if="this.$route.path == '/faq'">
            <div>
                <div class="columns">
                    <div class="column is-6 green" style="color: white;">
                        <div class="columns is-centered">
                            <div class="column is-10 collab-footer">
                                <p>Made possible by a great collaboration:</p>
                                <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/greenbelt_Logo.png">
                                <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/parkpeople-logo.png" alt="">
                            </div>
                        </div>
                    </div>
                    <div class="column is-6 green" style="color: white;">
                        <div class="columns">
                            <div class="column is-6">
                                <ul>
                                    <li style="color: white;font-weight: bold;">Park People</li>
                                    <li>401 Richmond Street West</li>
                                    <li>Studio 119, City Builder’s Lab</li>
                                    <li>Toronto, ON M5V 3A8</li>
                                </ul>
                                <ul class="details">
                                    <li>Phone: <a href="tel:+14165835776">416-583-5776</a></li>
                                    <li>Email: <a href="mailto:info@parkpeople.ca">info@parkpeople.ca</a></li>
                                    <li>Charity #: 846449437RR0001</li>
                                </ul>
                                <ul class="social-links">
                                    <li><a href="https://parkpeople.ca/" target="_blank"><i class="fas fa-home"></i></a></li>
                                    <li><a href="https://twitter.com/Park_People" target="_blank"><i class="fab fa-twitter"></i></a></li>
                                    <li><a href="https://www.facebook.com/ParkPeopleTO/" target="_blank"><i class="fab fa-facebook-f"></i></a></li>
                                </ul>
    
                            </div>
                            <div class="column is-6">
                                <a class="button" href="https://parkpeople.ca/donate-now" target="_blank">Donate</a>
                            </div>
    
                        </div>
                    </div>
                </div>
            </div>
        </footer> 
        <footer v-else class="footer-grants">
            <div>
                <div class="columns">
                    <div class="column is-6 green" style="color: white;">
                        <div class="columns is-centered">
                            <div class="column is-10 collab-footer">
                                <p>Made possible by a great collaboration:</p>
                                <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/greenbelt_Logo.png">
                                <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/parkpeople-logo.png" alt="">
                            </div>
                        </div>
                    </div>
                    <div class="column is-6 green" style="color: white;">
                        <div class="columns">
                            <div class="column is-6">
                                <ul>
                                    <li style="color: white;font-weight: bold;">Park People</li>
                                    <li>401 Richmond Street West</li>
                                    <li>Studio 119, City Builder’s Lab</li>
                                    <li>Toronto, ON M5V 3A8</li>
                                </ul>
                                <ul class="details">
                                    <li>Phone: <a href="tel:+14165835776">416-583-5776</a></li>
                                    <li>Email: <a href="mailto:info@parkpeople.ca">info@parkpeople.ca</a></li>
                                    <li>Charity #: 846449437RR0001</li>
                                </ul>
                                <ul class="social-links">
                                    <li><a href="https://www.instagram.com/parkppl/" target="_blank"><i class="fab fa-instagram"></i></a></li>
                                    <li><a href="https://twitter.com/Park_People" target="_blank"><i class="fab fa-twitter"></i></a></li>
                                    <li><a href="https://www.facebook.com/ParkPeopleTO/" target="_blank"><i class="fab fa-facebook-f"></i></a></li>
                                </ul>
    
                            </div>
                            <div class="column is-6">
                                <a class="button" href="https://parkpeople.ca/donate-now" target="_blank">Donate</a>
                            </div>
    
                        </div>
                    </div>
                </div>
            </div>
        </footer> 
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

    // Import Variables
    @import '../styles/variables.scss';

    .collab-footer {
        text-align: center;
        p {
            margin-bottom: 40px;
        }
        img {
            margin: 0 30px;
        }
    }

    .button {
        color: $white;
        background-color: $blue;
        font-family: $family-sanserif;
        font-weight: bold;
        border: 2px solid $blue;
        border-radius: 50px;
        padding: 8px 24px;
        &:hover {
            border: 2px solid $blue;
            background-color: $white;
            color: $blue; 
        }
    }

    footer {
        font-size: 0.8rem;
        p, ul, li {
            font-size: 0.8rem;
        }
        ul + ul {
            margin-top: 16px;
        }
    }

    footer {
        position: relative;
        padding-top: 150px;
        > div {
            position: relative;
            &:before {
                content: '';
                position: absolute;
                z-index: 5;
                left: 0;
                top: -70px;
                width: 100%;
                height: 160px;
                background: #fff;
                -webkit-transform: skewY(5deg);
                -moz-transform: skewY(5deg);
                -ms-transform: skewY(5deg);
                -o-transform: skewY(5deg);
                transform: skewY(5deg);
                -webkit-backface-visibility: hidden;
            }
        }
    }

    footer.footer-grants {
        position: relative;
        margin-top: 100px;
        padding-top: 60px;
        > div {
            position: relative;
            &:before {
                content: '';
                position: absolute;
                left: 0;
                top: -70px;
                width: 100%;
                height: 130px;
                background: #fff;
                @media #{$large-and-up} {
                    -webkit-transform: skewY(5deg);
                    -moz-transform: skewY(5deg);
                    -ms-transform: skewY(5deg);
                    -o-transform: skewY(5deg);
                    transform: skewY(5deg);
                }
                @media #{$xlarge-and-up} {
                    -webkit-transform: skewY(3deg);
                    -moz-transform: skewY(3deg);
                    -ms-transform: skewY(3deg);
                    -o-transform: skewY(3deg);
                    transform: skewY(3deg);
                }
            }
        }
    }

    footer >div >div >div {
        padding-top: 80px;
        padding-left: 40px;
        padding-right: 40px;
        @media #{$medium-and-up} {
           padding-top: 200px;
        }
    }
    footer >div >div >div:first-child {
        background: rgb(249, 249, 249);
    }
    footer >div >div >div:last-child {
        padding: 40px;
        @media #{$medium-and-up} {
            padding: 200px 80px 80px;
        }
    }

    footer img {
        max-width: 150px;
        height: auto;
        padding-top: 0px;
    }

    .social-links {
        li {
            display: inline-block;
            a {
                color: white;
                &:hover {
                    opacity: 0.6;
                }
            }
            i {
                font-size: 32px;
            }
        }
        li + li {
            margin-left: 16px;
        }
    }
    .details a {
        color: white;
        text-decoration: underline;
        &:hover {
            text-decoration: none;
        }
    }
</style>