<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section class="grid-container">
            <article class="grid-item">Grid Item 1</article>
            <article class="grid-item">Grid Item 2</article>
            <article class="grid-item">Grid Item 3</article>
        </section>
        <section class="flex-container">
            <article class="flex-item">Flex Item 1</article>
            <article class="flex-item">Flex Item 2</article>
            <article class="flex-item">Flex Item 3</article>
        </section>
    </main>
</body>
</html>


CSS (in styles.css file):

/* Global Styles */

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em;
    text-align: center;
}

nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
}

nav li {
    margin-right: 20px;
}

nav a {
    color: #fff;
    text-decoration: none;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2em;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
    margin-bottom: 40px;
}

.grid-item {
    background-color: #f7f7f7;
    padding: 20px;
}

.flex-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.flex-item {
    background-color: #f7f7f7;
    padding: 20px;
    margin: 10px;
    width: 200px;
}

/* Media Queries */

@media (max-width: 768px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }
    .flex-container {
        flex-direction: column;
        align-items: center;
    }
    .flex-item {
        width: 100%;
        margin: 10px 0;
    }
}

@media (max-width: 480px) {
    .grid-container {
        grid-template-columns: 1fr;
    }
    .flex-container {
        flex-direction: column;
        align-items: center;
    }
    .flex-item {
        width: 100%;
        margin: 10px 0;
    }
    nav ul {
        flex-direction: column;
    }
    nav li {
        margin-right: 0;
    }
}



