<style>
  nav {
    height: 80px;
    padding: 15px;
    text-align: left;
    line-height: 80px;
  }
  #logo {
    font-size: 31px;
    font-weight: bold;
  }
  #controls {
     float: right;
  }
</style>

<script>
  import { token } from '../stores';
  import { navigate } from 'svelte-routing';

  function logOut() {
    navigate('/', { replace: true });
    token.unset();
  }
</script>

<nav>
   <a href="/">
     <span id="logo"> FaceIT!</span>
   </a>
   <div id="controls"> 
    <a href="" on:click={logOut}>Log out</a>
   </div>
</nav>
