<template>
  <div class="list-icon">
    <h2 class="subtitle">{{list.title}}</h2>
    <ul class="list">
      <li class="item" v-for="(item, index) in list.data" :key="index">
        <div class="item_icon">
          <img class="icon" :src="item.icon">
          <img class="icon shadow" :src="item.icon">
        </div>
        <div class="content">
          <div class="item_title">
            <h3 class="title">{{ item.title || capitalize }}</h3>
          </div>
          <div class="item_text">
            <p class="text">{{ item.text }}</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ListIcon',
  data () {
    return {}
  },
  filters: {
    capitalize: item => {
      return item.toUpperCase()
    }
  },
  props: {
    list: {
      type: Object
    }
  },
  components: {
  },
  mounted () {
  }
}
</script>
<style scoped>
.list {
  margin: auto;
  max-width: 80%;
}
.item {
  align-items: center;
  display: flex;
  text-align: left;
  padding: 60px 40px 60px 60px;
  margin-bottom: 40px;
  border: 2px dotted var(--color-primary);
  border-radius: 30px;
}
.item_icon {
  width: 6vw;
  max-width: 80px;
  margin-right: 40px;
  position: relative;
}
.item_icon .shadow {
  position: absolute;
  top: 3px;
  left: 3px;
  opacity: .3;
  filter: blur(2px);
}
.icon {
  width: 100%;
  height: auto;
}
.item_icon,
.content {
  display: inline-block;
}
.content {
  vertical-align: middle;
  width: 80%;
}
.item_title {
  margin-bottom: 10px;
  color: var(--color-navy);
}
</style>
