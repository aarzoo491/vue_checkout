<template>
  <footer class="site-footer">
    <div class="footer-container">

      <!-- Column 1 -->
      <div class="footer-col">
        <h3>AI Company</h3>
        <p>
          We build intelligent digital solutions with the power of modern web
          technologies and Artificial Intelligence.
        </p>
        <div class="social-links">
          <a href="#"><i class="fab fa-facebook"></i></a>
          <a href="#"><i class="fab fa-twitter"></i></a>
          <a href="#"><i class="fab fa-linkedin"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
        </div>
      </div>

      <!-- Column 2 -->
      <div class="footer-col">
        <h4>Quick Links</h4>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/services">Services</router-link></li>
        </ul>
      </div>

      <!-- Column 3 -->
      <div class="footer-col">
        <h4>Services</h4>
        <ul>
          <li>AI Development</li>
          <li>Automation</li>
          <li>UI/UX Design</li>
          <li>Web Applications</li>
        </ul>
      </div>

      <!-- Column 4 -->
      <div class="footer-col">
        <h4>Contact Us</h4>
        <p>Email: hello@aicompany.com</p>
        <p>Phone: +1 234 567 890</p>
        <p>Location: Mumbai, India</p>
      </div>
    </div>

    <div class="footer-bottom">
      <p>© 2026 AI Company. All Rights Reserved.</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
};
</script>

<style scoped>
/* FOOTER */
.site-footer {
  background: #1a1a1a;
  color: #f0f0f0;
  padding: 60px 10%;
}

.footer-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  margin-bottom: 30px;
}

.footer-col h3,
.footer-col h4 {
  margin-bottom: 15px;
  color: #fff;
  font-weight: 600;
}

.footer-col h3 {
  font-size: 18px;
}

.footer-col h4 {
  font-size: 16px;
}

.footer-col p {
  font-size: 14px;
  line-height: 1.6;
  margin-bottom: 10px;
}

.footer-col ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-col ul li {
  margin-bottom: 10px;
}

.footer-col ul a {
  color: #b0b0b0;
  text-decoration: none;
  transition: 0.3s ease;
}

.footer-col ul a:hover {
  color: #0057ff;
}

/* SOCIAL LINKS */
.social-links {
  display: flex;
  gap: 15px;
  margin-top: 15px;
}

.social-links a {
  color: #b0b0b0;
  font-size: 18px;
  transition: 0.3s ease;
  text-decoration: none;
}

.social-links a:hover {
  color: #0057ff;
}

/* FOOTER BOTTOM */
.footer-bottom {
  border-top: 1px solid #333;
  padding-top: 20px;
  text-align: center;
  color: #888;
  font-size: 14px;
}

/* MOBILE RESPONSIVE */
@media (max-width: 768px) {
  .site-footer {
    padding: 40px 5%;
  }

  .footer-container {
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }

  .footer-col h3,
  .footer-col h4 {
    font-size: 14px;
  }
}
</style>
