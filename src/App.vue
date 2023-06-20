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
  <h1> Life's a Beach for Jim Penner</h1>
  <h5>Sound by Zapsplat</h5><audio controls preload muted>

    <source src="./Assets/noisecreations_AMB-NCFREE02_EnglishCoast-Waves-DistantSeagulls.mp3" type="audio/mpeg">

  </audio>
  <div @mouseenter="hover = true" @mousreleave="hover = false" class="container" :class="{ 'container-hover': hover }">
    <h4>Hover here...enjoy rolling waves, while you view:</h4>
  </div>
  <div>
    <div class="container">
      <h3><b>Life's a Beach with my wife!</b></h3>

      <div v-if="chooseOption === 'pic1'">
        <figure> <img alt="Beach1" class="image" src="./assets/beach1.JPG" width="396" height="504">
          <figcaption> Coolum : Our 1st beach pic </figcaption>
        </figure>

      </div>
      <div v-if="chooseOption === 'pic2'">
        <figure><img alt="Beach2" class="image" src="./assets/beach6.JPG" width="450" height="330">
          <figcaption> Moffat Beach: with Teddy </figcaption>
        </figure>

      </div>
    </div>
    <select class="pic-select" v-model="chooseOption">
      <option value="pic1">1st Pic</option>
      <option value="pic2">2nd Pic</option>
    </select>


    <div class="container">
      <h3> <b>Life's a beach with my Daughters!</b></h3>

      <div v-if="chooseOption === 'pic3'">
        <figure> <img alt="Beach3" class="image" src="./assets/bikebeachcp1.JPG" width="376" height="502">
          <figcaption> Venice Beach: with Charlotte Mar '15 </figcaption>
        </figure>

      </div>
      <div v-if="chooseOption === 'pic4'">
        <figure> <img alt="Beach4" class="image" src="./assets/bikebeach2op.JPG" width="376" height="502">
          <figcaption> Venice Beach: with Lilly Mar '17 </figcaption>
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
  background-color: purple;
  color: white;
  transition-duration: 6ms;
  padding: 40 px;
}

.container {
  background-color: coral;
  font-weight: 600;
  font-size: 24px;
  color: rgb(20, 78, 97);
  align-items: center;
  justify-content: center;
  height: 63vh;
  width: 48vh;
  border: 3 px solid #740e0e;

}

.container-hover {
  background-color: bisque;
  font-weight: 400;
  font-size: 16px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: rgb(128, 27, 69);
  height: 15vh;
  width: 11vh;
}


@media (min-width: 1024px) {
  template {
    display: grid;
    place-items: center;
    padding-right: 50%;
  }

}
</style>
