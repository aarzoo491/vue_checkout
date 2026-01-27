<template>
  <div class="about">
    <!-- HERO SECTION -->
    <section class="about-hero">
      <div class="hero-text">
        <h1>About Our Company</h1>
        <p>
          We are a forward-thinking technology company specializing in Artificial
          Intelligence, cloud platforms, and modern application development. Our mission
          is to empower organizations with digital solutions that create meaningful,
          measurable impact.
        </p>
        <button class="btn-primary">Get Started</button>
      </div>

      <img
        src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=400&fit=crop"
        alt="About banner"
        class="hero-image"
      />
    </section>

    <!-- OUR STORY -->
    <section class="our-story">
      <h2>Our Story</h2>
      <p>
        Founded in 2018, our company began with a simple idea — to help businesses
        harness the power of modern technology. Over the years, we have evolved into a
        full-scale digital innovation partner, delivering AI-powered solutions,
        enterprise applications, automation workflows, and user-centered experiences.
      </p>
      <p>
        Today, we work with clients across industries including eCommerce, healthcare,
        fintech, logistics, and education. Our commitment to quality, innovation, and
        client satisfaction has allowed us to build long-term partnerships around the
        world.
      </p>

      <img
        src="https://images.unsplash.com/photo-1521737604893-d14cc237f11d"
        alt="Team working together"
        class="story-image"
      />
    </section>

    <!-- MISSION & VISION -->
    <section class="mission-vision">
      <div class="mission-card">
        <h3>Our Mission</h3>
        <p>
          To empower businesses with intelligent, high-performance digital products that
          simplify processes, enhance user experiences, and unlock new opportunities.
        </p>
      </div>

      <div class="mission-card">
        <h3>Our Vision</h3>
        <p>
          To become a global leader in AI-driven innovation and help shape a future where
          technology elevates every aspect of human experience.
        </p>
      </div>
    </section>

    <!-- COMPANY VALUES -->
    <section class="values-section">
      <h2>Our Core Values</h2>

      <div class="values-grid">
        <div class="value-card">
          <h4>Innovation</h4>
          <p>
            We constantly explore new technologies to create smarter and more efficient
            solutions.
          </p>
        </div>

        <div class="value-card">
          <h4>Integrity</h4>
          <p>
            Our work is based on honesty, transparency, and a commitment to doing what's
            right.
          </p>
        </div>

        <div class="value-card">
          <h4>Excellence</h4>
          <p>
            We strive for perfection in everything we design, build, and deliver.
          </p>
        </div>

        <div class="value-card">
          <h4>Customer Success</h4>
          <p>
            Your success is at the core of every decision we make and every solution we
            build.
          </p>
        </div>
      </div>
    </section>

    <!-- TIMELINE -->
    <section class="timeline-section">
      <h2>Our Journey So Far</h2>

      <div class="timeline">
        <div class="timeline-item">
          <span>2018</span>
          <p>Company founded with a small team and a big vision.</p>
        </div>

        <div class="timeline-item">
          <span>2020</span>
          <p>Launched our first AI automation platform used by 70+ businesses.</p>
        </div>

        <div class="timeline-item">
          <span>2022</span>
          <p>Expanded to international markets with clients in 6+ countries.</p>
        </div>

        <div class="timeline-item">
          <span>2024</span>
          <p>Reached 50+ major enterprise projects delivered successfully.</p>
        </div>
      </div>
    </section>

    <!-- STATS SECTION -->
    <section class="stats-section">
      <div class="stats-grid">
        <div class="stat-box">
          <h3>6+</h3>
          <p>Years of Experience</p>
        </div>

        <div class="stat-box">
          <h3>150+</h3>
          <p>Projects Delivered</p>
        </div>

        <div class="stat-box">
          <h3>20+</h3>
          <p>Industries Served</p>
        </div>

        <div class="stat-box">
          <h3>98%</h3>
          <p>Satisfaction Rate</p>
        </div>
      </div>
    </section>

    <!-- LEADERSHIP TEAM -->
    <section class="leadership-section">
      <h2>Leadership Team</h2>

      <div class="leadership-grid">
        <div class="leader-card">
          <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=400&h=400&fit=crop" alt="James Anderson" />
          <h4>James Anderson</h4>
          <p>CEO & Founder</p>
        </div>

        <div class="leader-card">
          <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=400&h=400&fit=crop" alt="Olivia Turner" />
          <h4>Olivia Turner</h4>
          <p>Chief Technology Officer</p>
        </div>

        <div class="leader-card">
          <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=400&h=400&fit=crop" alt="Ethan Walker" />
          <h4>Ethan Walker</h4>
          <p>Head of Product</p>
        </div>
      </div>
    </section>

    <!-- FAQ SECTION -->
    <section class="about-faq">
      <h2>Frequently Asked Questions</h2>

      <div class="faq-container">
        <div class="faq-item">
          <h4>What industries do you work with?</h4>
          <p>
            We serve clients across healthcare, eCommerce, education, finance,
            logistics, entertainment, and more.
          </p>
        </div>

        <div class="faq-item">
          <h4>Do you offer post-launch support?</h4>
          <p>
            Yes. We provide continuous maintenance, monitoring, updates, and scaling
            support.
          </p>
        </div>

        <div class="faq-item">
          <h4>Can you build fully customized solutions?</h4>
          <p>
            Absolutely. Every solution we build is custom-tailored to business
            requirements, not templates.
          </p>
        </div>
      </div>
    </section>

    <!-- FINAL CTA -->
    <section class="about-final-cta">
      <h2>Want to Learn More About Our Team?</h2>
      <p>
        We'd love to hear from you. Let's discuss how we can help bring your ideas
        to life.
      </p>
      <button class="btn-primary">Contact Us</button>
    </section>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

section {
  padding: 60px 10%;
}

/* HERO SECTION */
.about-hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 50px;
  margin-bottom: 40px;
  background: linear-gradient(135deg, #f5f7fa 0%, #f9f9f9 100%);
  padding: 80px 10% !important;
  border-radius: 15px;
}

.about-hero .hero-text {
  flex: 1;
}

.about-hero h1 {
  font-size: 48px;
  font-weight: 800;
  margin-bottom: 20px;
  color: #1a1a1a;
  line-height: 1.2;
}

.about-hero p {
  font-size: 18px;
  color: #555;
  line-height: 1.8;
  margin-bottom: 30px;
}

.hero-image {
  flex: 1;
  width: 100%;
  height: 450px;
  object-fit: cover;
  border-radius: 15px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}

/* OUR STORY */
.our-story {
  background: linear-gradient(135deg, #f5f7fa 0%, #ffffff 100%);
  border-radius: 15px;
  padding: 80px 60px;
  border: 1px solid #e8eef5;
  box-shadow: 0 5px 20px rgba(102, 126, 234, 0.08);
}

.our-story h2 {
  font-size: 40px;
  font-weight: 800;
  margin-bottom: 30px;
  color: #1a1a1a;
  text-align: center;
}

.our-story p {
  font-size: 17px;
  line-height: 1.9;
  color: #666;
  margin-bottom: 25px;
  text-align: justify;
}

.story-image {
  margin-top: 40px;
  width: 100%;
  height: 450px;
  object-fit: cover;
  border-radius: 15px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}

/* MISSION & VISION */
.mission-vision {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  margin: 60px 0;
}

.mission-card {
  padding: 40px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.mission-card h3 {
  font-size: 24px;
  margin-bottom: 15px;
}

.mission-card p {
  font-size: 16px;
  line-height: 1.6;
}

/* VALUES SECTION */
.values-section h2 {
  font-size: 36px;
  font-weight: 700;
  text-align: center;
  margin-bottom: 40px;
  color: #1a1a1a;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.value-card {
  padding: 40px;
  border: 2px solid #e8eef5;
  border-radius: 12px;
  transition: all 0.3s ease;
  background: white;
  position: relative;
  overflow: hidden;
}

.value-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  transform: scaleY(0);
  transition: transform 0.3s ease;
}

.value-card:hover::before {
  transform: scaleY(1);
}

.value-card:hover {
  box-shadow: 0 12px 30px rgba(102, 126, 234, 0.15);
  transform: translateY(-8px);
  border-color: #667eea;
}

.value-card h4 {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 15px;
  color: #1a1a1a;
}

.value-card p {
  font-size: 15px;
  color: #666;
  line-height: 1.7;
}

/* TIMELINE */
.timeline-section h2 {
  font-size: 36px;
  font-weight: 700;
  text-align: center;
  margin-bottom: 50px;
  color: #1a1a1a;
}

.timeline {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;
}

.timeline-item {
  padding: 40px 30px;
  text-align: center;
  border-radius: 12px;
  background: white;
  border: 2px solid #e8eef5;
  transition: all 0.3s ease;
  position: relative;
}

.timeline-item:hover {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-color: transparent;
  box-shadow: 0 12px 35px rgba(102, 126, 234, 0.3);
  transform: translateY(-10px);
}

.timeline-item span {
  display: block;
  font-size: 28px;
  font-weight: 800;
  margin-bottom: 15px;
  color: #667eea;
}

.timeline-item:hover span {
  color: white;
}

.timeline-item p {
  font-size: 15px;
  line-height: 1.6;
  color: #666;
  font-weight: 500;
}

.timeline-item:hover p {
  color: white;
}

/* STATS SECTION */
.stats-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 80px 10%;
  margin: 60px 0;
  border-radius: 10px;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 40px;
  text-align: center;
}

.stat-box h3 {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 10px;
}

.stat-box p {
  font-size: 16px;
}

/* LEADERSHIP SECTION */
.leadership-section h2 {
  font-size: 36px;
  font-weight: 700;
  text-align: center;
  margin-bottom: 50px;
  color: #1a1a1a;
}

.leadership-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}

.leader-card {
  text-align: center;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  background: white;
  border: 1px solid #f0f0f0;
}

.leader-card:hover {
  transform: translateY(-15px);
  box-shadow: 0 15px 40px rgba(102, 126, 234, 0.2);
  border-color: #667eea;
}

.leader-card img {
  width: 100%;
  height: 350px;
  object-fit: cover;
  display: block;
}

.leader-card h4 {
  font-size: 20px;
  font-weight: 700;
  margin: 25px 0 8px;
  color: #1a1a1a;
}

.leader-card p {
  color: #667eea;
  font-size: 15px;
  font-weight: 600;
  margin-bottom: 25px;
}

/* FAQ SECTION */
.about-faq {
  background: linear-gradient(135deg, #f5f7fa 0%, #ffffff 100%);
  border-radius: 15px;
  padding: 80px 60px;
  margin: 60px 0;
  border: 1px solid #e8eef5;
}

.about-faq h2 {
  font-size: 40px;
  font-weight: 800;
  text-align: center;
  margin-bottom: 50px;
  color: #1a1a1a;
}

.faq-container {
  display: grid;
  gap: 30px;
  max-width: 800px;
  margin: 0 auto;
}

.faq-item {
  padding: 25px;
  border-left: 4px solid #667eea;
  background: white;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.faq-item:hover {
  box-shadow: 0 8px 20px rgba(102, 126, 234, 0.1);
  transform: translateX(5px);
}

.faq-item h4 {
  font-size: 18px;
  margin-bottom: 12px;
  color: #1a1a1a;
  cursor: pointer;
  transition: color 0.3s ease;
  font-weight: 700;
}

.faq-item h4:hover {
  color: #667eea;
}

.faq-item p {
  font-size: 15px;
  color: #666;
  line-height: 1.7;
}

/* FINAL CTA */
.about-final-cta {
  text-align: center;
  padding: 80px 10%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 10px;
  margin: 60px 0;
}

.about-final-cta h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 15px;
}

.about-final-cta p {
  font-size: 18px;
  margin-bottom: 30px;
  line-height: 1.6;
}

.btn-primary {
  padding: 14px 40px;
  background-color: white;
  color: #667eea;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

/* RESPONSIVE */
@media (max-width: 768px) {
  section {
    padding: 40px 5%;
  }

  .about-hero,
  .mission-vision {
    flex-direction: column;
    grid-template-columns: 1fr;
  }

  .values-grid,
  .timeline,
  .stats-grid,
  .leadership-grid {
    grid-template-columns: 1fr;
  }

  .about-hero h1 {
    font-size: 32px;
  }

  .mission-card,
  .about-faq {
    padding: 40px;
  }
}
</style>
