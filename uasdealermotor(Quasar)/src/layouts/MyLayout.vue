<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
       <q-toolbar class="bg-red-14 text-white" >
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          icon="menu"
          class="q-mr-sm"
          aria-label="Menu"
        />

        <q-toolbar-title>
        Aplikasi Dealer KONDA(Admin)
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-red-14 text-white"
    >
     <q-list>
        <q-item-label header class="text-white"> DAFTAR MENU</q-item-label>
    <q-tabs>
  <q-route-tab
    icon="home"
    to="/home"
    label="BERANDA"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="person"
    to="/root"
    label="DAFTARIN ADMIN"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="motorcycle"
    to="/daftarmotor"
    label="DAFTARIN MOTOR"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="list"
    to="/listmotor"
    label="LIST MOTOR"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="list"
    to="/listcustomer"
    label="LIST CUSTOMER"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="message"
    to="/pemesanan"
    label="LIST PEMESANAN"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="money"
    to="/transaksi"
    label="BUAT TRANSAKSI"
    exact
  />
</q-tabs>
    <q-tabs>
  <q-route-tab
    icon="list"
    to="/caritransaksi"
    label="DAFTAR TRANSAKSI"
    exact
  />
</q-tabs>
              <q-item clickable tag="a" target="_blank" >
          <q-item-section avatar>
            <q-icon name="logout" />
          </q-item-section>
          <q-item-section>
          <q-btn label="LOGOUT" to="/login" type="submit" color="red-14"/>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MyLayout',

  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
