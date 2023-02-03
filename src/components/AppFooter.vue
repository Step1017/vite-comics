<script>
    export default {
        name: 'AppFooter',
        data() {
            return {
                bluBarContent: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        title: 'digital comics',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-merchandise.png',
                        title: 'dc merchandise',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-subscriptions.png',
                        title: 'subscription',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-shop-locator.png',
                        title: 'comic shop locator',
                        link: '#',
                    },
                    {
                        img: 'buy-dc-power-visa.svg',
                        title: 'dc power visa',
                        link: '#',
                    },
                ],

                dcComicsContent: [
                    {
                        title:'characters',
                        link: '#',
                    },
                    {
                        title:'comics',
                        link: '#',
                    },
                    {
                        title:'Movies',
                        link: '#',
                    },
                    {
                        title:'TV',
                        link: '#',
                    },
                    {
                        title:'games',
                        link: '#',
                    },
                    {
                        title:'videos',
                        link: '#',
                    },
                    {
                        title:'news',
                        link: '#',
                    },
                ],

                shopContent: [
                    {
                        title:'shop DC',
                        link: '#',
                    },
                    {
                        title:'shop collectibles',
                        link: '#',
                    },
                ],

                dcContent: [
                    {
                        title:'terms of use',
                        link: '#',
                    },
                    {
                        title:'privacy policy (new)',
                        link: '#',
                    },
                    {
                        title:'ad choices',
                        link: '#',
                    },
                    {
                        title:'advertising',
                        link: '#',
                    },
                    {
                        title:'jobs',
                        link: '#',
                    },
                    {
                        title:'subscriptions',
                        link: '#',
                    },
                    {
                        title:'talent workshop',
                        link: '#',
                    },
                    {
                        title:'CPSC certificates',
                        link: '#',
                    },
                    {
                        title:'ratings',
                        link: '#',
                    },
                    {
                        title:'shop help',
                        link: '#',
                    },
                    {
                        title:'contact us',
                        link: '#',
                    },
                ],

                sitesContent: [
                    {
                        title:'DC',
                        link: '#',
                    },
                    {
                        title:'MAD magazine',
                        link: '#',
                    },
                    {
                        title:'DC kids',
                        link: '#',
                    },
                    {
                        title:'DC universe',
                        link: '#',
                    },
                    {
                        title:'DC power visa',
                        link: '#',
                    },
                ],

                socialList: [
                    {
                        img: 'footer-facebook.png',
                        link: '#',
                        social: 'facebook'
                    },
                    {
                        img: 'footer-twitter.png',
                        link: '#',
                        social: 'twitter'
                    },
                    {
                        img: 'footer-youtube.png',
                        link: '#',
                        social: 'youtube'
                    },
                    {
                        img: 'footer-pinterest.png',
                        link: '#',
                        social: 'pinterest'
                    },
                    {
                        img: 'footer-periscope.png',
                        link: '#',
                        social: 'periscope'
                    },
                ], 
            };
        },

        methods: {
            getImgPath(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },
        },
    }
</script>

<template>
    <footer>
        <div class="blu-bar">
            <div class="container">
                <ul>
                    <li v-for="item in bluBarContent">
                        <a :href="item.link">
                            <img :src="getImgPath(item.img)" :alt="item.title">
                            <span>{{ item.title }}</span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="nav-list">
            <div class="container">
                <nav>
                    <div class="col">
                        <div class="list">
                            <h3>dc comics</h3>
                            <ul>
                                <li v-for="item in dcComicsContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                        <div class="list">
                            <h3>shop</h3>
                            <ul>
                                <li v-for="item in shopContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <div class="list">
                            <h3>dc</h3>
                            <ul>
                                <li v-for="item in dcContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="col">
                        <div class="list">
                            <h3>sites</h3>
                            <ul>
                                <li v-for="item in sitesContent">
                                    <a :href="item.link"> {{ item.title }} </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </nav>
                <div class="logo-bg">

                </div>
            </div>
        </div>        
        <div class="social-bar">
            <div class="container">
                <a class="btn" href="#">SIGN-UP NOW!</a>
                <div class="social-box">
                    <span>FOLLOW US</span>
                    <a v-for="item in socialList" :href="item.link">
                        <img :src="getImgPath(item.img)" :alt="item.social">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @import "../styles/partials/colors.scss";
        .blu-bar {
            background-color: $dc-blue;
            padding: 3rem;

            ul {
            display: flex;
            list-style: none;
            justify-content: space-around;
                li {
                    color: $dc-white;

                    a {
                        display: flex;
                        align-items: center;
                        text-transform: uppercase;
                        text-decoration: none;
                        color: $dc-white;
                        &:hover {
                            text-decoration: underline;
                        }

                        img {
                            height: 50px;
                            margin-right: 1rem;
                        }
                    }
                }
            }
        }

        .nav-list {
            background-color: $dc-black;
            background-image: url('../assets/img/footer-bg.jpg');
            background-repeat: no-repeat;
            background-size: cover;
            .container {
                display: flex;
                justify-content: space-between;

                nav {
                    display: flex;
                    padding: 2rem 0;
                    color: $dc-white;
                    
                    .col {
                        margin-right: 3rem;                    

                        h3 {
                            text-transform: uppercase;
                            margin-bottom: 1rem;
                        }

                        ul {
                            list-style: none;
                            margin-bottom: 1rem;

                            a {
                                color: $dc-lightgray;
                                font-size: 0.7rem;
                                text-decoration: none;
                                text-transform: capitalize;

                                &:hover {
                                    text-decoration: underline;
                                }
                            }
                        }
                    }
                }
                .logo-bg {
                    width: 70%;
                    background-image: url('../assets/img/dc-logo-bg.png');
                    background-repeat: no-repeat;                    
                    background-position: right;
                }
            }
        }

        .social-bar {
            padding: 3rem;
            background-color: $dc-darkgray;
            .container {
                display: flex;
                justify-content: space-between;

                .btn {
                    color: $dc-white;
                    border: 2px solid $dc-blue;
                    padding: 1rem;
                    text-transform: uppercase;
                    text-decoration: none;
                    font-weight: bold;

                    &:hover {
                        text-decoration: underline;
                    }
                }

                .social-box {
                    display: flex;
                    align-items: center;
                    
                    span {
                        color: $dc-blue;
                        font-size: 1.2rem;
                        font-weight: bold;
                        margin-right: 2rem;
                    }

                    a {
                        margin-left: 1rem;                        
                    }
                }
            }
        }
</style>