# online-book-store-website-code
Create a website for online book stores with Home, Login, Catalogue, Registration page with 
links to all these pages in a menu on top of every page. Embed heading, paragraph, images, video, 
.iframe, form controls, table, and list in this website. Use both Internal and external CSS in this. 
CODE
Index.html

<!DOCTYPE html>
<html lang="en">
<head>

    <title>Online Bookstore</title>
    <link rel="stylesheet" href="css/style.css">
    <style>
        .home, .login, .catalogue, .registration {
            display: none;
        }
    </style>
    <script>
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => {
                page.style.display = 'none';
            });
            document.getElementById(pageId).style.display = 'block';
        }
        window.onload = function() {
            showPage('home');
        }
    </script>
</head>
<body>
    <header>
        <h1>Online Bookstore</h1>
    </header>
    <nav>
        <a href="#" onclick="showPage('home')">Home</a>
        <a href="#" onclick="showPage('login')">Login</a>
        <a href="#" onclick="showPage('catalogue')">Catalogue</a>
        <a href="#" onclick="showPage('registration')">Registration</a>
    </nav>
    <div class="container">
        <!-- Home Page -->
        <div id="home" class="page home">
            <h2>Welcome to Our Online Bookstore</h2>
            <p>Explore a wide variety of books across different genres. Our collection is constantly updated with the latest and greatest in literature.</p>
            <img src="boonimage.jpg" alt="Bookstore Image">
            
        </div>

        <!-- Login Page -->
        <div id="login" class="page login">
            <h2>Login</h2>
            <form>
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required>
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
                <button type="submit">Login</button>
            </form>
        </div>

        <!-- Catalogue Page -->
        <div id="catalogue" class="page catalogue">
            <h2>Book Catalogue</h2>
            <ul>
                <li><strong>Title:</strong> The Great Gatsby | <strong>Author:</strong> F. Scott Fitzgerald | <strong>Price:</strong> $10.99</li>
                <li><strong>Title:</strong> 1984 | <strong>Author:</strong> George Orwell | <strong>Price:</strong> $8.99</li>
                <li><strong>Title:</strong> To Kill a Mockingbird | <strong>Author:</strong> Harper Lee | <strong>Price:</strong> $12.99</li>
            </ul>
        </div>

        <!-- Registration Page -->
        <div id="registration" class="page registration">
            <h2>Registration</h2>
            <form>
                <label for="full-name">Full Name:</label>
                <input type="text" id="full-name" name="full-name" required>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
                <label for="course">Course:</label>
                <select id="course" name="course">
                    <option value="bsc">B.Sc</option>
                    <option value="bcom">B.Com</option>
                    <option value="ba">B.A</option>
                    <option value="mca">MCA</option>
                    <option value="mba">MBA</option>
                </select>
                <button type="submit">Register</button>
            </form>
        </div>
    </div>

    
</body>
</html>


Style.css


body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav {
    text-align: center;
    background-color: #444;
    padding: 10px 0;
}

nav a {
    color: #fff;
    margin: 0 15px;
    text-decoration: none;
    font-weight: bold;
}

.container {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    text-align: center;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 20px;
}

table, th, td {
    border: 1px solid #ddd;
    padding: 8px;
}

th {
    background-color: #f2f2f2;
    text-align: left;
}

form input, form select, form textarea {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
}

form button {
    padding: 10px 15px;
    background-color: #007bff;
    border: none;
    border-radius: 5px;
    color: #fff;
    cursor: pointer;
}

form button:hover {
    opacity: 0.9;
}

iframe {
    width: 100%;
    height: 200px;
    border: none;
}
