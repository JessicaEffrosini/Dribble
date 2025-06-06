# Project Responsive Web Design using Bootstrap
## Date:24.05.25

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Makeup Tools Platform</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      background-color: #debfd4;
      font-family: Arial, sans-serif;
    }
    .tool-card {
      border: 1px solid #dee2e6;
      border-radius: 8px;
      overflow: hidden;
      background: #fff;
      transition: transform 0.3s ease;
    }
    .tool-card:hover {
      transform: scale(1.03);
    }
    .tool-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .tool-info {
      padding: 15px;
    }
    .search-bar {
      max-width: 400px;
      margin: 0 auto;
    }
  </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-light bg-light px-4">
  <img src="logo2.avif" alt="Logo" height="40">
  <div>
    <button class="btn btn-outline-dark me-2" data-bs-toggle="modal" data-bs-target="#loginModal">Login</button>
    <button class="btn btn-dark" data-bs-toggle="modal" data-bs-target="#signupModal">Sign Up</button>
  </div>
</nav>

<!-- Header -->
<div class="text-center my-4">
  <h1>Discover Essential Makeup Tools</h1>
  <p class="text-muted">Everything you need for flawless beauty routines.</p>
  <div class="search-bar input-group mb-3">
    <input type="text" class="form-control" placeholder="Search makeup tools..." />
    <button class="btn btn-outline-secondary">Search</button>
  </div>
</div>

<!-- Tools Section -->
<div class="container">
  <h4 class="mb-3">Popular Makeup Tools</h4>
  <div class="row g-4">
    <!-- Tool 1 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="brush.webp" alt="Foundation Brush">
        <div class="tool-info">
          <h6>Foundation Brush</h6>
          <p class="text-muted small">Apply liquid foundation evenly for a flawless base.</p>
        </div>
      </div>
    </div>
    <!-- Tool 2 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="blenderto.jpeg" alt="Beauty Blender">
        <div class="tool-info">
          <h6>Beauty Blender</h6>
          <p class="text-muted small">Blend foundation and concealer for a smooth finish.</p>
        </div>
      </div>
    </div>
    <!-- Tool 3 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="eyebrush.jpg" alt="Eyeshadow Brush">
        <div class="tool-info">
          <h6>Eyeshadow Brush</h6>
          <p class="text-muted small">Pack and blend eyeshadow like a pro.</p>
        </div>
      </div>
    </div>
    <!-- Tool 4 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="EyelashCurler.webp" alt="Eyelash Curler">
        <div class="tool-info">
          <h6>Eyelash Curler</h6>
          <p class="text-muted small">Lift and curl your lashes for a wide-eyed look.</p>
        </div>
      </div>
    </div>
    <!-- Tool 5 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="eyebrowkit.avif" alt="Eyebrow Kit">
        <div class="tool-info">
          <h6>Eyebrow Kit</h6>
          <p class="text-muted small">Shape and define your brows effortlessly.</p>
        </div>
      </div>
    </div>
    <!-- Tool 6 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="lipbrush.jpg" alt="Lip Brush">
        <div class="tool-info">
          <h6>Lip Brush</h6>
          <p class="text-muted small">Achieve precise lipstick application every time.</p>
        </div>
      </div>
    </div>
    <!-- Tool 7 -->
    <div class="col-md-4">
      <div class="tool-card">
        <img src="contourkit.jpeg" alt="Contour Kit">
        <div class="tool-info">
          <h6>Contour Kit</h6>
          <p class="text-muted small">Define your features with sculpting powders.</p>
        </div>
      </div>
    </div>
     <!-- Tool 8 -->
  <div class="col-md-4">
    <div class="tool-card">
      <img src="highlighter.webp" alt="Highlighter Stick">
      <div class="tool-info">
        <h6>Highlighter Stick</h6>
        <p class="text-muted small">Add a natural glow to your cheekbones and brow bones.</p>
      </div>
    </div>
  </div>
  <!-- Tool 9 -->
  <div class="col-md-4">
    <div class="tool-card">
      <img src="organiser.webp" alt="Makeup Organizer">
      <div class="tool-info">
        <h6>Makeup Organizer</h6>
        <p class="text-muted small">Keep your tools and cosmetics neatly arranged.</p>
      </div>
    </div>
  </div>
  </div>
</div>

<!-- Login Modal -->
<div class="modal fade" id="loginModal" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content p-4">
      <div class="modal-header">
        <h5 class="modal-title">Login</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>
      <div class="modal-body">
        <form>
          <div class="mb-3">
            <label for="loginUserID" class="form-label">User ID</label>
            <input type="text" class="form-control" id="loginUserID" placeholder="Enter your user ID" />
          </div>
          <div class="mb-3">
            <label for="loginPassword" class="form-label">Password</label>
            <input type="password" class="form-control" id="loginPassword" placeholder="Enter your password" />
          </div>
          <button type="submit" class="btn btn-dark w-100">Login</button>
        </form>
      </div>
    </div>
  </div>
</div>

<!-- Sign Up Modal -->
<div class="modal fade" id="signupModal" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content p-4">
      <div class="modal-header">
        <h5 class="modal-title">Sign Up</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>
      <div class="modal-body">
        <form>
          <div class="mb-3">
            <label for="fullName" class="form-label">Full Name</label>
            <input type="text" class="form-control" id="fullName" placeholder="Enter your full name" />
          </div>
          <div class="mb-3">
            <label for="address" class="form-label">Address</label>
            <input type="text" class="form-control" id="address" placeholder="Enter your address" />
          </div>
          <div class="mb-3">
            <label for="dob" class="form-label">Date of Birth</label>
            <input type="date" class="form-control" id="dob" />
          </div>
          <div class="mb-3">
            <label for="signupUserID" class="form-label">User ID</label>
            <input type="text" class="form-control" id="signupUserID" placeholder="Create a user ID" />
          </div>
          <div class="mb-3">
            <label for="signupPassword" class="form-label">Password</label>
            <input type="password" class="form-control" id="signupPassword" placeholder="Create a password" />
          </div>
          <button type="submit" class="btn btn-dark w-100">Sign Up</button>
        </form>
      </div>
    </div>
  </div>
</div>

<!-- Footer -->
<footer style="background-color:#3a3a3a; color: rgb(240, 240, 240); text-align: center; padding: 30px 10px; margin-top: 40px;">
  <p style="margin: 5px;">Email: beautysupport@gmail.com</p>
  <p style="margin: 5px;">Contact: +91 9876543210</p>
  <p style="margin: 5px;">Address: No. 25, Glamour Lane, Beauty City, India - 600045</p>
  <p style="margin: 5px;">Developed by L Jessica Effrosini </p>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

```


## OUTPUT:
![alt text](<Screenshot 2025-05-24 151723.png>)
![alt text](<Screenshot 2025-05-24 151805.png>)
![alt text](<Screenshot 2025-05-24 151820.png>)
![alt text](<Screenshot 2025-05-24 151850.png>)
## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
