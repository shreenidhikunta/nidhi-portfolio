<script>
  let name = "Nidhi"; // Change this to your name
  //let favoriteNumber = 7; // Change this to your favorite number
  let bio = "Freshman at the University of Texas at Dallas Studying Business Analytics and AI";
  let school = "University of Texas at Dallas";
  let hobbies = ["HTML", "CSS", "JS", "Svelte", "React.js", "Swift", "Figma", "SQL", "Python", "Java", "AWS", "Tableau", "PowerBI", "Pandas", "NumPy", "AI/ML"]; // List some hobbies
  

    import NavBar from "./lib/NavBar.svelte";

    import ImageCard from "./lib/ImageCard.svelte";

    import matchaImage from './assets/matcha.png';

    import bannerImage from './assets/banner.png';

    import buildingImage from './assets/building.png';

    import dataImage from './assets/data.png';

    import meImage from './assets/me.png';

    import shootingStarsImage from './assets/shootingStars.png';

    import infosysImage from './assets/infosys.png';


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

   const img4 = {
    image: dataImage,
    title: 'Data',
    description: 'Project'
    
  };

   const img5 = {
    image: shootingStarsImage,
    title: 'Data',
    description: 'Project'
  };

  const img6 = {
    image: infosysImage,
    title: 'Data',
    description: 'Project'
  };



  
  
  let cardData = [
    {
      image: matchaImage,
      title: "Founder of Tapestries of Tech",
      description:
        "A cutting-edge online community that interweaves ideas of tech, culture, and equity. Post daily insights on Substack, Linkedin, and Instagram. Supported by students from Princeton University, UIUC, and more."

    },
    {
      image: bannerImage,
      title: "Kode With Klossy Instructional Leader",
      description: "Supported 30+ girls and non-binary youth through dedicated mentorship in building AI-powered image classifiers, inspiring middle and high school scholars to enter technology confidently." 
    },
    {
      image: shootingStarsImage,
      title: "Shooting Stars Foundation Director",
      description:
        "Organized numerous beginner-friendly, diversity-focused hackathons for the Shooting Stars Foundation to bring tech to underprivileged youth. Led workshops on pitching your product, app development basics, and web development to increase tech-literacy and skill set amongst middle and high school girls.",
    },
    {
      image: buildingImage,
      title: "Shooting Stars Foundation Director",
      description:
        "Spearheaded Congressional App Challenge Prep Camp, Game Design Camp for children in low-income housing, and an all-girls Finance Academy alongside NVIDIA Sr. Content Developer and the Shooting Stars Foundation.",
    },
     {
      image: dataImage,
      title: "Program Participant",
      description:
        "Worked with Bloomberg Philanthropies's Black Wealth Data Center to build an immersive story/data focused website showcasing the effects of redlining on African American economic success.",
       
      
    },
     {
      image: infosysImage,
      title: "Program Participant",
      description:
        "Currently working with Infosys to build a data science project focused on digital equity.",
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
   
    margin: 0 auto;
    padding: 20px;
    text-align: center;
     
  }
  .card-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  
    
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
  <h1>Hey, I'm Nidhi!</h1>
  <img class = "pic-of-me" src={meImage} alt="me">
  <p>{bio}</p>

  <h2>My Skills</h2>
  <div class="hobbies" id = "hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
</div>




  <h2>My experience</h2>
  <div class="card-container" id = "favorite">
    {#each cardData as { image, title, description, link }}
      <ImageCard {image} {title} {description} {link}/>
    {/each}
  </div>

  



