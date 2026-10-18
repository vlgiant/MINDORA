# MINDORA
Mindora - Brain Games, IQ Challenges and Free Online Tools
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MINDORA - Discover More</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #07111f;
      color: white;
    }

    header {
      padding: 20px;
      background: #101f35;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      color: #39e6c5;
      font-size: 25px;
      font-weight: bold;
    }

    .hero {
      text-align: center;
      padding: 65px 20px;
      background: linear-gradient(135deg, #102f50, #07111f);
    }

    .hero h1 {
      font-size: 38px;
      margin-bottom: 12px;
    }

    .hero span {
      color: #39e6c5;
    }

    .hero p {
      color: #c8d5e5;
      line-height: 1.7;
    }

    input {
      width: 90%;
      max-width: 420px;
      padding: 15px;
      border-radius: 10px;
      border: none;
      margin-top: 15px;
      font-size: 16px;
    }

    main {
      max-width: 1000px;
      margin: auto;
      padding: 25px 18px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 18px;
    }

    .card {
      background: #13243a;
      padding: 22px;
      border-radius: 15px;
      border: 1px solid #263d57;
    }

    .card h2 {
      color: #39e6c5;
    }

    .card p {
      color: #c8d5e5;
      line-height: 1.6;
    }

    button {
      background: #39e6c5;
      color: #07111f;
      border: none;
      padding: 12px 18px;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
    }

    footer {
      text-align: center;
      padding: 25px;
      color: #aabbd0;
      background: #101f35;
      margin-top: 30px;
    }
  </style>
</head>

<body>
  <header>
    <div class="logo">MINDORA</div>
    <div>Discover the Future 🌍</div>
  </header>

  <section class="hero">
    <h1>Discover a <span>New World</span></h1>
    <p>
      Explore ideas, technology, future predictions,
      and knowledge that can change your life.
    </p>

    <input
      id="search"
      type="text"
      placeholder="Search Mindora..."
      oninput="searchCards()"
    >
  </section>

  <main>
    <h2>Explore Mindora</h2>

    <div class="cards" id="cards">

      <article class="card">
        <h2>🌍 World 2086</h2>
        <p>
          Discover imaginative visions of how cities,
          technology, and everyday life might change by 2086.
        </p>
        <button onclick="showInfo('World 2086', 'Explore creative future scenarios. These are fictional possibilities, not guaranteed predictions.')">
          Explore
        </button>
      </article>

      <article class="card">
        <h2>🤖 Future Technology</h2>
        <p>
          Learn about artificial intelligence, robots,
          inventions, and emerging technologies.
        </p>
        <button onclick="showInfo('Future Technology', 'Technology is changing how people work, communicate, and create.')">
          Explore
        </button>
      </article>

      <article class="card">
        <h2>💡 Smart Ideas</h2>
        <p>
          Discover practical ideas for learning,
          creativity, and solving everyday problems.
        </p>
        <button onclick="showInfo('Smart Ideas', 'Start with one useful idea, test it, and improve it over time.')">
          Explore
        </button>
      </article>

      <article class="card">
        <h2>🚀 Digital Opportunities</h2>
        <p>
          Learn about online skills, digital projects,
          and ways to build useful things on the internet.
        </p>
        <button onclick="showInfo('Digital Opportunities', 'Build valuable skills first. Online income is possible, but never guaranteed.')">
          Explore
        </button>
      </article>

    </div>
  </main>

  <footer>
    <p>© 2026 MINDORA | Imagine More. Discover More.</p>
  </footer>

  <script>
    function showInfo(title, message) {
      alert(title + "\n\n" + message);
    }

    function searchCards() {
      const query = document.getElementById("search")
        .value.toLowerCase();

      const cards = document.querySelectorAll(".card");

      cards.forEach(function(card) {
        const content = card.textContent.toLowerCase();

        card.style.display = content.includes(query)
          ? "block"
          : "none";
      });
    }
  </script>
</body>
</html>
