<script>
    export default {
        name: 'CardElement',
        props: {
            label: String,
            src: String
        },
    }
</script>
<template>
    <div class="img-section">
        <div class="img-container">
            <img :src="src" alt="label">
        </div>
        <h4>{{ label }}</h4>
    </div>
</template>

<style lang="scss" scoped>   
        .img-container {
            margin-bottom: 1rem;
            overflow: hidden;
            aspect-ratio: 1/1;

            img {
                width: 100%;

                &:hover {
                    cursor: pointer;
                    opacity: 50%;
                }
            }
        }

        h4 {
            font-weight: 300;
            color: $dc-white;
            text-transform: uppercase;

            &:hover {
                text-decoration: underline;
                cursor: pointer;
            }
        }    
</style>