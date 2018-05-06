<template>
  <section class="signin">
    <div>
      <logo/>
      <h1 class="title">
        MyReader
      </h1>
      <h2 class="subtitle">
        Tech News Reader by yourself
      </h2>
      <div class="links">
        <a href="/feeds/" class="button" >Signin with Google</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  layout: 'signin'
}
</script>

<style>
.signin
{
  background-image: url("~assets/images/login-bg.png");
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  background-color: #464646;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #fff;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 18px;
  color: #fff;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
.button
{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #fff;
  color: #fff;
  text-decoration: none;
  padding: 10px 30px;
}
.button:hover
{
  color: #fff;
  text-decoration: none;
}
</style>
