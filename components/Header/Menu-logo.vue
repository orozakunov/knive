<script setup>
import LogoIconMenu from "@/assets/Social/logo.svg";
import swal from "sweetalert";

// const test = () => {
//   swal({
//     text: 'Search for a movie. e.g. "La La Land".',
//     content: "input",
//     button: {
//       text: "Search!",
//       closeModal: false,
//     },
//   })
//     .then((name) => {
//       if (!name) throw null;

//       return fetch(`https://itunes.apple.com/search?term=${name}&entity=movie`);
//     })
//     .then((results) => {
//       return results.json();
//     })
//     .then((json) => {
//       const movie = json.results[0];

//       if (!movie) {
//         return swal("No movie was found!");
//       }

//       const name = movie.trackName;
//       const imageURL = movie.artworkUrl100;

//       swal({
//         title: "Top result:",
//         text: name,
//         icon: imageURL,
//       });
//     })
//     .catch((err) => {
//       if (err) {
//         swal("Oh noes!", "The AJAX request failed!", "error");
//       } else {
//         swal.stopLoading();
//         swal.close();
//       }
//     });
// };
</script>

<template>
  <div class="menu-logo">
    <router-link to="/">
      <img class="logo-img" @click="test" :src="LogoIconMenu" alt=""
    /></router-link>
  </div>
</template>

<style>
.menu-logo {
  margin: 0 155px 0 0;
}
@media screen and (max-width: 376px) {
  .menu-logo {
    margin: 0 10px 0 -5px;
  }
  .logo-img {
    height: 30px;
  }
}
</style>
