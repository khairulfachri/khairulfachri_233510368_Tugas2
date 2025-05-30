<template>
  <div class="container">
    <aside class="sidebar">
      <h2>Khairul Fachri</h2>
      <ul>
        <li v-for="(topic, index) in topics" :key="index" @click="selectedTopic = topic">
          {{ topic }}
        </li>
      </ul>
    </aside>

    <main class="content">
      <p v-if="selectedTopic">{{ selectedTopic }}</p>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedTopic: '',
      topics: [
        "Home",
        "Tentang Saya",
        "Portofolio",
        "Blog",
        "Galeri",
        "Skill",
        "Pendidikan",
        "Kontak"
      ]
    };
  }
};
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
.container {
  display: flex;
  height: 100vh;
}
.sidebar {
  width: 300px;
  border-right: 1px solid #ccc;
  padding: 20px;
}
.sidebar h2 {
  margin-bottom: 20px;
}
.sidebar ul {
  list-style: none;
  padding: 0;
}
.sidebar li {
  margin: 10px 0;
  cursor: pointer;
}
.sidebar li:hover {
  color: rgb(146, 146, 203);
}
.content {
  flex: 1;
  padding: 40px;
}
</style>