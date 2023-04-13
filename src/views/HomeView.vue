<template>
    <div class="about">
        <div className="intro">
            <h1 >Welcome to my collection of books!</h1>
        </div>
        <b-button>See the books</b-button>
    </div>
</template>

<style>
@media (min-width: 1024px) {


    .intro {
    color: bisque;
    border: 2px solid white;
    background-color: rgba(128, 128, 128, 0.8);
    margin-top: 40px;

}

    .about {
    min-height: 100vh;
    border: 2px solid black;
	padding: 250px;
    padding-bottom: 200px;
    padding-top: 150px;
    background-image: url('../img/library.jpeg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
}
}
</style>
