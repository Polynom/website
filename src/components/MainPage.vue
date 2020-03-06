<template>
  <!-- Primary Page Layout
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <div class="container">
    <div class="row">
      <div class="one-half" style="margin-top: 25%">

        <div>
          <img id="logo-w" class="hidden" src="../assets/polynom_logo.png">
          <img id="logo" src="../assets/polynom_logo.png">
          <h2 id="cao" class="hidden"> Chao Ab Ordo </h2>
          <h2 id="cfo"> Chaos comes from Order </h2>

        </div>

        <div id="nav">
          <h3> We are</h3>
          <!-- <h3> <router-link to="/team"> We</router-link> are</h3>-->
          <ul>
            <li> <router-link to="/build">building</router-link> decentralized applications </li>
            <li> <router-link to="/research">researching</router-link> technology </li>
            <li> <router-link to="/organize">organizing</router-link> events </li>
            <li> <router-link to="/support">supporting</router-link> communities </li>
          </ul>
          <p id="overtrans"> Our interests lie in privacy, security and, wherever applicable,</p>
        </div>
        <span id="transparency" @click="transTog">transparency</span>
        <div id="contact" style="margin-top: 10%">
          <h4> You name it:  </h4>
          <p> <a href="mailto:root@polynom.com"> root@polynom.com</a> <a href="./polynom-pgp" target="_blank" download> (PGP) </a> </p>
        </div>

        <div>
          <p id="mandatory"> POLYNOM OÜ (14418967), Sepapaja 6, 15551, Tallinn, Estonia </p>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainPage',
  data () {
    return {
    }
  },
  methods: {
    transTog: () => {
      if (document.getElementById('bg').classList.length === 0) {
        document.getElementById('bg').classList.add('trans')
        document.getElementById('transparency').classList.add('transText')

        document.getElementById('logo').classList.add('hidden')
        document.getElementById('logo-w').classList.remove('hidden')

        document.getElementById('cfo').classList.add('hidden')
        document.getElementById('cao').classList.remove('hidden')

        document.getElementById('nav').classList.add('hidden')
        document.getElementById('contact').classList.add('hidden')

      } else {
        document.getElementById('bg').classList.remove('trans')
        document.getElementById('transparency').classList.remove('transText')
        document.getElementById('logo').classList.remove('hidden')
        document.getElementById('logo-w').classList.add('hidden')

        document.getElementById('cfo').classList.remove('hidden')
        document.getElementById('cao').classList.add('hidden')

        document.getElementById('nav').classList.remove('hidden')
        document.getElementById('contact').classList.remove('hidden')
      }
    }
  }
}
</script>

<style scoped>
  #logo {
    height: 54px;
    margin: 12px 0px;
  }

  #logo-w {
    height: 54px;
    margin: 12px 0px;
    filter: invert(100%);
    position: absolute;
  }

  #overtrans {
    margin-bottom: 0px;
  }

  #transparency {
    border-bottom: 1px dotted;
  }
  #transparency:hover {
    cursor: pointer;
    opacity: 0.5;
  }

  #cao {
    color: #FFFFFF;
    position: absolute;
  }

  #cfo {
    color: #000000;
    visibility: hidden;
  }

  .transText {
    color: #FFFFFF;
    opacity: 1;
  }

  #mandatory {
    color: #FFFFFF;
    opacity: 1;
  }

  h2 {
    opacity: 0.42;
  }
  a {
    color: #000;
    text-decoration: none;
    border-bottom: 2px dotted;
    font-weight: 600;
  }

  a:hover {
    color: #1EAEDB;
  }

  ul {
    list-style-type: none;
    margin: 0px 0px 20px 20px;
    padding: 0;
  }

  .hidden {
    visibility: hidden;
  }

</style>
