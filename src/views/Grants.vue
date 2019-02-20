<template>
	<div v-if="data != null" class="relative-div">
		<section class="section" v-if="data && data.hasOwnProperty('meta_box')">

			<div class="logo-container"><img src="https://parkpeople.ca/listings/custom/uploads/2018/04/GreenbeltGrant_logo_large_colour-04-04.png" alt="Greenbelt River Valley Connector Program" class="top-logo"></div>

			<div class="container">
	
				<div class="column-layout">
					<div class="topContent" v-html="data.content.rendered"></div>
	
					<div class="sidebar" v-html="data.meta_box._page_grant_more_info"></div>
				</div>

			</div>
		</section>

		<div class="alternating">
			<div class="single" v-for="single in data.meta_box._page_alternating" :key="single._page_alt_heading">
				<div class="image">
					<img :src="single._page_alt_image" alt="">
				</div>
				<div class="copy">
					<div class="copy-container">
						<h4 v-html="single._page_alt_heading"></h4>
						<div v-html="single._page_alt_copy"></div>
					</div>
				</div>
			</div>
		</div>

		<!-- <div class="cta-bottom">
			<a :href="data.meta_box._page_grant_cta_link" class="download-button"><i class="fas fa-download"></i> Application Form</a>
			<p>Please direct all questions about the program to: <a href="mailto:grants@parkpeople.ca">grants@parkpeople.ca</a></p>
		</div> -->

		<div class="squiggle">
			<svg viewBox="0 0 1024 44" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
				<!-- Generator: Sketch 49.3 (51167) - http://www.bohemiancoding.com/sketch -->
				<desc>Created with Sketch.</desc>
				<defs>
					<polygon id="path-1" points="0.175940741 0.27442623 527.476089 0.27442623 527.476089 35.9900973 0.175940741 35.9900973"></polygon>
				</defs>
				<g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" opacity="0.268568841">
					<g id="Greenbelt_" transform="translate(0.000000, -4154.000000)">
						<g id="Ribbon" transform="translate(-22.000000, 4154.000000)">
							<path d="M0,19.5365109 C0.00355365387,19.5376932 32.5508772,32.9075385 59.6534107,31.2174652 C97.7853012,28.8398944 101.783162,10.5771717 123.27803,11.0642722 C175.199282,12.2441905 250.643946,33.5217344 292.455052,34.4811569 C344.203952,35.6669866 366.90114,30.016857 382.05925,27.2916951 C404.411141,23.2737069 431.143502,7.7278701 466.245902,2.60562978 C502.283506,-2.65198192 525.504858,6.68568779 525.504858,6.68568779 L526,9.55331477 C526,9.55331477 495.599083,-0.574119868 459.640844,6.38006768 C428.825927,12.3399554 412.209042,21.6545706 385.289521,28.2522999 C366.466409,32.8667497 327.300998,43.143152 248.305641,31.9758996 C204.688094,25.8102947 161.27725,15.9305483 134.483292,13.433567 C96.9644072,9.93578326 102.031918,30.1930171 61.0399279,32.9075385 C30.8563765,34.9061876 0.211442405,22.9172486 0.211442405,22.9172486 L0,19.5365109 Z" id="Fill-1" fill="#00B0F5"></path>
							<path d="M76.6697204,37.8054067 C96.7644109,32.5878956 102.418005,27.0671906 188.475238,11.7517995 C228.175963,4.68585898 265.747929,0.596838044 336.986172,21.1993929 C346.904986,24.0686142 355.019033,27.1450377 361.816376,29.5026925 C375.50524,34.2525357 385.471439,36.0125824 389.576736,36.5709743 C439.048198,43.306211 440.335879,8.38857104 465.003198,21.5219022 C497.388902,38.7653258 508.019673,40.4323071 524.707991,38.3667252 L525,40.6629218 C525,40.6629218 502.917519,47.7341302 466.352479,24.1862629 C442.509655,8.8310703 433.503589,46.6231995 387.670092,38.8677561 C383.166763,38.1050888 374.194459,36.0383363 360.854466,31.3634135 C353.439936,28.767535 344.802879,25.2187611 334.528087,22.3255418 C296.654044,11.667514 237.75953,-7.68187826 86.5062035,37.0585429 C52.0166163,47.2606092 18.3367161,45.2512177 0.0100692607,37.2739394 L0,34.3485276 C26.779495,48.2228695 62.8280407,41.3992499 76.6697204,37.8054067" id="Fill-3" fill="#00B0F5"></path>
							<path d="M526,18.1713752 C526,18.1713752 460.190786,50.9366988 392.182937,13.8308678 C366.232184,-0.327928465 342.281104,2.41242701 295.176565,11.9383409 C250.467252,20.9802835 212.606095,41.6111701 141.577715,31.7618275 C116.593343,28.2978588 93.7791817,7.33475463 63.168248,4.99575548 C51.6143155,4.11394342 24.9636473,3.09795532 0.0124350442,9.68547222 L0,13.2994368 C0,13.2994368 22.6157925,5.75569584 56.2093604,6.59180601 C96.2851392,7.59021647 110.579519,32.0501009 156.628264,35.9066371 C226.731121,41.7793296 249.079264,22.4093464 289.062076,15.4427382 C345.064778,5.68597116 368.206987,3.0135826 392.068653,16.2718173 C453.948393,50.6536986 525.881571,22.404659 525.881571,22.404659 L526,18.1713752 Z" id="Fill-5" fill="#00B0F5"></path>
							<g id="Group-9" transform="translate(540.000000, 0.000000)">
								<mask id="mask-2" fill="white">
									<use xlink:href="#path-1"></use>
								</mask>
								<g id="Clip-8"></g>
								<path d="M0.175940741,17.6181049 C0.179496296,17.6192852 33.7634963,31.9047934 60.8799407,30.2175148 C99.032237,27.8438754 103.032237,9.61135082 124.538607,10.0976459 C176.487644,11.2756131 251.973274,32.5179738 293.806756,33.4758098 C345.583348,34.6596787 368.292089,29.0183016 383.458904,26.2982361 C405.822163,22.2868918 432.516681,6.39495738 467.690607,1.65299016 C501.56557,-2.91251803 527.32083,5.3244 527.32083,5.3244 L527.476089,8.58859672 C527.476089,8.58859672 497.059496,-1.52150164 461.081422,5.42118689 C430.250607,11.3712197 413.624237,20.6698426 386.690904,27.2572525 C367.857719,31.863482 328.671348,42.1228918 249.633719,30.9746951 C205.992237,24.8192852 162.558163,14.9558754 135.750459,12.463023 C98.2114963,8.97043279 103.281126,29.1947607 62.2672,31.9047934 C32.0674963,33.9001377 1.2989037,21.5521377 1.2989037,21.5521377 L0.175940741,17.6181049 Z" id="Fill-7" fill="#00B0F5" mask="url(#mask-2)"></path>
							</g>
							<path d="M618.300746,37.8053954 C638.4023,32.5878862 644.057825,27.0671831 730.144453,11.7517975 C769.85874,4.68585945 807.443539,0.596839962 878.706116,21.1993875 C888.628318,24.0686078 896.745137,27.1450302 903.544802,29.5020988 C917.238341,34.2525257 927.207945,36.0125717 931.314644,36.5709634 C980.803005,43.3061978 982.091125,8.38857019 1006.76687,21.5218967 C1039.16364,38.7647288 1051.30598,40.0108672 1068,37.9447007 L1067.87261,40.7752902 C1067.87261,40.7752902 1044.69414,47.7341154 1008.11661,24.1862564 C984.265643,8.83106929 975.256502,46.6225998 929.407348,38.8671592 C924.902481,38.1050774 915.92652,36.0377403 902.582563,31.3634045 C895.1655,28.7675269 886.525494,25.2187543 876.247192,22.325536 C838.360211,11.667512 779.445581,-7.68245872 628.140589,37.0579466 C599.215349,45.6117586 570.859513,45.5819074 551.646134,40.6476913 C547.942342,39.6965523 548.266446,37.4202573 551.746268,38.5393821 C576.845659,46.6085522 606.140627,40.9614208 618.300746,37.8053954" id="Fill-10" fill="#00B0F5"></path>
							<path d="M1068,18.1709564 C1068,18.1709564 1002.19079,50.9365751 934.182937,13.8304875 C908.232184,-0.327597083 884.281104,2.41214814 837.176565,11.9385634 C792.467844,20.9804257 754.606095,41.6111292 683.577715,31.761288 C658.593343,28.2973501 635.779182,7.33501799 605.168248,4.9960396 C593.614315,4.11364946 566.963647,3.09825628 542.012435,9.68571471 L542,13.2996472 C542,13.2996472 564.616385,5.75597321 598.20936,6.59207596 C638.285139,7.58989164 652.579519,32.0495589 698.628264,35.9066468 C768.731121,41.7792872 791.079264,22.4094759 831.062076,15.4429295 C887.064778,5.68566324 910.206987,3.01388432 934.068653,16.2714154 C995.948393,50.6529915 1067.88157,22.4042027 1067.88157,22.4042027 L1068,18.1709564 Z" id="Fill-12" fill="#00B0F5"></path>
							<path d="M545.839429,8 L541.580702,9.07815235 C541.580702,9.07815235 536.199177,10.9160642 533.157914,13.9721482 C533.157914,13.9721482 526.623632,18.7261243 523,19.9424701 L523,24 C523,24 531.338309,21.1594247 535.831901,16.4900692 C535.831901,16.4900692 540.218844,12.3814017 546,11.5351952 L545.839429,8 Z" id="Fill-14" fill="#00B0F5"></path>
							<path d="M517,4 L522.554605,5.56244193 C522.554605,5.56244193 530.71673,7.81989097 535.735937,13.5847426 C535.735937,13.5847426 538.339864,17.3834479 545,19.6055876 L545,23 C545,23 536.460581,20.5724772 532.436112,15.8315988 C532.436112,15.8315988 528.862001,10.784117 517.316807,7.16313572 L517,4 Z" id="Fill-16" fill="#00B0F5"></path>
							<path d="M523,41 C523,41 539.628907,37.51663 551.559703,40.0832071 L552,38.1903842 C552,38.1903842 542.029763,35.2656157 523.284296,38.5851145" id="Fill-18" fill="#00B0F5"></path>
						</g>
					</g>
				</g>
			</svg>
		</div>


		<section class="grants-newsletter">
			<div class="container">
				<p>Would someone you know also benefit from reading this? Share it!</p>
				<div class="social-share-container social-home">
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
				<p style="margin-bottom: 1rem;">Want to stay up-to-date on Park People news?</p>
				<a class="button" href="http://eepurl.com/dx3BWX" target="_blank">Get the Park People newsletter!</a>
			</div>
		</section>

	</div>
	<div v-else class="loading-panel">
		<div>
			<img src="https://parkpeople.ca/listings/custom/uploads/2018/01/birdflying_pp_small.gif" alt="">
		</div>
	</div>
</template>

<script>
import axios from 'axios';
// import { mapState } from 'vuex'
export default {
	data() {
		return {
			// data: {},
			relatedPosts: [],
			errors: [],
			loading: true,
			test: [
				{'title': 'Title1', 'copy': 'Lorem ipsum'},
				{'title': 'Title2', 'copy': 'Lorem ipsum'},
				{'title': 'Title3', 'copy': 'Lorem ipsum'},
				{'title': 'Title4', 'copy': 'Lorem ipsum'}
			]
		};
	},
	filters: {
		removeHyphen(value){
			return value.replace("-", ' ');
		},
		capitalizeFirstLetter(value) {
			return value.charAt(0).toUpperCase() + value.slice(1);
		},
		toUppercase(value) {
			return value.toUpperCase();
		},
		readMore(value, length, suffix) {
			if (value.length < length)
			return value;	
			return value.substring(0, length) + suffix;
		},
		stripHTML(value) {
			return value.replace(/(<([^>]+)>)/ig,"");
		},
		toTitleCase(value) {
    		return value.replace(/\w\S*/g, (txt) => {
				return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
			});
		},
	},
	computed: {
		data() {
			return this.$store.state.pageData;
		}
    },
	methods: {

	},
	mounted() {

	},
	created() {
		axios.get('https://parkpeople.ca/listings/wp-json/wp/v2/pages/2117?_embed')
		.then(response => {
            console.log(response.data)
			// this.data = response.data
			
			this.loading = false
			this.$store.commit('SET_PAGE_DATA', response.data);

		})
		.catch(e => {
			console.log(e)
			this.errors.push(e)
		})
	},
};
</script>

<style lang="scss" scoped>

@import '../styles/variables.scss';
@import '../styles/grants.scss';

.section {
	background-color: #fff;
	@media #{$small-and-down} {
		padding: 24px 1.5rem !important;
	}
}

.card-content {
	padding: 0.8rem 1.5rem;
}



.sidebar {
	h3 {
		font-size: 18px;
	}
} 

h1 {
    color: $orange;
	font-size: 35px;
	line-height: 1.2;
	font-weight: 700;
	text-align: center;
	font-family: 'Roboto Condensed', sans-serif;
	text-transform: uppercase;
	color: grey; 
	margin: 0;
	font-weight: 300;
	@media #{$large-and-up} {
		font-size: 30px;
		line-height: 1.3;
		font-weight: 700;
		margin-top: 20px;
		font-weight: 400;
	}
}

h1.main-heading {
	// font-size: 25px;
}

.intro-logo {
	margin: 0 auto;
	// max-width: 400px;
	text-align: center;
	img {
		max-width: 150px;
		height: auto;
	}
	span.top-logo-text {
		font-family: 'Open Sans';
		text-transform: uppercase;
		color: grey; 
		margin: 0;
		font-weight: 800;
		font-size: 35px;
		// line-height: 1.3;
	}
	span.bottom-logo-text {
		font-family: 'Roboto Condensed', sans-serif;
		text-transform: uppercase;
		color: $body-color;
		font-weight: 400;
		font-size: 25px; 
		// line-height: 1.3;
	}
	h1 {
		margin: 0;
		line-height: 1;
		margin-top: 20px;
	}
}

.container {
    max-width: 960px;
    margin: 0 auto;
}

.loading-panel {
	min-height: 100vh;
	background: $white;
	display: flex;
	align-items: center;
	justify-content: center;
}

.wide-container {
    max-width: 1160px;
    margin: 0 auto;
}

.content a h4 {
	color: rgba(30,177,242, 1);
	font-size: 1.2rem;
	line-height: 1.7rem;
	font-weight: 700;
	margin-bottom: 0.3rem;
	margin-top: 0.3rem;
	// line-height: 1.4;
	&:hover {
		color: rgba(30,177,242,0.7);
	}
}

.card .content {
	p {
		margin-bottom: 0.3rem;
	}
}

.activity-list-container,
.activity-list-container span,
.activity-list-container strong {
	font-size: 12px;
	line-height: 1.5;
	color: rgba(0,0,0,0.4) !important;
}

.activity-list-container span {
	display:inline-block;
	margin-right: 5px;
	position: relative;
	&:after {
		content: ',';
		position: absolute;
		bottom: 0;
		right: -2px;
		color: rgba(0,0,0,0.4) !important;
	}
}

.activity-list-container span:last-child {
	margin-right: 0px;
	&:after {
		display: none;
	}
}

.skewed-bg{
  	background: #fff;
 	padding: 100px 0;
	transform: skew(0deg, -5deg);
  	margin-top: -130px;
	position: relative;
	z-index: -1;
}

img {
	object-fit: cover;
}

.content {
	p {
		font-size: 0.8rem;
		line-height: 1.3rem;
	}
	ul {
		list-style-type: none;
		margin: 0 0 10px 0;
		li { 
			color: rgba(0,0,0,0.5);
			display: inline;
			font-weight: 700;
			&:not(:last-child):after {
				content: " | ";
			}
		}
	}
}

.topContent {
    margin: 0;
	margin-bottom: 50px;
    font-size: 1rem;
	@media #{$medium-and-up} {
		font-size: 1.2rem;
    }
    p {
        font-size: 1.2rem;
	}
}

.application-eligibility {
	position: relative;
	z-index: 500;
	@media #{$small-and-down} {
        div + div {
			margin-top: 40px;
		}
	}
	@media #{$large-and-up} {
        display: flex;
		justify-content: space-between;
		>div {
			width: 45%;
			// margin: 0 1%;
			h2 {
				font-size: 1rem;
				font-weight: 700;
				font-family: $family-sanserif;
				@media #{$medium-and-up} {
					font-size: 1.2rem;
				}
			}
		}
	}
}

.application-eligibility ul {
	li {
		display: flex;
		align-items: center;
		margin-bottom: 16px;
		font-size: 0.9rem;
		line-height: 1.5;
		img {
			margin-right: 16px;
			max-height: 40px;
			width: auto;
		}
	}
}

.application-eligibility ol {
	list-style: none;
	>li {
		counter-increment: item;
		margin-bottom: 5px;
		position: relative;
		padding-left: 70px;
		padding-bottom: 24px;
		margin-bottom: 8px;
		font-size: 0.9rem;
		line-height: 1.5;
	}
	> li:first-child {
		margin-top: 24px;
	}
	>li:not(:last-child) {
		// border-bottom: 2px dashed $orange;
	}
	>li:before {
		margin-right: 10px;
		content: counter(item);
		background: white;
		border-radius: 100%;
		border: 2px solid $orange;
		color: $orange;
		width: 40px;
		height: 40px;
		font-family: serif;
		font-size: 24px;
		font-style: italic;
		font-weight: bold;
		text-align: center;
		padding-top: 0px;
		// display: inline-block;
		position: absolute;
		top: 0;
		left: 0px;
	}
}

.align-center {
	text-align: center;
	position: relative;
	z-index: 200;
}

.cta_button {
	display: inline-block;
	margin: 0 auto;
	color: $white;
	background-color: $orange;
	border:4px solid $orange;
	padding: 16px 40px;
	border-radius: 50px;
	font-size: 32px;
	margin: 32px 0;
	font-weight: bold;
	&:hover {
		background-color: $white;
		color: $orange;
		border:4px solid $orange;
	}
}

.more-info {
	position: relative;
	z-index: 500;
	p {
		font-size: 1.5rem;
	}
}

.grants-newsletter {
	text-align: center;
	font-size: 0.8rem;
	line-height: 1.5;
	margin-top: 40px;
	p {
		font-size: 0.8rem;
		line-height: 1.5;
	}
}

.grant-sponsors {
	padding-top: 100px;
	text-align: center;
	font-size: 0.8rem;
	line-height: 1.5;
	p {
		font-size: 0.8rem;
		line-height: 1.5;
	}
	ul {
		margin: 0 auto;
		li {
			display: inline-block;
			margin: 0 24px;
			img {
				max-width: 100px;
				height: auto;
			}
		}
	}
}

.grants-newsletter {
	.button {
		background: $white;
		border: 2px solid $blue;
		color: $blue;
		border-radius: 50px;
		font-weight: bold;
		padding: 16px 32px;
		height: 50px;
		@media #{$small-and-down} {
			height: auto;
			margin-top: 8px;
			width: 80%;
			white-space: normal;
			display: block;
			margin: 0 auto;
		}
		&:hover {
			background: $blue;
			border: 2px solid $blue;
			color: $white;
		}
	}
}


.related-resources {
	padding: 24px;
	padding-bottom: 180px;
	margin-top: 50px;
	margin-bottom: -50px;
	@media #{$medium-and-up} {
		padding: 50px;
		padding-bottom: 200px;
	}
	h3 {
		color: $green;
		font-size: 40px;
		@media #{$small-and-down} {
			font-size: 32px;
			font-weight: bold;
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

.related-resources-copy {
	text-align: center;
	margin-bottom: 24px;
}

@-webkit-keyframes slide {
    from { background-position: 0 0; }
    to { background-position: -400px 0; }
}

@keyframes slide {
    from { background-position: 0 0; }
    to { background-position: -200% 0; }
}

.grant-illustration {
	position: relative;
	margin-top: -200px;
	z-index: 100;
	padding-bottom: 15%;
	min-height: 300px;
	@media #{$medium-and-up} {
		min-height: 300px;
	}
	@media #{$large-and-up} {
		min-height: 500px;
	}
	.main-animation {
		position: absolute;
		left: 0;
		top: 130px;
		z-index: 20;
		@media #{$medium-and-up} {
			top: 15%;
			width: 700px;
			left: 50%;
			margin-left: -350px;
			// right: 50%;
		}
		@media #{$large-and-up} {
			top: -15%;
			width: 1300px;
			left: 50%;
			margin-left: -650px;
			// right: 50%;
		}
		@media #{$xlarge-and-up} {
			width: 1300px;
			left: 50%;
			margin-left: -650px;
			// right: 50%;
		}
	}
	.clouds {
		position: absolute;
		background: url('https://parkpeople.ca/listings/custom/uploads/2018/01/park_people_event_greenline_background_long.jpg') repeat 0 0;
		width: 100%;
		height: 500px;
		background-size: cover;
		left: 0;
		top: 0%;
		z-index: 10;
		-webkit-animation: slide 40s linear infinite alternate;
		animation: slide 40s linear infinite alternate;
		@media #{$small-and-down} {
			height: 350px;
		}
		@media #{$medium-and-up} {
			height: 400px;
		}
		@media #{$large-and-up} {
			height: 500px;
		}
		@media #{$xlarge-and-up} {
			// width: 1000px;
			background-size: contain;
		}
	}
}

#bird-anchor {
	position: relative;
	&:before {
		content: url('https://parkpeople.ca/listings/custom/uploads/2018/01/birdflying_pp_small.gif');
		position: absolute;
		width: 50px;
		height: 50px;
		top: 100px;
		left: -120px;
		-moz-transform: scaleX(-1);
        -o-transform: scaleX(-1);
        -webkit-transform: scaleX(-1);
	}
	@media #{$xlarge-and-up} {
        &:before {
			content: url('https://parkpeople.ca/listings/custom/uploads/2018/01/birdflying_pp_small.gif');
			position: absolute;
			width: 50px;
			height: 50px;
			left: -120px;
			top: 200px;
		}
	}
}

.card__activity-list {
	ul {
		li {
			font-size: 0.8rem;
		}
	}
}

.social-share-container {
	padding: 16px 0 8px;
	font-size: 24px;
	color: $blue;
}

.winners {
	padding: 3rem;
	.winners-container {
		max-width: 1100px;
		margin: 50px auto;
	}
	h3 {
		max-width: 950%;
		text-align: center;
		margin: 0 auto;
		font-weight: bold;
		color: $darkGreen;
		font-size: 30px;
		@media #{$large-and-up} {
		font-size: 35px;
		max-width: 80%;
		}
	}
	h4 {
		font-size: 25px;
		font-weighT: bold;
	}
	.single-winner {
		margin-bottom: 40px;
		img {
			margin-bottom: 20px;
		}
		@media #{$large-and-up} {
			margin-bottom: 80px;
			display: flex;
			.image {
				width: 30%;
				img {
					width: 100%;
					height: auto;
				}
			}
			.copy {
				width: 65%; 
			}
		}	
	}
	.winner-copy-container {
		@media #{$large-and-up} {
		padding: 0 3rem;
		}
	}
}
</style>