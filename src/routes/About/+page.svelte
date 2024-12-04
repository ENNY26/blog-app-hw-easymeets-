<script>
    import NavBar from "../../Coponents/NavBar.svelte";
  </script>
  
  <main>
    <nav class="pr-11">
      <NavBar />
    </nav>
  
    <div class="flex flex-col sm:flex-row items-center sm:items-start gap-12 pl-11">
      <!-- Left Section: Text -->
      <div class="flex-1">
        <img 
          src="/src/Assets/about.jpg" 
          alt="about img"
          width="500px" 
          class=" object-cover sm:max-w-1xl" 
        />
      </div>
      
  
      <!-- Right Section: Image -->
      <div class="flex-1 max-w-sm ">
        <h1 class="text-7xl font-bold pt-16 text-[#1e40d7]">This Is Us</h1>
        <p class="text-2l max-w-[12] text-gray-600 leading-relaxed pt-6">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores tempora voluptas, 
          deserunt dolorum velit dolore, corrupti perferendis aliquid eveniet fugit ex nam cum 
          dolor tenetur odit laboriosam ratione consequatur distinctio.
          dolor tenetur odit laboriosam ratione consequatur distinctio.
          dolor tenetur odit laboriosam ratione consequatur distinctio.
        </p>
      </div>
    </div>
  </main>
  
  <style>
    main {
      padding: 2rem;
    }
  
    img {
      max-width: 100%;
      height: auto;
    }
  </style>
  