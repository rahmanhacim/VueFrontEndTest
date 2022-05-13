<script>
export default {
  // state
  data() {
    return {
      boxItems: [
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
        {
          shortDesc:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
          longDesc:
            "  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur maximus quam",
        },
      ],
      activeBox: null,
      title: "Experienced & Multi-Talented",
    };
  },
  // actions
  methods: {
    increment() {
      this.count++;
    },
  },
};
</script>
<template>
  <div>
    <h1 class="title">{{ title }}</h1>
    <div class="devider" />
    <h3 class="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi consectetur
      maximus quam Morbi consectetur maximus quamMorbi consectetur maximus
      quamMorbi consectetur maximus quamMorbi consectetur maximus quam
    </h3>
    <div class="gridBox">
      <div class="wrapperBox" v-for="(item, index) in boxItems" :key="index">
        <div class="boxHeader">
          <img src="../assets/infowhite.png" class="imgCenter" />
        </div>
        <div
          class="boxDescription"
          v-bind:class="{ sizeBoxDescription: activeBox === index }"
        >
          <div class="descriptionHeader">Block</div>
          <div class="descriptionDetails">
            <div v-if="activeBox === index">
              <div>{{ item.longDesc }}</div>
              <button @click="activeBox = null" class="button">-</button>
            </div>
            <div v-else>
              <div>{{ item.shortDesc }}</div>
              <button @click="activeBox = index" class="button">+</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://cdn.jsdelivr.net/npm/vuesax/dist/vuesax.css");
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.gridBox {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  padding: 0 2rem;
  column-gap: 20px;
  row-gap: 20px;
}

@media screen and (max-width: 768px) {
  .gridBox {
    grid-template-columns: repeat(1, 1fr);
  }
}

.boxDescription {
  background-color: rgb(0, 0, 0);
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.sizeBoxDescription {
  width: 100%;
  height: 100%;
}

.descriptionHeader {
  color: white;
  text-align: center;
  font-family: "gotham-bold";
}
.button {
  background-color: #000000; /* Green */
  border: 2px;
  color: white;
  padding: 20px;
  text-align: center;
  border-color: white;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  border-radius: 50%;
}
.boxHeader {
  background-color: rgb(114, 146, 120);
  border: 10px;
  width: 100%;
  height: 50px;
  text-align: center;
  justify-content: center;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
.devider {
  background-color: rgb(177, 177, 177);
  border: 1px;
  width: 35px;
  height: 5px;
  margin: 0 auto;
  margin-bottom: 20px;
}
.wrapperBox {
  display: flex;
  flex-direction: column;
}
.descriptionDetails {
  overflow: hidden;
  display: flex;
  flex-direction: row;
}
.grayscale {
  filter: grayscale(100%);
}
.imgCenter {
  margin: 0 auto;
  margin-top: 5px;
  z-index: auto;
  width: 15%;
}
</style>
