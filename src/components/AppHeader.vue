<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                active: 0,
                navbar: [
                    {
                        title: 'characters',
                        link: '#',
                    },
                    {
                        title: 'comics',
                        link: '#',
                    },
                    {
                        title: 'movies',
                        link: '#',
                    },
                    {
                        title: 'tv',
                        link: '#',
                    },
                    {
                        title: 'games',
                        link: '#',
                    },
                    {
                        title: 'collectibles',
                        link: '#',
                    },
                    {
                        title: 'videos',
                        link: '#',
                    },
                    {
                        title: 'fans',
                        link: '#',
                    },
                    {
                        title: 'news',
                        link: '#',
                    },
                    {
                        title: 'shop',
                        link: '#',
                    },
                ]
            }
        },
    }    
</script>

<template>
    <header>
        <div class="container">
            <div class="logo-container">
                <img src="../assets/img/dc-logo.png" alt="dc-logo">
            </div>
            <div class="navbar">
                <ul>
                    <li v-for="navitem,i in navbar">
                        <a 
                            :href="navitem.link"
                            @click="active = i"
                            :class="{
                                active: active == i,
                            }"> 
                            {{ navitem.title }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @import "../styles/partials/colors.scss";
        header {
            height: 120px;
            background-color: white;
            .container {
                height: 100%;
                display: flex;
                justify-content: space-between;
                align-items: center;

                .logo-container {
                    height: 100%;
                    padding: 1rem 0;

                    img {
                        height: 100%;
                    }
                }

                ul {
                    display: flex;
                    list-style: none;
                    
                    a {
                        display: inline-block;
                        height: 120px;
                        padding: 0 1rem;
                        line-height: 120px;
                        text-transform: uppercase;
                        font-size: 0.8rem;
                        font-weight: bold;
                        color: $dc-black;
                        text-decoration: none;        
                        
                    &.active {
                        color: $dc-blue;
                    }
                    &:hover {
                        color: $dc-blue;
                        }
                    }
                }                    
            }
        }        
</style>