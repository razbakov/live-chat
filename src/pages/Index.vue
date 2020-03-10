<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          Meetup Chat
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <q-page>
        <q-list bordered padding separator>
          <q-item v-for="message in Array(100)" :key="message">
            <q-item-section top avatar>
              <q-avatar>
                <img src="https://cdn.quasar.dev/img/boy-avatar.png">
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label>John Doe</q-item-label>
              <q-item-label caption>Hello.</q-item-label>
            </q-item-section>

            <q-item-section side top>
              19:27
            </q-item-section>
          </q-item>
        </q-list>
      </q-page>
    </q-page-container>

    <q-footer elevated class="bg-white q-pa-md">
      <q-input v-model="message" label="Write a message" />
    </q-footer>
  </q-layout>
  
</template>

<script>
export default {
  name: 'PageIndex',
  data: () => ({
    message: ''
  })
}
</script>
