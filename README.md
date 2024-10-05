# INTERNNOVATEL1
#html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Blog</title>
    <!-- Bootstrap CSS for responsiveness -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="internL1.css">
</head>
<body>
    <!-- Header -->
    <header class="text-center py-4 bg-dark text-light">
        <h1>My Personal Blog</h1>
        <p>A simple blog about coding, technology, and more!</p>
    </header>

    <!-- Main Content -->
    <main class="container my-5">
        <section class="row" id="blog-posts">
            <!-- Blog posts will be dynamically loaded here -->
        </section>
    </main>

    <!-- Footer -->
    <footer class="text-center py-4 bg-dark text-light">
        <p>&copy; 2024 My Personal Blog | Designed by Ramavath Indhu</p>
    </footer>

    <!-- Bootstrap JS and custom JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <script src="script.js"></script>
</body>
</html>
#css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f9f9f9;
}

/* Header styling */
header {
    background-color: #343a40;
    color: white;
    padding: 20px 0;
    text-align: center;
}

header h1 {
    font-size: 2.5rem;
    margin-bottom: 10px;
}

header p {
    font-size: 1.2rem;
}

/* Main section styling */
main {
    margin-top: 20px;
}

/* Blog post card styling */
.card {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease-in-out;
}
#java script
const blogPosts = [
    {
        title: "My First Blog Post",
        image: "https://via.placeholder.com/600x300",
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        link: "#"
    },
    {
        title: "Learning JavaScript",
        image: "https://via.placeholder.com/600x300",
        text: "JavaScript is essential for creating interactive websites. Learn how I started my journey into JavaScript.",
        link: "#"
    },
    {
        title: "Exploring CSS",
        image: "https://via.placeholder.com/600x300",
        text: "CSS is the language that styles the web. Here’s how I learned to use it effectively.",
        link: "#"
    },
    {
        title: "Understanding HTML",
        image: "https://via.placeholder.com/600x300",
        text: "HTML is the backbone of web content. Let’s dive into its structure and usage.",
        link: "#"
    }
];

// Function to load blog posts dynamically
function loadBlogPosts() {
    const blogSection = document.getElementById('blog-posts');
    
    blogPosts.forEach(post => {
        const article = document.createElement('article');
        article.classList.add('col-md-6', 'mb-4');

        article.innerHTML = `
            <div class="card">
                <img src="${post.image}" class="card-img-top" alt="${post.title}">
                <div class="card-body">
                    <h2 class="card-title">${post.title}</h2>
                    <p class="card-text">${post.text}</p>
                    <a href="${post.link}" class="btn btn-primary">Read More</a>
                </div>
            </div>
        `;

        blogSection.appendChild(article);
    });
}

// Load blog posts when the page is ready
document.addEventListener('DOMContentLoaded', loadBlogPosts);


