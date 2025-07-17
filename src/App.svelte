<script>
  let name = "Nidhi Kunta"; // Change this to your name
  //let favoriteNumber = 7; // Change this to your favorite number
  let bio = "I love combining design with technology!";
  let school = "University of Texas at Dallas";
  let hobbies = ["Digital Design", "Banner Painting", "Photography", "Content Creation", "Coding", "Reading", "Hand-lettering", "Traveling", "Eating"]; // List some hobbies
  

    import NavBar from "./lib/NavBar.svelte";

    import ImageCard from "./lib/ImageCard.svelte";

    import matchaImage from './assets/matcha.png';

    import bannerImage from './assets/banner.png';

    import buildingImage from './assets/building.png';

    import meImage from './assets/me.png';


  const img0 = {
    image: matchaImage, // pass the imported image
    title: 'Matcha Latte',
    description: 'Green and aesthetic.'
  };

  const img1 = {
    image: bannerImage,
    title: 'Banner Image',
    description: 'Creative and colorful'
  };

  const img2 = {
    image: buildingImage,
    title: 'Building Image',
    description: 'High-tech and luxury'
  };

   const img3 = {
    image: meImage,
    title: 'Me',
    description: 'Gorgeous'
  };


  
  
  let cardData = [
    {
      image: matchaImage,
      title: "Trying new cafes",
      description:
        "I love trying new boba and matcha drinks! 🍵 🧋",
    },
    {
      image: bannerImage,
      title: "Banner Painting",
      description: "Painting banners helps me focus my creativity into a fun hobby 🌄🎨" ,
    },
    {
      image: buildingImage,
      title: "Traveling",
      description:
        "I've been to some cool places like Singapore and Dubai! ✈️ 🌎",
    },
  ];
</script>

<style>
    .poppins-regular {
    font-family: "Poppins", sans-serif;
    font-weight: 400;
    font-style: normal;
  }
  .poppins-bold {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    font-style: normal;
  }
  h1 {
    color: #000000;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .card-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #3498db;
    color: white;
    padding: 10px 15px;
    border-radius: 30px;
  }

  .pic-of-me
  {
    border-radius: 50%;
    height: 300px;
    border: 200px rgb(255, 255, 255);

  }

  h2 {
      padding-top: 10px;
      margin-top: 10px;
  }

</style>

<NavBar />

<div class="container">
  <h1>Nidhi Kunta</h1>
  <img class = "pic-of-me" src={meImage} alt="me">
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>I attend the {school}</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <div class="hobbies" id = "hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>




  <h2>Some of My Favorite Things</h2>
  <div class="card-container" id = "favorite">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>

  



