<script>
export default {
  data() {
    return {
      hover: false,
      chooseOption: null,
    };
  },
};
</script>

<template>
  <h1> Life's a Beach for Jim Penner!</h1>
  <div @mouseenter="hover = true" @mousreleave="hover = false" class="container" :class="{ 'container-hover': hover }">
    <h4>Hover here</h4>
  </div>
  <div>
    <div class="container">
      <h3>Life's a Beach with my wife!</h3>

      <div v-if="chooseOption === 'pic1'">
        <figure> <img alt="Beach1" class="image" src="./assets/beach1.JPG" width="330" height="420">
          <figcaption> Coolum : 1st beach pic </figcaption>
        </figure>

      </div>
      <div v-if="chooseOption === 'pic2'">
        <figure><img alt="Beach2" class="image" src="./assets/beach6.JPG" width="450" height="330">
          <figcaption> Moffat Beach with Teddy </figcaption>
        </figure>

      </div>
    </div>
    <select class="pic-select" v-model="chooseOption">
      <option value="pic1">1st Pic</option>
      <option value="pic2">2nd Pic</option>
    </select>


    <div class="container">
      <h3> Life's a beach with my Daughters!</h3>

      <div v-if="chooseOption === 'pic3'">
        <figure> <img alt="Beach3" class="image" src="./assets/bikebeachcp1.JPG" width="384" height="512">
          <figcaption> Venice Beach with Charlotte Mar '15 </figcaption>
        </figure>

      </div>
      <div v-if="chooseOption === 'pic4'">
        <figure> <img alt="Beach4" class="image" src="./assets/bikebeach2op.JPG" width="384" height="512">
          <figcaption> Venice Beach with Lilly Mar '17 </figcaption>
        </figure>

      </div>
    </div>
    <select class="pic-select" v-model="chooseOption">
      <option value="pic3">3rd Pic</option>
      <option value="pic4">4th Pic</option>
    </select>

  </div>
</template>



<style scoped>
template {
  height: 100vh;
  background-color: blue;
  transition-duration: 1ms;
}

img {
  justify-content: center;
}

.container {
  background-color: coral;
  font-weight: 600;
  font-size: 24px;
  color: rgb(20, 78, 97);
  height: 64vh;
  width: 50vh;

}

.container-hover {
  background-color: bisque;
  font-weight: 400;
  font-size: 16px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: rgb(128, 27, 69);
  height: 8vh;
  width: 5vh;
}

.main {
  background-color: bisque;
  font-weight: 600;
  font-size: 24px;
  color: lightslategray;
  height: 65vh;
  width: 46vh;
}


@media (min-width: 1024px) {
  template {
    display: grid;
    place-items: center;
    padding-right: 50%;
  }

}
</style>
