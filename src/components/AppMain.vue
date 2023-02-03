<script>
    export default {
        name: 'AppMain',
    }
</script>

<template>
    <main>
        <div class="container">
            <div class="content">
                <h2>
                    <!-- usa &lt per mettere simbolo minore -->
                    --> Content goes here &lt--
                </h2>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @import "../styles/partials/colors.scss";

        main {
            background-color: $dc-black;

            .content{
                color: white;
                padding: 3rem 0;

                h2 {
                    font-size: 1.5rem;
                }
            }

        }
</style>