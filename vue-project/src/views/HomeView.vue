<template>
  <div>
    <CardComponent
      v-for="item in items"
      :key="item"
      :name="item.name"
      :price="item.price"
      v-bind:image="item.image"
    />
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
<style>
:root {
  /*Colors*/
  --light-blue: #3f51b5;
  --dark-blue: #303f9f;
  --purple: #7c4dff;
  --light-amber: #ffc107;
  --dark-amber: #ffa000;
  --orange: #ff5722;
  --gray: #252c30;
  --black: #000;

  /*Typography*/
  --h1: 7.594rem;
  --h2: 5.063rem;
  --h3: 3.375rem;
  --h4: 2.25rem;
  --h5: 1.5rem;

  /*Intentions*/
  --primary: ;
  --secondary: ;
}
html,
body,
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
}
body {
  background-color: var(--secondary);
}
.head {
  border: 1rem solid var(--accent);
  background-color: var(--primary);
}

.main {
  background-color: var(--secondary);
  height: 100vh;
}

h1 {
  font-size: var(--h1);
  text-align: center;
}
h2 {
  font-size: var(--h2);
  text-align: center;
}
.btns {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--secondary);
  flex-wrap: wrap;
}
.btn,
.btn:link,
.btn:visited {
  text-decoration: none;
  padding: 2rem 3rem;
  display: inline-block;
  margin-top: 2rem;
  margin-left: 2rem;
  font-size: 2rem;
  border: none;
  border-radius: 10rem;
  transition: all 0.2s;
}
.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 0.5rem rgba(0, 0, 0, 0.2);
}
#list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
.item {
  margin-top: 2rem;
  margin-left: 2rem;
  margin-right: 2rem;
  padding: 2rem;
  background-color: var(--primary);
  border: 0.5rem solid var(--accent);
  border-radius: 3rem;
}
#img {
  width: 25rem;
  height: 20rem;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 1rem;
  border: 0.5rem solid var(--accent);
  border-radius: 3rem;
}
h3 {
  font-size: var(--h3);
  text-align: center;
}
#price {
  font-size: var(--h4);
  text-align: center;
  margin-top: 1rem;
}
#purchaseBtn {
  text-decoration: none;
  padding: 2rem 3rem;
  display: block;
  font-size: 2rem;
  border: none;
  border-radius: 10rem;
  transition: all 0.2s;
  text-align: center;
  margin-top: 1rem;
  margin-left: auto;
  margin-right: auto;
}
#purchaseBtn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 0.5rem rgba(0, 0, 0, 0.2);
}
#description {
  font-size: var(--h4);
  text-align: center;
}
</style>
