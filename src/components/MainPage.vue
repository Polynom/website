<template>
  <!-- Primary Page Layout
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <div class="container">
    <div class="row">
      <div class="one-half culumn" style="margin-top: 25%">
        <img id="logo" src="../assets/polynom_logo.png">
        <h2> Simply doing stuff </h2>
        <h3> We are</h3>
<!--        <h3> <router-link to="/team"> We</router-link> are</h3>-->
        <ul>
          <li> <router-link to="/build">building</router-link> decentralized applications </li>
          <li> <router-link to="/research">researching</router-link> expressivity of tech </li>
          <li> <router-link to="/organize">organizing</router-link> events </li>
          <li> <router-link to="/support">supporting</router-link> communities </li>

        </ul>

        <p> Our interests lie in privacy, security and, wherever applicable, <span id="transparency" @click="transTog" @mouseover="transIn" @mouseout="transOut" >transparency</span>.</p>
      </div>
      <div class="" style="margin-top: 10%">
        <h4> You name it:  </h4>
        <p> <a href="mailto:root@polynom.com"> root@polynom.com</a> <a href="../../static/polynom-pgp" target="_blank"> (PGP) </a> </p>
        <p id="mandatory"> POLYNOM OÜ (14418967), Sepapaja 6, 15551, Tallinn, Estonia </p>
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
    transIn: () => {
      document.getElementById('bg').classList.add('trans')
      document.getElementById('transparency').classList.add('transText')
    },
    transOut: () => {
      document.getElementById('bg').classList.remove('trans')
      document.getElementById('transparency').classList.remove('transText')
    },
    transTog: () => {
      if (document.getElementById('bg').classList.length === 0) {
        document.getElementById('bg').classList.add('trans')
        document.getElementById('transparency').classList.add('transText')
      } else {
        document.getElementById('bg').classList.remove('trans')
        document.getElementById('transparency').classList.remove('transText')
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

  #transparency:hover {
    color: #FFFFFF;
    cursor: none;
    opacity: 1;
  }

  .transText {
    color: #FFFFFF;
    cursor: none;
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
</style>
