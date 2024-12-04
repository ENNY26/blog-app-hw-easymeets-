<script>
    import NavBar from "../../Coponents/NavBar.svelte";
  </script>
  
  <main>
    <nav>
      <NavBar />
    </nav>
  <!--Left Section: large Text-->
    <div class="flex flex-wrap md:flex-row justify-center items-center gap-8 ">
      <div class="flex-1 max-w-lg text-center md:text-left">
        <img src="/src/Assets/contactimg.jpg" alt="">
        <p class="text-lg text-gray-600">
            Question or Suggestion ?
        </p>
        <h1 class="text-6xl font-semibold mb-4">Reach Out!</h1>   
      </div>
  
      <!-- Right Section: Contact Form -->
      <form class="flex-1 max-w-lg bg-white shadow-lg p-6 rounded-lg space-y-4">
        <!-- Full Name -->
        <div>
          <label class="block text-gray-700 font-medium mb-1"
           for="name">Full Name</label>
           <input type="text"
           id="name"
           placeholder="Full Name"
           class="w-full border border-gray-300 rounded-lg px-4 py-2"
           />
        </div>
  
        <!-- Email -->
        <div>
          <label for="email" class="block text-gray-700 font-medium mb-1">Email</label>
          <input
            type="email"
            id="email"
            placeholder="Enter your email"
            class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
  
        <!-- Message -->
        <div>
          <label for="message" class="block text-gray-700 font-medium mb-1">Message</label>
          <textarea
            id="message"
            rows="4"
            placeholder="Type your message here"
            class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          ></textarea>
        </div>
  
        <!-- Newsletter Subscription -->
        <div class="flex items-center">
          <input
            type="checkbox"  
            id="newsletter"
            class="w-5 h-5 text-blue-500 focus:ring-blue-500 rounded"
          />

          <label for="newsletter" class="ml-2 text-gray-600">Subscribe to our newsletter</label>
        </div>
  
        <!-- Submit Button -->
        <button
          type="submit"
          class="w-full bg-blue-500 text-white font-bold py-2 rounded-lg hover:bg-blue-600 transition"
        >
          Send
        </button>
      </form>
    </div>
  </main>
  
  <style>
        main {
      padding: 2rem;
    }
  
    form input,
    form textarea {
      outline: none;
    }
  </style>
  