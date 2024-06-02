---
layout: base
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Tech Blog</title>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            padding-top: 56px;
        }
        .navbar-brand {
            font-weight: bold;
        }
        .profile-pic {
            border-radius: 50%;
            width: 150px;
            height: 150px;
        }
        .section-title {
            margin-top: 40px;
        }
        .card-img-top {
            height: 200px;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <a class="navbar-brand" href="#">My Tech Blog</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a class="nav-link" href="#about">About Me</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#projects">Projects</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#blog">Blog Posts</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#videos">Videos</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contact">Contact</a>
                </li>
            </ul>
        </div>
    </nav>

    <div class="container">
        <section id="about" class="text-center">
            <img src="https://github.com/username.png" class="profile-pic mt-4" alt="Profile Picture">
            <h1 class="mt-3">Welcome to My Tech Blog</h1>
            <p>Hi, I'm [Your Name], a passionate full-stack developer and machine learning enthusiast. I love solving real-world problems through technology and enjoy collaborating with teams to build innovative solutions.</p>
        </section>

        <section id="projects">
            <h2 class="section-title text-center">Featured Projects</h2>
            <div class="card-deck">
                <div class="card">
                    <img class="card-img-top" src="path/to/ai-project-image.jpg" alt="AI Project">
                    <div class="card-body">
                        <h5 class="card-title"><a href="https://github.com/username/ai-recommendation-system">AI-Driven Recommendation System</a></h5>
                        <p class="card-text">An AI-driven recommendation system that increased user engagement by 30%.</p>
                        <p><strong>Technologies:</strong> Python, TensorFlow, Scikit-Learn, Flask.</p>
                        <p><strong>Outcome:</strong> Enhanced user experience and engagement.</p>
                    </div>
                </div>
                <div class="card">
                    <img class="card-img-top" src="path/to/collaboration-app-image.jpg" alt="Collaboration App">
                    <div class="card-body">
                        <h5 class="card-title"><a href="https://github.com/username/collaboration-app">Real-Time Collaboration Web Application</a></h5>
                        <p class="card-text">A full-stack web application for managing team projects with real-time collaboration features.</p>
                        <p><strong>Technologies:</strong> React, Node.js, MongoDB, Socket.IO.</p>
                        <p><strong>Outcome:</strong> Improved team productivity by 25%.</p>
                    </div>
                </div>
                <div class="card">
                    <img class="card-img-top" src="path/to/data-visualization-image.jpg" alt="Data Visualization">
                    <div class="card-body">
                        <h5 class="card-title"><a href="https://github.com/username/data-visualization-dashboard">Data Visualization Dashboard</a></h5>
                        <p class="card-text">A data visualization tool that helps in making data-driven decisions.</p>
                        <p><strong>Technologies:</strong> D3.js, Python, Django.</p>
                        <p><strong>Outcome:</strong> Enabled better decision-making, increasing sales by 15%.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="blog" class="mt-5">
            <h2 class="section-title text-center">Recent Blog Posts</h2>
            <ul class="list-group list-group-flush">
                <li class="list-group-item"><a href="https://username.github.io/blog/ai-recommendation-system">Building an AI-Driven Recommendation System</a></li>
                <li class="list-group-item"><a href="https://username.github.io/blog/collaboration-web-app">Improving Team Collaboration with Real-Time Web Apps</a></li>
                <li class="list-group-item"><a href="https://username.github.io/blog/data-visualizations">Creating Interactive Data Visualizations</a></li>
            </ul>
        </section>

        <section id="videos" class="mt-5">
            <h2 class="section-title text-center">Videos</h2>
            <div class="row">
                <div class="col-md-4">
                    <div class="embed-responsive embed-responsive-16by9">
                        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/your_video_id" allowfullscreen></iframe>
                    </div>
                    <p class="text-center mt-2">Introduction Video</p>
                </div>
                <div class="col-md-4">
                    <div class="embed-responsive embed-responsive-16by9">
                        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/your_video_id" allowfullscreen></iframe>
                    </div>
                    <p class="text-center mt-2">AI-Driven Recommendation System</p>
                </div>
                <div class="col-md-4">
                    <div class="embed-responsive embed-responsive-16by9">
                        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/your_video_id" allowfullscreen></iframe>
                    </div>
                    <p class="text-center mt-2">Real-Time Collaboration Web Application</p>
                </div>
            </div>
        </section>

        <section id="contact" class="text-center mt-5">
            <h2 class="section-title">Contact Me</h2>
            <p>Feel free to reach out via <a href="mailto:email@example.com">email@example.com</a> or connect with me on <a href="https://www.linkedin.com/in/yourprofile">LinkedIn</a>.</p>
        </section>
    </div>

    <footer class="bg-dark text-white text-center py-3">
        © 2024 [Your Name]. All rights reserved.
    </footer>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
