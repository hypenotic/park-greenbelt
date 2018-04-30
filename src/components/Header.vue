<template>
    <nav v-if="scrolled == true" id="scrolling" class="navbar green">
        <div class="navbar-brand">
            <div>
                <!-- <a href="https://parkpeople.ca"><img src="https://parkpeople.ca/listings/custom/themes/parkpeople/dist/images/parkpeople-logo-PMS.png" class="grants-logo"></a> -->
                <div class="social-share-container">
					<div id="social-share-trigger" v-bind:class="{ 'social-menu-open': showSocialShare }" v-on:click="showSocialShare = !showSocialShare">
						<i class="fa fa-share-alt" aria-hidden="true"></i> Tell someone!
					</div>
					<social-sharing :url="`https://parkpeople.ca/possibilityflowshere`"
					title="Park People | Greenbelt River Valley Connector Program"
					description="Over the next three years, through a collaboration between The Greenbelt Foundation and Park People, the Greenbelt River Valley Connector Program will provide grants to support fifteen place-based community projects across the GTHA that will celebrate and enhance these natural valley areas."
					quote=""
					hashtags="PossibilityFlowsHere"
					twitter-user="Park_People"
					inline-template>
					<div class="social-share-buttons">
						<network network="email">
							<i class="far fa-envelope"></i>
						</network>
						<network network="twitter">
							<i class="fab fa-twitter"></i>
						</network>
						<network network="facebook">
							<i class="fab fa-facebook-f"></i>
						</network>
						<network network="linkedin">
							<i class="fab fa-linkedin-in"></i>
						</network>
					</div>
					</social-sharing>
				</div>
            </div>
        </div>

        <!-- <div class="lang">
            <a v-if="this.$route.path == '/faq'" href="https://parkpeople.ca/boursesdeparc/faq">FR</a>
            <a v-else href="https://parkpeople.ca/boursesdeparc">FR</a>
        </div> -->

         <div id="mobile-menu-trigger" v-on:click="showMobileMenu = !showMobileMenu">
            <i class="fa fa-bars" aria-hidden="true"></i>
        </div>

        <div id="navbarExampleTransparentExample" class="navbar-menu" v-bind:class="{ 'menu-open': showMobileMenu }">
            <div class="navbar-end">
                <span class="navbar-item" v-on:click="showMobileMenu = !showMobileMenu" v-if="this.$route.path == '/'"><router-link to="/faq"  exact>FAQ</router-link></span>
                <span class="navbar-item" v-on:click="showMobileMenu = !showMobileMenu" v-if="this.$route.path == '/faq'"><router-link to="/" exact>Back </router-link></span>
                <a href="https://parkpeople.ca" class="navbar-item">ParkPeople.ca</a>
            </div>
        </div>
    </nav>
    <nav v-else class="navbar green">
        <div class="navbar-brand">
            <div>
                <!-- <a href="https://parkpeople.ca"><img src="https://parkpeople.ca/listings/custom/themes/parkpeople/dist/images/parkpeople-logo-PMS.png" class="grants-logo"></a> -->
                <div class="social-share-container">
					<div id="social-share-trigger" v-bind:class="{ 'social-menu-open': showSocialShare }" v-on:click="showSocialShare = !showSocialShare">
						<i class="fa fa-share-alt" aria-hidden="true"></i> Tell someone!
					</div>
					<social-sharing :url="`https://parkpeople.ca/possibilityflowshere`"
					title="Park People | Greenbelt River Valley Connector Program"
					description="Over the next three years, through a collaboration between The Greenbelt Foundation and Park People, the Greenbelt River Valley Connector Program will provide grants to support fifteen place-based community projects across the GTHA that will celebrate and enhance these natural valley areas."
					quote=""
					hashtags="PossibilityFlowsHere"
					twitter-user="Park_People"
					inline-template>
					<div class="social-share-buttons">
						<network network="email">
							<i class="far fa-envelope"></i>
						</network>
						<network network="twitter">
							<i class="fab fa-twitter"></i>
						</network>
						<network network="facebook">
							<i class="fab fa-facebook-f"></i>
						</network>
						<network network="linkedin">
							<i class="fab fa-linkedin-in"></i>
						</network>
					</div>
					</social-sharing>
				</div>
            </div>
        </div>

        <!-- <div class="lang">
            <a v-if="this.$route.path == '/faq'" href="https://parkpeople.ca/boursesdeparc/faq">FR</a>
            <a v-else href="https://parkpeople.ca/boursesdeparc">FR</a>
        </div> -->

         <div id="mobile-menu-trigger" v-on:click="showMobileMenu = !showMobileMenu">
            <i class="fa fa-bars" aria-hidden="true"></i>
        </div>

        <div id="navbarExampleTransparentExample" class="navbar-menu" v-bind:class="{ 'menu-open': showMobileMenu }">
            <div class="navbar-end">
                <span class="navbar-item" v-on:click="showMobileMenu = !showMobileMenu" v-if="this.$route.path == '/'"><router-link to="/faq"  exact>FAQ</router-link></span>
                <span class="navbar-item" v-on:click="showMobileMenu = !showMobileMenu" v-if="this.$route.path == '/faq'"><router-link to="/" exact>Back</router-link></span>
                <a href="https://parkpeople.ca" class="navbar-item">ParkPeople.ca</a>
            </div>
        </div>
    </nav>
</template>

<script>
import { eventBus } from '../main.js';
export default {
    data() {
        return {
            id: this.$route.params.id,
            lang: '',
            showMobileMenu: false,
            scrolled: false,
            showSocialShare: false
        }
    },
    methods: {
        handleScroll: function (event) {
            if (window.addEventListener){
                // console.log('A');
                // console.log(pageYOffset);
                if (window.pageYOffset > 20) {
                    this.scrolled = true;
                } else {
                    this.scrolled = false;	
                }
            } else if (window.attachEvent){
                // console.log('B');
                if (window.scrollY > 20) {
                    this.scrolled = true;
                } else {
                    this.scrolled = false;	
                }
            } else {
                if (window.pageYOffset > 20) {
                    // console.log('C');
                    this.scrolled = true;
                } else {
                    this.scrolled = false;	
                }
            }
        }
    },
    created: function () {
        // window.addEventListener('scroll', this.handleScroll);
        if (window.addEventListener){
            // console.log('Option 1');
            window.addEventListener('scroll', this.handleScroll);
        } else if (window.attachEvent){
            // console.log('Option 2');
            window.attachEvent('scroll', this.handleScroll);
        } else {
            // console.log('Option 3');
            jQuery(window).on('scroll', this.handleScroll);
            // console.log('IE');
        }
    },
    destroyed: function () {
        // window.removeEventListener('scroll', this.handleScroll);
        if (window.addEventListener){
            window.removeEventListener('scroll', this.handleScroll);
        } else if (window.attachEvent){
            window.detachEvent('scroll', this.handleScroll);
        } else {
            window.removeEventListener('scroll', this.handleScroll);
        }
    }
};
</script>

<style lang="scss" scoped>

@import '../styles/variables.scss';

nav {
    z-index: 500;
    font-family: "Dosis", sans-serif;
    font-weight: bold;
    a {
        &:hover {
            font-weight: bold;
        }
    }
}

.green {
    background-color: $darkGreen;
}

nav#scrolling {
    @media #{$medium-and-down} {
		// display: block;
		position: fixed; 
        width: 100%;
		z-index: 6000;
    }
}

#mobile-menu-trigger {
	display: none;
	&:hover {
		cursor: pointer;
	}
	i {
		color: $white;
		font-size: 30px;
	}
	@media #{$medium-and-down} {
		display: block;
		position: fixed; 
		right: 30px;
		top: 15px;
		z-index: 5000000;
    }
	
}

.navbar {
    @media #{$medium-and-down} {
        display: flex;
        align-items: center;
        position: relative;
        z-index: 5000;
    }
}

.navbar-brand {
    @media #{$medium-and-down} {
        display: inline-block;
    }
}

.navbar-menu {
    a {
        color: $white;
        &:hover {
            color: $blue;
            background: $white;
            border-bottom: none;
        }
    }
    span {
        &:hover {
            background: $white;
            color: $blue;
            a {
                color: $blue;
            }
        }
    }
}

.navbar-menu.menu-open {
    @media #{$medium-and-down} {
        position: absolute;
        display: inline-block;
        top: 55px;
        width: 100%;
        background: $darkGreen;
    }
}

.lang {
    display: flex;
    align-items: center;
    color: white;
    margin: 1em;
    @media #{$medium-and-down} {
        display: inline-block;
        margin: 0 0 0 16px;
    }
    a {
        color: white;
        &:hover {
            font-weight: bold;
        }
    }
}

.navbar-item {
    color: white;
}

.grants-logo {
    max-height: 50px;
    width: auto;
    margin-top: 3px;
    margin-left: 8px; 
    @media #{$large-and-up} {
		max-height: 50px;
        width: auto;
        margin-top: 8px;
        margin-bottom: 2px;
        margin-left: 20px; 
	}
    @media #{$xlarge-and-up} {
		max-height: 80px;
        width: auto;
        margin-top: 3px;
        margin-left: 20px; 
	}
}

.social-share-container {
    color: $white;
    font-family: "Dosis", sans-serif;
    font-weight: bold;
}

.social-share-buttons {
    display: none;
    i,
    span {
        margin: 0 8px;
    }
}

#social-share-trigger {
    padding: 16px 24px;
    display: inline-block;

    &:hover {
        cursor: pointer;
        color: lighten($blue, 10);
    }
}

#social-share-trigger.social-menu-open + .social-share-buttons {
    display: inline-block;
}
</style>