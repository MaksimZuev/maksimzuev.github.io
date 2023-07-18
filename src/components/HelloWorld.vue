<script>
export default {
  data() {
    return {
      data: [
        { name: 'foo1', value: 'bar1' },
        { name: 'foo2', value: 'bar2' },
        { name: 'foo3', value: 'bar3' },
        { name: 'foo4', value: 'bar4' },
        { name: 'foo5', value: 'bar5' },
        { name: 'foo6', value: 'bar6' },
        { name: 'foo7', value: 'bar7' },
        { name: 'foo8', value: 'bar8' },
        { name: 'foo9', value: 'bar9' },
        { name: 'foo10', value: 'bar10' },
        { name: 'foo11', value: 'bar11' },
        { name: 'foo12', value: 'bar12' },
        { name: 'foo13', value: 'bar13' },
        { name: 'foo14', value: 'bar14' },
        { name: 'foo15', value: 'bar15' },
        { name: 'foo16', value: 'bar16' },
        { name: 'foo17', value: 'bar17' },
        { name: 'foo18', value: 'bar18' },
        { name: 'foo19', value: 'bar19' },
        { name: 'foo20', value: 'bar20' },
      ],
      selectedItem: null,
    };
  },
  methods: {
    selectItem(index) {
      this.selectedItem = index;
    },
    saveChanges() {
      this.selectedItem = null;
    },
  },
};
</script>

<template>
  <div class="wrapper">
    <ul>
      <li v-for="(item, index) in data" :key="index">
        <span>{{ item.name }}:</span>
        <input type="text" v-model="item.value" @click="selectItem(index)" />
      </li>
    </ul>

    <form v-if="selectedItem !== null">
      <h3>Редактирование элемента {{ selectedItem + 1 }}</h3>
      <input type="text" v-model="data[selectedItem].value" />
      <button @click="saveChanges">Сохранить</button>
    </form>
  </div>
</template>

<style scoped>
.wrapper {
  width: 900px;
  height: auto;
  border-radius: 50px;
  padding: 20px;
  background: black;
  text-align: center;
  color: #fff;
}
.wrapper h3 {
  margin-top: 50px;
}

.wrapper input {
  background: transparent;
  border: 0;
  border-bottom: 2px solid #110813;
  color: #fcfcfc;
  font-size: 14px;
  padding: 5px 8px;
  outline: none;
}
.wrapper input:hover {
  border: 2px solid #6e2d7d;
  border-radius: 10px;
}

.wrapper input:focus {
  border-bottom-color: #6e2d7d;
}
.wrapper button {
  background: #e3bc4d;
  color: #fff;
  border-radius: 10px;
  border: 2px solid #b99935;
  padding: 10px 15px;
  margin-left: 20px;
  cursor: pointer;
  transition: transform 500ms ease;
}
.wrapper button:hover {
  transform: scale(1.1) translateY(-1px);
}
ul {
  list-style-type: none;
}
</style>
