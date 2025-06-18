# FILMSTAR-
<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Movie Zone</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-900 text-white">

  <!-- Header -->
  <header class="p-4 bg-gray-800 shadow-md flex justify-between items-center">
    <h1 class="text-2xl font-bold">🎬 My Movie Zone</h1>
    <input
      type="text"
      placeholder="Search movies..."
      id="searchInput"
      class="p-2 rounded bg-gray-700 text-white"
      onkeyup="searchMovies()"
    />
  </header>

  <!-- Movie Grid -->
  <main class="p-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6" id="movieList">
    <!-- Example Movie Card -->
    <div class="bg-gray-800 rounded-xl overflow-hidden shadow-md movie-card">
      <img src="https://i.imgur.com/YOZz9fl.jpg" alt="Movie Poster" class="w-full h-60 object-cover" />
      <div class="p-4">
        <h2 class="text-xl font-semibold movie-title">Pathaan</h2>
        <p class="text-sm text-gray-400">Action | 2023 | ⭐ 4.5</p>
        <iframe class="w-full h-48 mt-2 rounded" src="https://www.youtube.com/embed/vqu4z34wENw" allowfullscreen></iframe>
        <p class="mt-2 text-sm">🔥 Shah Rukh Khan returns in style in this high-octane spy thriller!</p>
        <div class="mt-2">
          <input type="text" placeholder="Leave a comment..." class="p-1 w-full rounded bg-gray-700 text-white" />
        </div>
      </div>
    </div>

    <!-- Add more movie cards as needed -->

  </main>

  <script>
    function searchMovies() {
      const input = document.getElementById("searchInput").value.toLowerCase();
      const cards = document.querySelectorAll(".movie-card");
      cards.forEach((card) => {
        const title = card.querySelector(".movie-title").innerText.toLowerCase();
        card.style.display = title.includes(input) ? "block" : "none";
      });
    }
  </script>

</body>
</html>
