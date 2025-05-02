<template>
  <div>
    <h1>戰隊球員</h1>

    <!-- 球員介紹區域 -->
    <div class="players-container">
      <PlayerCard 
        v-for="player in players" 
        :key="player.id" 
        :image="player.image" 
        :name="player.name" 
        :birthday="player.birthday" 
        :height="player.height" 
        :weight="player.weight" 
        :skill="player.skill" 
      />
    </div>
  </div>
</template>

<script>
import PlayerCard from '@/components/PlayerCard.vue';

export default {
  name: 'HappyView',
  components: {
    PlayerCard
  },
  data() {
    return {
      players: [
        {
          id: 1,
          image: '/assets/player1.jpg',  // 如果在 public 資料夾內
          name: '林奎翰',
          birthday: '1995.08.05',
          height: 203,
          weight: 102,
          skill: '得分能力強'
        },
        {
          id: 2,
          image: '/assets/player1.jpg',  // 如果在 public 資料夾內
          name: '林奎翰',
          birthday: '1998.07.19',
          height: 193,
          weight: 95,
          skill: '防守與籃板球'
        },
        {
          id: 3,
          image: '/assets/player1.jpg',  // 如果在 public 資料夾內
          name: '林奎翰',
          birthday: '1998.10.07',
          height: 185,
          weight: 85,
          skill: '突破與助攻'
        }
      ]
    };
  }
}
</script>

<style scoped>
.players-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
