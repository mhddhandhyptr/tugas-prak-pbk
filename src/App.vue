<template>
 
 <nav class="navbar">
    <div class="logo">Portofolio</div>
    <ul class="nav-links">
      <li><a href="#about">Menu</a></li>
      <li><a href="#work">Tentang Saya</a></li>
      <li><a href="#contact">Kontak</a></li>
    </ul>
  </nav>
  <div class="profile-page">
    <div class="profile-photo">
      <!-- Ganti 'url-foto-anda.jpg' dengan URL foto profil Anda -->
      <img src="../src/assets/dndy.jpeg" alt="Foto Profil">
    </div>
  </div>
  <div class="profile-page">
    <section class="about-me">
      <h2>Tentang Saya</h2>
      <p>{{ aboutMe }}</p>
    </section>
    <section class="my-work">
      <h2>Informasi</h2>
      <div v-for="work in works" :key="work.id">
        <h3>{{ work.title }}</h3>
        <p>{{ work.description }}</p>
      </div>
    </section>
  </div>
  <footer class="site-footer">
    <div class="container">
      <p>&copy; 2024 Muhammad Dhandhy Putera Irvantie</p>
      <p>Ikuti kami di sosial media:</p>
      <ul class="social-links">
        <li><a href="#" target="_blank">Facebook</a></li>
        <li><a href="#" target="_blank">Twitter</a></li>
        <li><a href="#" target="_blank">Instagram</a></li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'ProfilePage',
  data() {
    return {
      aboutMe: 'Saya Muhammad Dhandhy Putera Irvantie saat ini sedang berkuliah di Universitas Islam Riau Fakultas Teknik, Prodi Teknik Informatika.Saat ini saya masih semester 4 dan saya mempunyai minat dan bakat dalam bidang Database dan Networking.',
      works: [
        { id: 1, title: 'Pengalaman', description: 'Saya pernah mengikuti lomba basketball tingkat kabupaten/kota yang bernama HSBL.' },
        { id: 2, title: 'Hobi', description: 'Hobi saya yaitu bermain game dan basketball.' },
        // Tambahkan lebih banyak pekerjaan sesuai kebutuhan
      ]
    }
  }
}
</script>

<style>
.site-footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1rem 0;
}
.container {
  max-width: 1200px;
  margin: auto;
  padding: 0 1rem;
}
.social-links {
  list-style: none;
  padding: 0;
}
.social-links li {
  display: inline;
  margin: 0 0.5rem;
}
.social-links a {
  color: white;
  text-decoration: none;
  transition: color 0.3s ease-in-out;
}
.social-links a:hover {
  color: #4CAF50;
}
profile-page {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Menggunakan 100% dari tinggi viewport */
}

.profile-photo img {
  max-width: 200px; /* Atau ukuran lain sesuai keinginan Anda */
  border-radius: 50%; /* Membuat foto menjadi bentuk lingkaran */
}
@keyframes animatedBackground {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: bold;
  font-style: italic ;
  padding: 1rem;
  color: white;
  background: linear-gradient(270deg, #00d2ff, #3a7bd5, #ff758c);
  background-size: 600% 600%;
  animation: animatedBackground 10s ease infinite;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
}

.nav-links li {
  padding: 0 1rem;
}

.nav-links a {
  text-decoration: none;
  color: white;
  transition: color 0.3s ease-in-out;
}

.nav-links a:hover {
  color: #4CAF50;
}

.profile-page {
  max-width: 800px;
  margin: 30px auto;
  padding: 30px;
  background: linear-gradient(to right, #6dd5ed, #2193b0);
  border-radius: 10px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.about-me, .my-work {
  text-align: center;
  padding: 20px;
  color: #fff;
}

.about-me h2, .my-work h2 {
  margin-bottom: 15px;
  color: #ffefba;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}

.about-me p, .my-work div {
  background: rgba(255, 255, 255, 0.1);
  padding: 10px;
  border-radius: 4px;
  margin-bottom: 10px;
}

.my-work div {
  transition: transform 0.3s ease;
}

.my-work div:hover {
  transform: translateY(-5px);
}
.profile-photo img {
  display: block;
  margin: 0 auto; /* Ini akan menempatkan gambar di tengah secara horizontal */
  max-width: 200px; /* Pastikan gambar responsif dan tidak melebihi lebar kontainer */
  height: auto; /* Ini akan memastikan bahwa tinggi gambar sesuai dengan lebar yang disesuaikan */
}

</style>
