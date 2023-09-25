<script setup>
import {ref} from 'vue'

let num = ref(0)
</script>

<template>
 <nav class=" navbar navbar-expand-lg navbar-white bg-white border-bottom border-body">
    <div class="container-fluid">
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR6M2R7iMFqz_MN0W-jcQWsFzcq7L47YfwysWdfyh9xmQ&s" class="card-img-top" alt="..."
            height="60">
          </li>
          <li class="nav-item">
            <router-link to="/" class="navbar-brand">Rick and Morty</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/" class="nav-link" aria-current="page">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/about" class="nav-link" aria-current="page">About</router-link>      
          </li>
        </ul>
      </div>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      
    </div>
 </nav>
 <div class="main">
  <router-view>

  </router-view>
 </div>

 <footer class="bg-dark text-light">
  <div>Unimar | ADS | {{ new Date().getFullYear() }}</div>
 </footer>
</template>

<style>
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}

</style>

