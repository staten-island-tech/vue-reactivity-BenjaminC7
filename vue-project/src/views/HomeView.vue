<template>
  <div>
    <li v-for="item in items" :key="item">{{ item.name }}</li>
  </div>
</template>

<script>
import CardComponent from "../components/CardComponent.vue";
export default {
  name: "Home",
  components: {
    CardComponent,
  },
  data() {
    return {
      items: [
        {
          name: "Red Dragon",
          image: "/RedDragon.jpg",
          price: 499.99,
          categories: ["dragon", "fire"],
        },
        {
          name: "Beholder",
          image: "/Beholder.jpg",
          price: 299.99,
          categories: ["aberration", "psychic"],
        },
        {
          name: "Pikachu",
          image: "/Pikachu.png",
          price: 24.99,
          categories: ["beast", "electric", "pokemon"],
        },
        {
          name: "Skeleton",
          image: "/Skeleton.webp",
          price: 9.99,
          categories: ["undead"],
        },
        {
          name: "Ghoul",
          image: "/Ghoul.png",
          price: 14.99,
          categories: ["undead"],
        },
        {
          name: "Mammott",
          image: "/Mammott.webp",
          price: 29.99,
          categories: ["singing", "ice", "beast"],
        },
        {
          name: "Maw",
          image: "/Maw.webp",
          price: 49.99,
          categories: ["singing", "ice", "water", "beast"],
        },
        {
          name: "Mimikyu",
          image: "/Mimikyu.png",
          price: 69.99,
          categories: ["ghost", "fairy", "pokemon"],
        },
        {
          name: "Oaktopus",
          image: "/Oaktopus.webp",
          price: 49.99,
          categories: ["singing", "grass", "water"],
        },
        {
          name: "Gelatinous Cube",
          image: "/Gelatinous_Cube.webp",
          price: 4.99,
          categories: ["ooze"],
        },
        {
          name: "Cleric Beast",
          image: "/Cleric_Beast.png",
          price: 199.99,
          categories: ["beast"],
        },
        {
          name: "Garchomp",
          image: "/Garchomp.png",
          price: 99.99,
          categories: ["dragon", "ground", "pokemon"],
        },
        {
          name: "Mafia Snowman",
          image: "/Mafia_Snowman.png",
          price: 7.99,
          categories: ["ice"],
        },
        {
          name: "White Dragon",
          image: "/White_Dragon.webp",
          price: 499.99,
          categories: ["ice", "dragon"],
        },
        {
          name: "Amygdala",
          image: "/Amygdala.png",
          price: 699.99,
          categories: ["aberration"],
        },
        {
          name: "Momoo",
          image: "/Momoo.webp",
          price: 89.99,
          categories: ["water", "beast"],
        },
        {
          name: "Swampert",
          image: "Swampert.png",
          price: 99.99,
          categories: ["water", "ground", "pokemon"],
        },
        {
          name: "Mimic",
          image: "Mimic.png",
          price: 49.99,
          categories: ["aberration"],
        },
        {
          name: "Zombie",
          image: "Zombie.webp",
          price: 4.99,
          categories: ["undead"],
        },
      ],
    };
  },
  methods: {
    authState: function () {
      if (this.loggedIn === false) {
        this.loggedIn = true;
      } else {
        this.loggedIn = false;
      }
    },
  },
  computed: {
    now: function () {
      const time = new Date();
      return `${time.getHours()}:${time.getMinutes()}`;
    },
  },
};
</script>
<style scoped>
h1 {
  color: blue;
}
</style>
