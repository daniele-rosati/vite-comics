<script>
    import SingleCard from "./SingleCard.vue"

    export default{
        name: "AppCards",
        components: {
            SingleCard,
        },
        data() {
			return {
				comics: [
							{
								"thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
								"price": "$19.99",
								"series": "Action Comics",
								"type": "comic book"
							},
							{
								"thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
								"price": "$3.99",
								"series": "American Vampire 1976",
								"type": "comic book"
							},
							{
								"thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
								"price": "$16.99",
								"series": "Aquaman",
								"type": "graphic novel"
							},
							{
								"thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
								"price": "$2.99",
								"series": "Batgirl",
								"type": "comic book"
							},
							{
								"thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
								"price": "$3.99",
								"series": "Batman",
								"type": "comic book"
							},
							{
								"thumb": "https://upload.wikimedia.org/wikipedia/it/8/8d/Batman_beyond_1-195x300.jpg",
								"price": "$2.99",
								"series": "Batman Beyond",
								"type": "comic book"
							},
							{
								"thumb": "https://www.fumetto-online.it/ew/ew_albi/images/DC%20COMICS/323412_20141217060820_large.jpg",
								"price": "$3.99",
								"series": "Batman/Superman",
								"type": "comic book"
							},
							{
								"thumb": "https://static1.cbrimages.com/wordpress/wp-content/uploads/2020/09/Batman-Superman-Annual-Cv1.jpg",
								"price": "$4.99",
								"series": "Batman/Superman Annual",
								"type": "comic book"
							},
							{
								"thumb": "https://m.media-amazon.com/images/I/41nGyVF7C2L.jpg",
								"price": "$5.99",
								"series": "Batman: The Joker War Zone",
								"type": "comic book"
							},
							{
								"thumb": "https://www.ibs.it/images/9788828737711_0_536_0_75.jpg",
								"price": "$6.99",
								"series": "Batman: Three Jokers",
								"type": "comic book"
							},
							{
								"thumb": "https://i.ebayimg.com/images/g/YgYAAOSwu0BfjPo5/s-l1200.jpg",
								"price": "$4.99",
								"series": "Batman: White Knight Presents: Harley Quinn",
								"type": "comic book"
							},
							{
								"thumb": "https://mycomics.it/wp-content/uploads/sites/16/2022/12/FUMCAWOPA0008.jpg",
								"price": "$16.99",
								"series": "Catwoman",
								"type": "graphic novel"
							}
							]
			}
		},
    };
</script>

<template>
    <section class="hero">
        <div class="container">
            <div>current series</div>
        </div>
    </section>
    <section class="comics">
        <div class="container">
            <SingleCard v-for="comic in comics" :comic="comic"></SingleCard>
            <button type="button">load more</button>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

    section.hero{
        height: 300px;
        background-image: url(../src/assets/img/jumbotron.jpg);
        background-position: center top;
        background-size: cover;
        .container{
            height: 100%;
            position: relative;
            div{
                background-color: $primary_color;
                text-transform: uppercase;
                padding: 10px 20px;
                color: white;
                font-weight: 600;
                position: absolute;
                bottom: 0;
                left: 0;
                transform: translateY(50%);
            }
        }
    }

    section.comics{
        background-color: $secondary_dark;
        color: white;
        .container{
            padding: 20px 0px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        button{
            background-color: $primary_color;
            text-transform: uppercase;
            padding: 10px 40px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            margin: 10px auto;
        }
    }
</style>