<template>
  <div>
    <div class="row">
      <div class="col-3">
        <NuxtLink to="/good_ideas">
          <div class="idea">
            <img src="../assets/svg/idea.svg" width="240px" />
          </div>
        </NuxtLink>
        <NuxtLink to="/bad_ideas">
          <div class="trash">
            <img src="../assets/svg/basket.svg" width="240px" />
          </div>
        </NuxtLink>
      </div>
      <div class="col-3-sm"></div>
      <div class="col-6">
        <h1 class="title">Ideas and a trash can</h1>
        <p>
          I upload my ideas on this website daily. Good ideas go into the ideas
          section and bad ideas go into the trash can.
        </p>
        <br>
        <p>
          Visit my <a href="https://github.com/grayusan">Github</a> profile!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

 <style>
@import url("https://fonts.googleapis.com/css2?family=Londrina+Outline&display=swap");
img {
  max-width: 240px;;
  height: auto;
}
</style>