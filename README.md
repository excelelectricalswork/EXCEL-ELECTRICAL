<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Excel Electricals - Choondy, Aluva</title>
  <style>
    body { margin:0; font-family: 'Segoe UI', Arial, sans-serif; background:#f4f4f4; }
    header { background:linear-gradient(90deg,#ff6600,#ffcc00); color:#fff; padding:50px; text-align:center; }
    header h1 { margin:0; font-size:3em; }
    nav { background:#222; display:flex; justify-content:center; flex-wrap:wrap; }
    nav a { color:#fff; padding:15px 20px; text-decoration:none; transition:0.3s; }
    nav a:hover { background:#ff6600; }
    section { padding:60px 20px; text-align:center; }
    h2 { color:#333; margin-bottom:20px; }
    .services { display:flex; flex-wrap:wrap; justify-content:center; gap:20px; }
    .card { background:#fff; border-radius:8px; box-shadow:0 4px 8px rgba(0,0,0,0.1); width:250px; padding:20px; transition:0.3s; }
    .card:hover { transform:scale(1.05); background:#fffbf0; }
    .gallery { display:flex; flex-wrap:wrap; justify-content:center; gap:15px; }
    .gallery img { width:250px; height:180px; object-fit:cover; border-radius:8px; box-shadow:0 3px 6px rgba(0,0,0,0.2); transition:0.3s; }
    .gallery img:hover { transform:scale(1.05); }
    footer { background:#222; color:#fff; text-align:center; padding:20px; }
    .btn { display:inline-block; margin:10px; padding:12px 20px; background:#ff6600; color:#fff; border-radius:5px; text-decoration:none; transition:0.3s; }
    .btn:hover { background:#e65c00; }
    form { max-width:500px; margin:auto; text-align:left; }
    input, textarea { width:100%; padding:10px; margin:10px 0; border:1px solid #ccc; border-radius:5px; }
    button { background:#ff6600; color:#fff; padding:12px 20px; border:none; border-radius:5px; cursor:pointer; }
    button:hover { background:#e65c00; }
  </style>
</head>
<body>
  <header>
    <h1>Excel Electricals</h1>
    <p>Motor Winding • Repairing • Servicing • Varnishing</p>
  </header>

  <nav>
    <a href="#services">Services</a>
    <a href="#gallery">Gallery</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="services">
    <h2>Our Services</h2>
    <div class="services">
      <div class="card"><h3>Motor Winding</h3><p>Expert rewinding for all types of motors.</p></div>
      <div class="card"><h3>Repairing</h3><p>Reliable electrical repairs with quick turnaround.</p></div>
      <div class="card"><h3>Servicing</h3><p>Regular maintenance to extend motor life.</p></div>
      <div class="card"><h3>Varnishing</h3><p>High-quality varnishing for durability.</p></div>
    </div>
  </section>

  <section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery">
      <img src="https://source.unsplash.com/250x180/?electric-motor" alt="Motor Image 1">
      <img src="https://source.unsplash.com/250x180/?machine" alt="Motor Image 2">
      <img src="https://source.unsplash.com/250x180/?engineering" alt="Motor Image 3">
      <img src="https://source.unsplash.com/250x180/?electric" alt="Motor Image 4">
    </div>
  </section>

  <section id="about">
    <h2>About Us</h2>
    <p>Located in Choondy, Aluva, Excel Electricals is your trusted partner for motor winding, repairing, and servicing. We combine experience with modern techniques to deliver reliable solutions.</p>
    <a class="btn" href="https://excelelectricals.co.in" target="_blank">Visit Our Website</a>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <p>📞 Phone: <a href="tel:+918590259451">+91 8590259451</a></p>
    <p>📧 Email: <a href="mailto:excelelectricalswork@gamil.com">excelelectricalswork@gamil.com</a></p>
    <p>💬 WhatsApp: <a href="https://wa.me/918590259451" target="_blank">Chat on WhatsApp</a></p>

    <form id="contactForm">
      <label for="name">Your Name</label>
      <input type="text" id="name" name="name" required>
      <label for="email">Your Email</label>
      <input type="email" id="email" name="email" required>
      <label for="message">Message</label>
      <textarea id="message" name="message" rows="5" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2026 Excel Electricals | Choondy, Aluva</p>
  </footer>

  <script>
    // Simple contact form handler (demo only)
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      alert('Thank you for contacting Excel Electricals! We will get back to you soon.');
      this.reset();
    });
  </script>
</body>
</html>
