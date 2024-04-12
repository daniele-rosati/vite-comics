<script>
    export default{
        name: "AppNav",
        data() {
            // TODO: change navContent words
            return {
                navContent: [
                    ["DC Comics", "Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"],
                    ["Shop", "Shop DC", "Shop DC collectibles"],
                    ["DC", "Term of use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificate", "Ratings", "Shop Help", "Contact Us"],
                    ["SITES", "DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
                ]
            }    
        },
    };
</script>

<template>
    <section>
        <div class="container">
            <nav v-for="list, index in navContent">
                <ul>
                    <li v-for="listElement in navContent[index]"><a href="#">{{ listElement }}</a></li>
                </ul>
            </nav>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    section{
        background: url(../assets/img/footer-bg.jpg) no-repeat center;
        background-size: cover;
        color: white;
        font-size: 2rem;
        .container{
            height: 300px;
            padding: 30px 0;
            background: url(../assets/img/dc-logo-bg.png) no-repeat 90%;
            background-size: 40%;
            display: flex;
            flex-direction: column;
            align-content: flex-start;
            flex-wrap: wrap;
            > nav {
                margin: 8px;
            }
        }
    }

    ul{
        li{
            font-size: 0.8rem;
            color: rgb(139, 139, 139);
            &:first-child{
                color: white;
                margin-bottom: 10px;
                font-size: 1.4rem;
                font-weight: 500;
                text-transform: uppercase;
            }
        }
    }
</style>