<template>
    <div>
        <button @click="toggleTweet">List Layout/Grid Layout</button>
        <article></article>

    </div>
</template>

<script>
    export default {
        name: "TweetList",
        data() {
            return{
                isListVisible : false,
                tweets : [
                {
                    tweet : "I'm fast, but it would take me three matches to run this far",
                    userName : "Cristiano Ronaldo",
                    dateCreated :  "05-05-2017"
                },
                {
                    tweet : "Hey world. Ya boy is back and I'm here in beautiful lala land",
                    userName : "Dwight Howard",
                    dateCreated : "08-05-2012"
                },
                {
                    tweet : "Kobe and Harden setting up for the 100M final",
                    userName : "Kevin Love",
                    dateCreated : "05-15-2014"
                },
                {
                    tweet : "I'm glad I don't get interviewed by tha diaper breath bandit in DC anymore",
                    userName : "Javale Mcgee",
                    dateCreated : "07-30-2012"
                }
                ],
            }
        },
        methods : {
            makeTweets(){
                for (let getTweets of this.tweets){
                    console.log(getTweets);
                    document.querySelector(`article`).insertAdjacentHTML(`beforeend`, `<p>${getTweets.tweet}</p>`);
                    document.querySelector(`article`).insertAdjacentHTML(`beforeend`, `<p>${getTweets.userName}</p>`);
                    document.querySelector(`article`).insertAdjacentHTML(`beforeend`, `<p>${getTweets.dateCreated}</p>`);
                }
            },
        },
        mounted(){
            this.makeTweets();
        },
    }

</script>

<style scoped>

</style>