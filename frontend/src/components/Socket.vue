<template>
  <div :class="{ blue: frontComparator }">Front</div>
  <div :class="{ blue: socketComparator }">Socket</div>
  <input type="text" v-model="textToCompare"/>
</template>
<script>

export default {
  name: "Socket",
  data: () => ({
    socket: new WebSocket("ws://172.17.0.1:8080/test"),
    textToCompare: "",
    socketComparator: false,
    frontComparator: false,
  }),
  mounted() {
    this.socket.addEventListener("message", ({ data }) => {
      this.socketComparator = data == "true";
    });
  },
  watch: {
    textToCompare: function (val) {
      this.socket.send(val);
      this.frontComparator = val == "test";
    }
  }
}
</script>

<style>
  .blue { background-color: blue;}
</style>
