<template>
  <v-footer height="auto" class="toolb" color="#19D3CC">
    <v-layout justify-center row wrap>
      <v-flex color="indigo" dark py-3 text-xs-center white--text xs12>
        <div style="display: flex; justify-content: space-between">
          <img src="../assets/footer-logo.png" height="32" width="143" />
          <div>
            &copy;2020 —
            <a
              href="http://it-solutions.uz"
              style="text-decoration: none; color: white"
              ><strong>IT-Solutions</strong></a
            >
          </div>
        </div>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
* {
  margin: 0;
}
.toolb {
  padding: 0 5%;
  text-align: center;
  background-color: #19d3cc;
}
.ftr {
  display: flex;
  justify-content: space-between;
}
</style>