<script>
  import List from '$components/List.svelte';
  import choclo from '$img/choclo.svg';
  import zapallo from '$img/zapallo.svg';
  import hongo from '$img/hongo.svg';
  import { onMount } from 'svelte';

  // Define images in items lists
  let items1 = [
    
  ];
  let items2 = [
    { id: 1, title: 'Choclo', src: choclo },
    { id: 2, title: 'Zapallo', src: zapallo },
    { id: 3, title: 'Hongo', src: hongo }
  ];


  

  function handleSection1Update(ids) {
    console.log('Tracked IDs in Section 1:', ids);
  }

  

</script>

<div class="main-thing">

  <h6>You have three ingredients <br>You can choose one, two, or all three <br>The arrangement determines the cooking order</h6>

  <h1>Your task is to determine the number of arrangements</h1>

  <!-- Pass unique types and custom classes -->
  <List items={items1} type="zone1" customClass="light-style" on:trackUpdate={e => handleSection1Update(e.detail)} />
  <List items={items2} type="zone1" customClass="dark-style" />
</div>

<style>
  .main-thing {
    display: flex;
    justify-content: center; 
    align-items: center;
    flex-direction: column; 
    width: 100%;
    height: 100vh;
    padding: 0.5em;
    box-sizing: border-box;
  }

  h1 {
    font-size: 3rem;
    font-weight: 900;
    color: #333333;
    padding-bottom: 45px;
    text-align: center;
    max-width: 80%;
    
  }

  h6 {
    font-size: 2rem;
    font-weight: 600;
    color: #333333;
    padding-bottom: 35px;
    text-align: center;
    max-width: 80%;
    
  }
</style>

