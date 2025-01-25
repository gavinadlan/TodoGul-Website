<template>
  <footer>
    <div class="footer-content">
      <p>&copy; 2025 Todogul. All rights reserved.</p>
      <p>Follow us on:</p>
      <div class="social-icons">
        <a href="#"><i class="fab fa-facebook"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterSection",
};
</script>

<style scoped>
footer {
  padding: 20px;
  background-color: #333;
  color: white;
  text-align: center;
}

.footer-content p {
  margin: 10px 0;
}

.social-icons a {
  color: white;
  margin: 0 10px;
  font-size: 1.5rem;
}

.social-icons a:hover {
  color: #8875ff;
}
</style>
