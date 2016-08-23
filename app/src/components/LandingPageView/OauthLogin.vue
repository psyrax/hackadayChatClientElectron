<style scoped>
  a {
    color: rgb(50, 174, 110);
    text-decoration: none;

    &:hover { color: rgb(40, 56, 76); }
  }

  ul {
    list-style-type: none;
    margin-top: 10px;
  }

  li { display: inline-block; }
</style>

<template>
  <ul>
    <li><button v-on:click="openoauth">Login</button></li>
  </ul>
</template>
<script>
  var options = {
    client_id: 'CJdGbZYiFOmlI9FZpHywkDYUAdU2fw7L97S9CuaSlO9zpaNa'
  }
  export default {
    methods: {
      openoauth () {
        var authWindow = new this.$electron.remote.BrowserWindow({ width: 800, height: 600, show: false, 'node-integration': false })
        var hackaDayUrl = 'https://auth.hackaday.io/authorize?'
        var authUrl = hackaDayUrl + 'client_id=' + options.client_id + '&state=&response_type=code'
        authWindow.loadURL(authUrl)
        authWindow.show()
        console.log('click', authUrl)
      }
    }
  }
</script>
