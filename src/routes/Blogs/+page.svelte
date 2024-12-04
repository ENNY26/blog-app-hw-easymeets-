<script>
import NavBar from "../../Coponents/NavBar.svelte";

  let blogs = [
    {
      image: '/src/Assets/blogimg1.jpg',
      title: "Chicken Curry",
      description: "This is the description of the first blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg2.jpg',
      title: "Catfish Pepper soup",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg3.jpg',
      title: "wakye",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg4.jpg',
      title: "Bunny Chow",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg5.jpg',
      title: "",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg6.jpg',
      title: "Peri Peri Chicken",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg9.webp',
      title: "Japche Noodles",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    },
    {
      image: '/src/Assets/blogimg8.jpg',
      title: "Jollof Rice",
      description: "This is the description of the second blog post.",
      link: "/BlogPage"
    }
  ];
</script>
<nav>
  <NavBar/>
</nav>
<div class="p-8">
  <!-- Page Title -->
  <h1  class="text-3xl mb-6  text-left">The Real <br>  <br><span class="text-[155px] font-semibold mr-0 text-[#1e40d7]">Blog</span>
  </h1>
  <!-- Blog Grid -->
  <div class=" p-8 mx-auto max-w-6xl grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3
  gap-6">
    {#each blogs as blog}
      <div class="bg-white rounded-lg shadow-md overflow-hidden">
        <!-- Blog Image -->
        <img src={blog.image} alt={blog.title} class="w-full h-48 object-cover" />

        <!-- Blog Content -->
        <div class="p-4">
          <h2 class="text-xl font-semibold mb-2">{blog.title}</h2>
          <p class="text-gray-600 mb-4">{blog.description}</p>
          
          <!-- Action Section -->
          <div class="flex justify-between items-center">
            <a href={blog.link} class="bg-blue-500 text-white px-3 py-1 rounded-md
             hover:bg-blue-600">Read More</a>
            <div class="flex space-x-4 text-gray-600">
              <span class="cursor-pointer "><img src="/src/Assets/save.svg" alt="save icon" width="26px"></span>
              <span class="cursor-pointer"><img src="/src/Assets/love.svg" alt="love icon" width="26px"></span>
              <span class="cursor-pointer"><img src="/src/Assets/share.svg" alt="share icon" width="26px"></span>
            </div>
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
  /* Basic Styling */
  .grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  }
  .h-48 {
    height: 12rem; /* Ensure a consistent height for images */
  }
</style>
