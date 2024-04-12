<script>
    export default{
        name: "AppHeader",
        data(){
            return {
                navElements: ["characters", "comics", "movies", "tv", "games", "collectibles", "videos", "fans", "news", "shop"],
                activeElement: 2,
            }
        },
        methods: {
            changeActive(index){
                this.activeElement = index;
            }
        }
    };
</script>

<template>
    <header>
        <div class="container">
            <img src="/src/assets/img/dc-logo.png" alt="">
            <nav>
                <ul>
                    <li v-for="element, index in navElements" :class="{ 'active': index == activeElement }" @click="changeActive(index)"><a href="#">{{ element }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

    header{
        height: $small_sect_h;
        
        .container{
            height: inherit;
            display: flex;
            justify-content: space-between;
            
            img{
                align-self: center;
                height: 80%;
            }
    
            ul{
                display: flex;
                height: 100%;
    
                li{
                    padding: 0.6rem;
                    display: flex;
                    align-items: center;
                    text-transform: uppercase;
                    font-weight: 700;
                    color: $secondary_dark;
    
                      &.active{
                           border-bottom: 3px solid $primary_color;
                           color: $primary_color;
                      }
                 }
            }
        }
    }

</style>