<template>
  <div>
    <header>
      <div>
        <h1>Dora</h1>
        <h1>Diego</h1>
        <span>&</span>
      </div>
    </header>
    <section id="diego">
      <div class="profile-pic">
        <img src="../assets/diego_profile.png" />
        <h2>Diego</h2>
      </div>
      <div class="about">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      </div>
      <div class="photos">
        <img src="../assets/diego02.png" />
        <img src="../assets/diego01.png" />
        <img src="../assets/diego04.png" />
      </div>
    </section>
    <section id="dora">
      Dora
    </section>
  </div>
</template>

<script>
import { Vue } from 'vue-class-component';

export default class DoraDiego extends Vue{

}
</script>

<style scoped lang="scss">
  header, section {
    min-height: 100vh;
  }

  header {
    position: relative;
    background-image: url('../assets/doradiego.png');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    z-index: 0;

    div {
      position: absolute;
      text-align: left;
      right: 3em;
      font-size: 1.75rem;

      h1 {
        z-index: 1;
      }

      span {
        position: absolute;
        font-size: 11rem;
        top: 0;
        color: rgba(0,0,0,.1);
        z-index: 0;
      }
    }
  }

  section {
    padding: 3em;
  }

  .profile-pic {
    position: relative;
    width: fit-content;
    margin-bottom: 2em;

    img {
      height: 300px;
      clip-path:  polygon(0% 0%, 100% 0%, 70% 100%, 0% 100%);
    }
    h2 {
      position: absolute;
      background: #F8E1C4;
      width: 200px;
      font-size: 2rem;
      top: 60%;
      left: 60%;
      padding: 0.25em 0;
      text-align: center;
    }
  }

  .about {
    font-size: 1.25rem;
    line-height: 1.5;
    margin-bottom: 1em;
  }

  .photos {
    display: flex;
    flex-wrap: wrap;
    img {
      margin: 1em;
      // transform: rotate(90deg);
    }
  }
</style>