<script setup>
import { ref } from "vue"
let num = ref(0)
</script>

<template>
  <nav class="navbar navbar-expand-lg border-bottom">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">Rick and Morty</router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbar" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="main">
    <router-view></router-view>
  </div>

  <footer>
    <div>
      Unimar | Rick and Morty | {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>

<style>
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  background-color:  rgb(0, 255, 234);
}
</style>

<style>
nav {
  background-color:  rgb(0, 255, 234);
  color: black;
}
</style>

