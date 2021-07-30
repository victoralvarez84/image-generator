<template>
  <header>
      <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
    props: ['title']
}
</script>

<style Lang="scss" scoped>
   header{
       padding: 24px 32px;
       display:flex;
       justify-content: center;
   }

   h1{
       font-size:32px;
       font-weight:700;
       text-align:center;
       text-transform: uppercase;
       font-family: Futura;
   }

</style>