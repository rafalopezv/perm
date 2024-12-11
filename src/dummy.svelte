<script>
    import pimiento from '$img/pimiento.svg'
    import lechuga from '$img/lechuga.svg'
    import zana from '$img/zanahoria.svg'
    import alca from '$img/alcachofa.svg'
    import coliflor from '$img/coliflor.svg'
    import pepino from '$img/pepino.svg'
    import arverja from '$img/arverja.svg'
    import brocoli from '$img/brocoli.svg'
    import apio from '$img/apio.svg'
    import choclo from '$img/choclo.svg'
    import zapallo from '$img/zapallo.svg'
    import repollo from '$img/repollo.svg'
    import cebolla from '$img/cebolla.svg'
    import hongo from '$img/hongo.svg'
    import palta from '$img/palta.svg'
    import tomate from '$img/tomate.svg'
    import ajo from '$img/ajo.svg'
  </script>
  
  <main>
    <!-- <img src={pimiento} alt="pimiento"> 
    <img src={lechuga} alt="lechuga"> 
    <img src={zana} alt="zanahoria"> 
    <img src={alca} alt="alcachofa"> 
    <img src={coliflor} alt="coliflor"> 
    <img src={pepino} alt="pepino"> 
    <img src={arverja} alt="arverja"> 
    <img src={brocoli} alt="brocoli"> 
    <img src={apio} alt="apio">  -->
    <img src={choclo} alt="choclo"> 
    <img src={zapallo} alt="zapallo"> 
    <!-- <img src={repollo} alt="repollo"> 
    <img src={cebolla} alt="cebolla">  -->
    <img src={hongo} alt="hongo"> 
    <!-- <img src={palta} alt="palta"> 
    <img src={tomate} alt="tomate"> 
    <img src={ajo} alt="ajo">  -->
  </main>
  
  <style>
    main {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 10px 5px; /* Smaller gap between rows and columns */
      height: 100vh;
      padding: 20px;
    }
  
    img {
      flex: 1 1 420px; /* Minimum width per item */
      max-width: 420px;
      height: auto;
    }
  
    /* Responsive adjustments for smaller screens */
    @media (max-width: 768px) {
      img {
        max-width: 80px; /* Adjust for tablets */
      }
    }
  
    @media (max-width: 480px) {
      img {
        max-width: 60px; /* Adjust for small screens */
      }
    }
  </style>