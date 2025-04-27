<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img :src="logo">
          </q-avatar>
          Title
        </q-toolbar-title>
		<q-btn outline color="white" icon="login">
		Log in
		</q-btn>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup>
import logo from 'src/assets/logo.png';
</script>