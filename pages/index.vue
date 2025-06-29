<template>
  <div class="container">
    <!-- Header -->
    <header class="header">
      <div class="logo">onlearn</div>
      <nav>
        <a href="#">Home</a>
        <a href="#">Careers</a>
        <a href="#">Blog</a>
        <a href="#">About Us</a>
      </nav>
      <div class="auth-buttons">
        <button class="login">Login</button>
        <button class="signup">Sign Up</button>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <h1>Grow up your skills by online courses with Onlearning</h1>
      <p>Never stop learning</p>
      <div class="stats">
        <div>250k Assisted Student</div>
        <div>★★★★★</div>
      </div>
      <button class="explore-btn">Explore Path</button>
      <img src="/assets/hero-image.jpg" alt="Hero Image" width="240" height="240"/>
    </section>

    <!-- Popular Courses -->
    <section class="popular-courses">
      <h2>Popular Courses</h2>
      <div class="course-grid">
        <div class="course-card" v-for="(course, index) in courses" :key="index">
          <img :src="course.image" :alt="course.title" width="240" height="240"/>
          <h3>{{ course.title }}</h3>
          <p class="price">{{ course.price }} <span>{{ course.duration }}</span></p>
          <button>Enroll Now</button>
        </div>
      </div>
    </section>

    <!-- Course Categories -->
    <section class="courses-category">
      <h2>Courses Category</h2>
      <p>Onlearning is one powerful online software suite that combines all tools</p>
      <div class="category-grid">
        <div class="category-item" v-for="(cat, index) in categories" :key="index">
          <img :src="cat.image" :alt="cat.name" width="240" height="240"/>
          <p>{{ cat.name }}</p>
        </div>
      </div>
      <button class="explore-btn">Explore courses</button>
    </section>

    <!-- Benefits -->
    <section class="benefits">
      <h2>Benefits</h2>
      <div class="benefit-item" v-for="(benefit, index) in benefits" :key="index">
        <p>{{ benefit }}</p>
      </div>
      <div class="student-id">
        <h3>Get Student ID Card</h3>
        <img src="/assets/student-id.jpg" alt="Student ID" width="240" height="240"/>
      </div>
    </section>

    <!-- Staff Training -->
    <section class="staff-training">
      <h2>Staff Training</h2>
      <div class="training-item" v-for="(item, index) in training" :key="index">
        <p>{{ item }}</p>
      </div>
    </section>

    <!-- Gift Cards -->
    <section class="gift-cards">
      <h2>Why You should buy gift cards?</h2>
      <button class="buy-now-btn">Buy Now</button>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="columns">
        <div class="column">
          <h4>onlearn</h4>
          <p>Address: 1234 Example St, connecticut</p>
          <p>Tel: +1-555-555-555</p>
          <p>Response hours: 8 to 5</p>
          <p>Email: who@onlearn.com</p>
        </div>
        <div class="column">
          <h4>Categories</h4>
          <a href="#">Counseling</a>
          <a href="#">Health and Fitness</a>
          <a href="#">Individual Development</a>
          <a href="#">more</a>
        </div>
        <div class="column">
          <h4>Links</h4>
          <a href="#">About us</a>
          <a href="#">Blog</a>
          <a href="#">Email</a>
        </div>
        <div class="column newsletter">
          <h4>Stay up to date with the latest courses</h4>
          <input type="email" placeholder="Email" />
          <button>Send</button>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      courses: [
        { image: 'assets/course1.jpg', title: 'Course Management Basic', price: '$99', duration: '6h 40m' },
        { image: 'assets/course2.jpg', title: 'IBM Data Science Professionals', price: '$78', duration: '4h 20m' },
        { image: 'assets/course3.jpg', title: 'The Science of Well-Being', price: '$12', duration: '2h 30m' },
        { image: 'assets/course4.jpg', title: 'Python for Beginners', price: '$57', duration: '5h 10m' },
      ],
      categories: [
        { image: 'assets/beauty.jpg', name: 'Beauty' },
        { image: 'assets/medical.jpg', name: 'Medical' },
        { image: 'assets/sports.jpg', name: 'Sports' },
        { image: 'assets/nutrition.jpg', name: 'Nutrition' },
      ],
      benefits: [
        "Teachers don't get lost in the grid view and have a dedicated Podium space",
        "TA's and presenters can be moved to the front of the class",
        "Teachers can easily see all students and class data at one time"
      ],
      training: [
        "Teachers don't get lost in the grid view and have a dedicated Podium space",
        "TA's and presenters can be moved to the front of the class",
        "Teachers can easily see all students and class data at one time"
      ]
    }
  }
}
</script>

<style scoped>

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
  border-bottom: 1px solid #e0e0e0;
}
.header .logo {
  color: #2e7d32;
  font-size: 24px;
  font-weight: bold;
}
.header nav {
  display: flex;
  gap: 20px;
}
.header nav a {
  text-decoration: none;
  color: #666;
  font-size: 16px;
}
.header .auth-buttons {
  display: flex;
  gap: 10px;
}
.header .auth-buttons button {
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.header .auth-buttons .login {
  background: none;
  color: #2e7d32;
}
.header .auth-buttons .signup {
  background-color: #2e7d32;
  color: white;
}
.hero {
  background-color: #e0f2e9;
  padding: 50px 20px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.hero h1 {
  font-size: 36px;
  color: #333;
  margin-bottom: 20px;
}
.hero p {
  font-size: 18px;
  color: #666;
  margin-bottom: 20px;
}
.hero .stats {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 20px;
}
.hero .stats div {
  background-color: white;
  padding: 10px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.hero .explore-btn {
  background-color: #ff5722;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}
.hero img {
  position: absolute;
  right: 20px;
  top: 50%;
  transform: translateY(-50%);
  max-width: 40%;
}
.popular-courses {
  padding: 40px 20px;
  text-align: center;
}
.popular-courses h2 {
  font-size: 28px;
  color: #2e7d32;
  margin-bottom: 20px;
}
.course-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
.course-card {
  background-color: #e0f7fa;
  padding: 20px;
  border-radius: 8px;
  text-align: left;
}
.course-card img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 4px;
}
.course-card h3 {
  font-size: 20px;
  margin: 10px 0;
}
.course-card .price {
  color: #ff5722;
  font-weight: bold;
}
.course-card button {
  background-color: #2e7d32;
  color: white;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.footer {
  background-color: #e0f2e9;
  padding: 40px 20px;
  margin-top: 40px;
  text-align: center;
}
.footer .columns {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-bottom: 20px;
}
.footer .column h4 {
  color: #2e7d32;
  margin-bottom: 10px;
}
.footer .column a, .footer .column p {
  display: block;
  color: #666;
  text-decoration: none;
  margin: 5px 0;
}
.footer .newsletter input {
  padding: 8px;
  margin-right: 10px;
}
.footer .newsletter button {
  background-color: #2e7d32;
  color: white;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

</style>
