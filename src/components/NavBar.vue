<template>
  <div class="navbar-wrapper">
    <nav class="navbar">
      <ul class="nav-list">
        <li class="nav-item"><a href="#">Microsoft 365</a></li>
        <li class="nav-item"><a href="#">Teams</a></li>
        <li class="nav-item"><a href="#">Copilot</a></li>
        <li class="nav-item"><a href="#">Windows</a></li>
        <li class="nav-item"><a href="#">Xbox</a></li>
        <li class="nav-item"><a href="#">Destek</a></li>
      </ul>
      <div class="nav-actions">
        <a @click="toggleMenu" href="#">Tüm Microsoft</a>
        <a href="#">Ara <a href="#" class="fa fa-search"> </a></a>
        <a href="#">Sepet <a href="#"  class="fa fa-shopping-cart"> </a></a>
        <a href="#"
          >Hesabınızda oturum açın <a href="#" class="fa fa-user-circle"> </a>
        </a>
      </div>
    </nav>

    <div v-if="menuOpen" class="dropdown-menu">
      <div class="menu-list-wrapper">
        <ul>
          <li>Yazılım</li>
          <li><a href="#">Windows uygulamaları</a></li>
          <li><a href="#">Yapay Zeka</a></li>
          <li><a href="#">One Drive</a></li>
          <li><a href="#">Outlook</a></li>
          <li><a href="#">Skype</a></li>
          <li><a href="#">OneNote</a></li>
          <li><a href="#">Microsoft Teams</a></li>
        </ul>
        <ul>
          <li>PCs ve cihazlar</li>
          <li><a href="#">x box alın</a></li>
          <li><a href="#">aksesuarlar</a></li>
        </ul>
        <ul>
          <li>Eğlence</li>
          <li><a href="#">Xbox Game Pass Ultimate</a></li>
          <li><a href="#">Xbox Live Gold</a></li>
          <li><a href="#">Xbox ve oyunlar</a></li>
          <li><a href="#">PC Oyunları </a></li>
          <li><a href="#">Windows Oyunları</a></li>
        </ul>
        <ul>
          <li>İş</li>
          <li><a href="#">Microsoft Cloud</a></li>
          <li><a href="#">Microsoft Güvenlik</a></li>
          <li><a href="#">Azure</a></li>
          <li><a href="#">Dynamics 365</a></li>
          <li><a href="#">Microsoft Industry </a></li>
          <li><a href="#">Microsoft Power Platform</a></li>
          <li><a href="#">Windows 365</a></li>
        </ul>
        <ul>
          <li>Geliştirici ve BT</li>
          <li><a href="#">Geliştirici Merkezi</a></li>
          <li><a href="#">Belgeler</a></li>
          <li><a href="#">Microsoft Learn</a></li>
          <li><a href="#">Microsoft Tech Community</a></li>
          <li><a href="#">Azure Market</a></li>
          <li><a href="#">AppSource</a></li>
          <li><a href="#">Visual Studio </a></li>
        </ul>
        <ul>
          <li>Diğer</li>
          <li><a href="#">Ücretsiz yüklemeler ve güvenlik</a></li>
          <li><a href="#">Eğitim</a></li>
        </ul>
      </div>
      <div>
        <button style="width: 100%">Site Haritasını Göster ></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "myNavBar",

  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
  },
};
</script>

<style scoped src="../styles/nav-bar.css"></style>
