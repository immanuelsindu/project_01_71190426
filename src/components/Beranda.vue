<template>
  <div id="menu">
    <h3>Daftar Makanan</h3>
    <ol>
      <li @click="showMakanan()"><a href="#">Makanan</a></li>
      <li @click="showMinuman()"><a href="#">Minuman</a></li>
      <li @click="showSnack()"><a href="#">Snack</a></li>
    </ol>

    <div id="checkoutBtn">
      <button>
        Checkout
      </button>
    </div>
    
  </div>

  <div id="itemMenu">
    <h2 v-show="isItemMenu">
      Selamat Datang di Aplikasi MacDonal, Silahkan Pesan Makanan Anda
    </h2>

    
    <div v-show="isMakanan" id="makanan" >
      <div @click="detailMenu()" id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>GigaMac</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan2.jpg" alt="makanan1">
        <p>Cheese Burger</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan3.jpg" alt="makanan1">
        <p>Mac Nugget</p>
      </div>
    </div>

  
    <div v-show="isMinuman" id="makanan" >
      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Es Teh</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Es Jeruk</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Es Good day</p>
      </div>
    </div>


    <div v-show="isSnack" id="makanan" >
      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Tempe Goreng</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Sate Usus</p>
      </div>

      <div id="itemMakanan">
        <img src="../assets/makanan1.jpg" alt="makanan1">
        <p>Pisang Coklat</p>
      </div>
    </div>

    <div v-show="isDetailMenu" id="detailMenu">
      <div id="menuKiriMakan">
        <h3>Pedas/Tidak</h3>
        <p @click="(isBoldTipe = true, isBoldTipe2= false)" v-bind:class="{boldTipe: isBoldTipe}">Pedas</p>
        <p @click="(isBoldTipe2 = true, isBoldTipe = false)" v-bind:class="{boldTipe: isBoldTipe2}">Tidak</p>
        
        <h3>Ekstra Kentang(+10.000)</h3>
        <p @click="(isBoldTipe3 = true, isBoldTipe4= false)" v-bind:class="{boldTipe: isBoldTipe3}">Ya</p>
        <p @click="(isBoldTipe4 = true, isBoldTipe3 = false)" v-bind:class="{boldTipe: isBoldTipe4}">Tidak</p>
      </div>
      

      <div id="menuKananMakan">
          <img src="../assets/makanan1.jpg" alt="fotoItemMakanan">
          <p>GigaMac</p>
          <p>Rp 70.000</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'hal-beranda',
    data(){
      return{
        isItemMenu : true,
        isMakanan : false,
        isMinuman : false,
        isSnack: false,
        isBoldTipe: false,
        isBoldTipe2: false,
        isBoldTipe3: false,
        isBoldTipe4: false,
        isDetailMenu: false
       
      }
    },
    methods:{
      showMakanan(){
        this.isItemMenu = false
        this.isMakanan = true
        this.isMinuman = false
        this.isSnack = false
        this.isDetailMenu = false
      },
      showMinuman(){
        this.isItemMenu = false
        this.isMakanan = false
        this.isMinuman = true
        this.isSnack = false
        this.isDetailMenu = false
      },
      showSnack(){
        this.isItemMenu = false
        this.isMakanan = false
        this.isMinuman = false
        this.isSnack = true
        this.isDetailMenu = false
      },
      detailMenu(){
        this.isDetailMenu = true
        this.isMakanan = false
      }

    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    #menu {
      width: 200px;
      height: 606px;
      background-color: #e15d5d;
      float: left;
    }
    #menu h3 {
      text-align: center;
      padding-top: 20px;
    }
    #menu ol li {
      color: white;
      line-height: 30px;
      list-style-type: none;
    }
    #menu ol li a {
      color: white;
      text-decoration: none;
    }

    #itemMenu {
      width: 600px;
      height: 600px;
      border: 3px solid #e15d5d;
      float: left;
    }

    #itemMenu h2 {
      margin-top: 45%;
      text-align: center;
    }

    #makanan{
      margin: 30px;
    }
    #itemMakanan{
      width: 150px;
      height: 150px;
      padding-bottom: 20px;
      border: 1px solid black;
      float: left;
      margin-right: 20px;
      margin-top: 20px;
    }
    #itemMakanan img{
      width: 150px;
    }
    #itemMakanan p{
      margin: 0px;
      text-align: center;
      font-weight: bold;
    }


    #detailMenu{
      margin: 20px;
    }
    #menuKiriMakan{
      width: 50%;
      height: 550px;
      float: left;
    }

    #menuKananMakan{
      width: 50%;
      height: 550px;
      text-align: center;
      float: left;
    }

    #menuKiriMakan p:nth-child(3){
      color: gray;
      
      margin-right: 20px;
    }
    #menuKiriMakan p:nth-child(2){
      color: gray;
      float: left;
      margin-right: 30px;
    }

    #menuKiriMakan p:nth-child(5){
      color: gray;
      float: left;
      margin-right: 20px;
    }
    #menuKiriMakan p:nth-child(6){
      color: gray;
      float: left;
      margin-right: 30px;
    }

    #menuKiriMakan h3{
      margin: 0;
    }

    .boldTipe{
      font-weight: bold;
        color: black !important
    }

    #checkoutBtn button{
      text-align: center;
      background-color: #EAED5B;
      padding: 10px 20px;
      border-radius: 5px;
      font-weight: bold ;
      border:0px;
    }
</style>
