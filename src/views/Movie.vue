<template>
<div class="container">
  <div class="content">
    <div class="row">
    <movie-component
            v-for="(movie, index) in movies"
            v-bind="movie"
            :index="index"
            :key="movie.id"
            @view="view"
            @rentals="rentals"
    ></movie-component>
    </div>
  </div>
  <div class="icon-bar">
    <a href="#" class="facebook"><i class="fa fa-facebook"></i></a>
    <a href="#" class="twitter"><i class="fa fa-twitter"></i></a>
    <a href="#" class="google"><i class="fa fa-google"></i></a>
    <a href="#" class="linkedin"><i class="fa fa-linkedin"></i></a>
    <a href="#" class="youtube"><i class="fa fa-youtube"></i></a>
  </div>
</div>
</template>

<script>

    function Movie ({ id, title, rating, length, onDVD, onBluRay, updated_at}) {
        this.id = parseInt(id)
        this.title = title
        this.rating = rating
        this.length = length
        this.onDVD = onDVD
        this.onBluRay = onBluRay
        this.updated_at = updated_at
    }
    /* Go get the code for the customer-component tag that is in the template */
    import MovieComponent from '@/components/MovieComponent.vue'

    export default {
        data () {
            return {
                movies: []
            }
        },
        methods: {
            read () {
                this.movies = []
                window.axios.get('https://codeflare.tech/api/movies').then(({ data }) => {
                    data.forEach(movie => {
                        this.movies.push(new Movie (movie))
                    })
                })
            },
            view (id) {
            },
            rentals (id) {
            }
        },
        components: {
            MovieComponent
        },
        created () {
            this.read()
        }
    }
</script>
<style>

</style>