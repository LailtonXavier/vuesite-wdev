<template>
  <main>

    <div class="text-top">
      Projeto feito usando VueJS, estou refazendo esse projeto,
      consumindo a Api do canal WDEV
    </div>

    <a
     href="https://www.youtube.com/watch?v=kmsM_hHrDHE"
     target="_black"
     >
      <img id="subscribe" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="ir para tutorial">
     </a>

     <div class="text-bottom">tutorial/wdevoficial</div>

  </main>

</template>

<script>

  export default {
    name: 'Home',
  }

</script>

<style scoped>

main {
  background-color: var(--color-background-home);
  justify-content: center;
  align-items: center;
  padding: 8px;
}

.text-top, .text-bottom {
  color: var(--color-text-light);
  font-size: 22px;
  text-align: center;
  margin-bottom: 20px;
}

.text-bottom {
  font-size: 10px;
  margin-top: 15px;
}

#subscribe {
  width: 340px;
}

@media (min-width: 700px) {
    #subscribe {
    width: 370px;
    }
    
  }



</style>
