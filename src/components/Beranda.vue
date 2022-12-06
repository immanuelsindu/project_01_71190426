<template>
  <div id="menu">
    <h3>Daftar Makanan</h3>
    <ol>
      <li><a href="#">Makanan</a></li>
      <li><a href="#">Minuman</a></li>
      <li><a href="#">Snack</a></li>
    </ol>

  </div>

  <div id="itemMenu">
    <h2>Selamat Datang di Aplikasi MacDonal, Silahkan Pesan Makanan Anda</h2>
  </div>
</template>

<script>
export default {
  name: 'hal-beranda'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #menu{
    width: 200px;
    height: 606px;
    background-color:#E15D5D ; 
    float: left;
  }
  #menu h3{
    text-align: center;
    padding-top: 20px;
  }
  #menu ol li{
    color: white;
    line-height: 30px;
    list-style-type: none;
  }
  #menu ol li a{
    color: white;
    text-decoration: none;
  }

  #itemMenu{
    width: 600px;
    height: 600px;
    border: 3px solid #E15D5D;
    float: left;
  }

  #itemMenu h2{
    margin-top: 45%;
    text-align: center;

  }
</style>
