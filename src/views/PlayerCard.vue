<template>
  <div class="player-card">
    <img :src="image" alt="Player" class="player-image"/>
    <div class="player-details">
      <h3>{{ name }}</h3>
      <p><strong>生日：</strong>{{ birthday }}</p>
      <p><strong>身高：</strong>{{ height }} cm</p>
      <p><strong>體重：</strong>{{ weight }} kg</p>
      <p><strong>籃球特長：</strong>{{ skill }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PlayerCard',
  props: {
    image: String,
    name: String,
    birthday: String,
    height: Number,
    weight: Number,
    skill: String
  }
}
</script>

<style scoped>
.player-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid #ccc;
  padding: 20px;
  margin: 10px;
  width: 200px;
}

.player-image {
  width: 100%;
  height: auto;
  border-radius: 50%;
  margin-bottom: 10px;
}

.player-details {
  text-align: center;
}

.player-details h3 {
  font-size: 1.2rem;
  margin: 10px 0;
}

.player-details p {
  margin: 5px 0;
}
</style>
