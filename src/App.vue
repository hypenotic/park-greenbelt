<template>
    <div style="position: relative;">
        <app-header></app-header>
        <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/GreenbeltGrant_bg_pattern-03.png" alt="" class="decor-image decor-1">
        <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/GreenbeltGrant_bg_pattern-03.png" alt="" class="decor-image decor-2" v-if="this.$route.path == '/'">
        <img src="https://parkpeople.ca/listings/custom/uploads/2018/04/GreenbeltGrant_bg_pattern-03.png" alt="" class="decor-image decor-3" v-if="this.$route.path == '/'">
        <transition name="fade">
            <router-view :key="$route.fullPath"></router-view>
        </transition>
        <app-footer></app-footer>
        <div class="credits">
            <div class="container">
                <p>Made with <i class="fa fa-heart" aria-hidden="true"></i> by <a href="https://hypenotic.com" target="_blank">Hypenotic</a>.</p>
            </div>
        </div>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import Footer from './components/Footer.vue';
    export default {
    components: {
        appHeader: Header,
        appFooter: Footer
    }
}
</script>

<style lang="scss">

// Import Bulma's core
@import "~bulma/sass/utilities/_all";
@import url('https://fonts.googleapis.com/css?family=Dosis:400,700,800|Comfortaa|Merriweather');
// Import Variables
@import './styles/variables.scss';

$family-cursive: "Comfortaa", cursive;
$family-sanserif: "Dosis", sans-serif;
$serif: "Merriweather", serif;

html, body {
    font-size: 16px;
    line-height: 1.5;
    font-family: $family-cursive;
    color: $body-color;
    @media #{$medium-and-up} {
		font-size: 18px;
        line-height: 26px;
    }
}

.green {
    background-color: $darkGreen;
}

.decor-image {
    position: absolute;
    z-index: 0;
    opacity: 0.3;
}

.decor-1 {
    right: -40%;
    top: 70vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    @media #{$xlarge-and-up} {
        top: 500px;
        right: -200px;
    }
}

.decor-2 {
    left: -40%;
    top: 300vh;
    @media #{$xlarge-and-up} {
        left: -200px;
        top: 1600px;
    }
}

.decor-3 {
    right: -40%;
    top: 530vh;
    -webkit-transform: scaleX(-1);
    transform: scaleX(-1);
    @media #{$xlarge-and-up} {
        right: -200px;
        top: 3200px;
    }
}

.relative-div,
div {
    z-index: 1;
}

.credits {
    width: 100%;
    position: absolute;
    bottom: 0;
    p {
        margin: 0;
        font-size: 0.7rem;
        color: $white;
        text-align: right;
        padding: 16px;
        opacity: 0.4;
        a {
            color: $white;
            // text-decoration: underline;
            border-bottom: 1px solid $white;
        }
    }
}

a {
    color: $blue;
}

p {
    font-size: 1rem;
    line-height: 1.5rem;
    margin-top: 1.5rem;
    margin-bottom: 0;
    color: $body-color;
}

h1, h2, h3, h4, h5, h6 {
    font-weight: 500;
    line-height: 1.2;
    margin-top: 0;
    margin-bottom: 1rem;
    color: $body-color;
}

h1 {
    font-size: 5.063rem;
    margin-bottom: 0;
}

h2 {
    font-size: 1.5rem;
    @media #{$large-and-up} {
        font-size: 32px;
        line-height: 1.3;
    }
}

h3 {
    font-size: 2.75rem;
    @media #{$large-and-up} {
        font-size: 28px;
        line-height: 1.3;
    }
}

h4 {
    font-size: 2.25rem;
    @media #{$small-and-down} {
		font-size: 1.3rem;
    }
}

h5 {
    font-size: 1.833rem;
    @media #{$small-and-down} {
		font-size: 1.5rem;
    }
}

h6 {
    font-size: 1.222rem;
    font-weight: bold;
}

small {
    font-size: 0.815rem;
}

.fade-enter-active {
    transition: opacity .5s
}

.fade-leave-active {
    transition: opacity .5s
}

.wfs-loading {
    visibility: hidden;
}

.wfs-active, .wf-inactive {
    visibility: visible;
}

.card .content {
    p {
		font-size: 0.8rem;
		line-height: 1.3rem;
        margin-bottom: 0.8rem;
	}
}

.card__learn-list,
.card__activity-list,
.activity-list-container {
    font-family: $family-sanserif;
}

ol.resource__bullets {
	>li {
		ul, ol {
			list-style-type: disc;
			margin-left: 24px;
            padding-left: 10px;
            margin-top: 16px;
            li:not(:last-child) {
                margin-bottom: 8px;
            }
		}
	}
}

.resource__takeaways {
    h4 {
        font-size: 1.3rem;
        line-height: 1.8rem;
        font-weight: bold;
    }
}

.resource__excerpt p {
	font-size: 1.2rem;
	line-height: 1.8rem;
}

.case-study__context {
    blockquote{
        padding-left: 40px;
        padding-right: 15%;
        p {
            font-family: $serif;
            color: $green;
            font-size: 1.3rem;
            line-height: 1.8rem;
            font-style: italic;
        }
    }
}

.quote {
    max-width: 75%;
    margin: 0 auto;
    cite {
        display: block;
        text-align: right;
        margin-top: 8px;
    }
}

.full-width-quote {
    font-family: $serif;
    color: $green;
    font-size: 1.5rem;
    line-height: 2.2rem;
    font-style: italic;
    position: relative;
    &:after {
        content: '“';
        position: absolute;
        top: 0;
        left: -20px;
    }
}

// Grants

.topContent {
    margin: 32px 0;
    font-size: 1rem;
    color: $body-color;
    @media #{$medium-and-up} {
		 font-size: 1.2rem;
    }
    p {
        font-size: 1rem;
        line-height: 1.6;
        color: $body-color;
        @media #{$medium-and-up} {
		 font-size: 1.2rem;
         line-height: 1.5;
        }
    }
    a {
        border-bottom: 1px solid $blue;
        &:hover {
            color: $blue;
            font-weight: bold;
        }
    }
    ul {
        list-style-type: disc;
        margin-left: 40px;
        color: $body-color;
        li {
            margin-bottom: 8px;
            line-height: 1.5;
            color: $body-color;
        }
    }
    ul + p {
        margin-top: 1.5rem;
    }
    p + ul {
        margin-top: 0.8rem;
    }
    ul + h3 {
        // margin-top: 1.5rem;
    }
    h3 {
        margin-top: 3rem;
    }
}

.eligibility {
    a {
        border-bottom: 1px solid $blue;
        &:hover {
            color: $blue;
            font-weight: bold;
        }
    }
}


.more-info {
    // text-align: center;
    margin-top: 50px;
    margin-bottom: 50px;
    @media #{$medium-and-down} {
        padding: 0 24px;
    }
    @media #{$medium-and-up} {
		margin-top: 150px;
	}
    @media #{$large-and-up} {
		margin-top: 50px;
	}
    p, li {
		font-size: 1rem;
        line-height: 1.5;
        @media #{$large-and-up} {
			font-size: 1.1rem;
            line-height: 1.7;
		}
    }
    h4,h5 {
        color: $orange;
    }
    h4 {
        // margin-bottom: 8px;
        line-height: 1.5;
    }
    h4 strong {
        color: $orange !important;
    }
    h5 {
        font-size: 1.2rem;
        font-weight: bold;
        line-height: 1.5;
        @media #{$medium-and-up} {
            font-size: 1.3rem;
        }
    }
    ul {
        margin-left: 48px;
        list-style-type: disc;
        li {
            list-style-type: disc;
            margin-bottom: 20px;
        }
    }
    a {
        border-bottom: 1px solid $blue;
        &:hover {
            color: $blue;
            font-weight: bold;
        }
    }
}

strong {
    color: $body-color;
}

// Newsletter 
.mailchimp-form-container {
    #MERGE0{
        border: 2px dashed rgb(17, 116, 191) !important;
        min-width: 400px;
        // max-width: 300px;
        padding: 2px 16px;
        border-radius: 8px;
        min-height: 45px;
        font-size: 0.8rem;
        font-family: $family-cursive;
        background-color: rgb(242, 248, 252);
        &:focus,
        &:active {
            background-color: $white;
        }
    }   
    #mc-embedded-subscribe {
        border-radius: 50px;
        background-color: $blue;
        color: $white;
        box-shadow: none;
        border: 2px solid $blue;
        min-height: 45px;
        padding: 0 42px;
        font-family: $family-sanserif;
        font-weight: bold;
        margin-left: 16px;
        border: 2px solid $blue;
        &:hover {
            border: 2px solid $blue;
            color: $blue;
            background: $white;
        }
    }
}


.FAQ-content {
	h2 {
		font-size: 1.3rem;
		line-height: 1.5;
	}
    p + h2 {
        margin-top: 40px !important;
    }
    span {
        color: $off-black !important;
    }
	ul {
		margin: 20px 0 0 40px;
		li {
			line-height: 1.5;
			margin-bottom: 1rem;
			list-style-type: disc;
			font-size: 1rem;
			padding-left: .6em;

		}
	}
}

// Footer
footer {
    font-size: 0.8rem;
    p, ul, li {
        font-size: 0.8rem;
    }
}

.topContent {
    p:first-child {
		margin-top: 0;
    }
    p {
        font-size: 18px;
        line-height: 1.5;
        @media #{$large-and-up} {
            font-size: 26px;
            line-height: 1.5;
        }
    }
    a {
        text-decoration: none;
        border-bottom: none;
        &:hover {
            font-weight: normal;
            border-bottom: 1px solid $blue;
        }
    }
}

a {
    text-decoration: none;
    border-bottom: none;
    &:hover {
        color: $blue;
        font-weight: normal;
        border-bottom: 1px solid $blue;
    }
}

.sidebar {
	h3 {
        font-size: 18px;
        font-family: $family-sanserif;
        font-weight: bold;
        margin: 0;
    }
    p {
        margin: 16px 0;
        font-size: 16px;
        line-height: 1.5;
    }
}

.download-button {
    color: $white;
    background: $orange;
    border-radius: 50px;
    padding: 10px 32px;
    font-weight: bold;
    display: inline-block;
    margin: 16px 0 24px;
    font-family: "Dosis", sans-serif;
    i {
        margin-right: 10px;
    }
    &:hover {
        color: $white;
        border: none;
        font-weight: bold;
        background: darken($orange, 10)
    }
}

.copy-container {
    padding: 40px 32px;
    @media #{$large-and-up} {
        padding: 100px 80px;
    }
    ul {
        padding-left: 32px;
        @media #{$xlarge-and-up} {
            padding-left: 40px;
        }
    }
    ul, li {
        list-style-type: disc;
        font-size: 16px;
        line-height: 1.5;
    }
    li {
        margin-bottom: 16px;
    }
    h4 {
        font-family:"Dosis", sans-serif;
        font-size: 20px;
        line-height: 1.5;
        font-weight: bold;
    }
}
</style>