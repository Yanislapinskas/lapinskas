<template>
  <q-item
    clickable
    tag="a"
    target="_blank"
    :href="p.link"
  >
	 <q-item-section>
      <q-item-label>{{ p.title }}</q-item-label>
      <q-item-label caption v-if="p.caption!=''"> 
		<q-chip class="glossy" color="orange" text-color="white" icon-right="star">
			{{ p.caption }}
		</q-chip>
	  </q-item-label>
    </q-item-section>
	
    <q-item-section
      v-if="p.icon"
      avatar
    >
      <q-icon :name="p.icon" />
    </q-item-section>
  </q-item>
</template>

<script setup>
const p  = defineProps({
  title: {
    type: String,
    required: true
  },

  caption: {
    type: String,
    default: ''
  },

  link: {
    type: String,
    default: '#'
  },

  icon: {
    type: String,
    default: ''
  }
})
</script>
