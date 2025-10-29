# kary-portfolio
a quick portfolio showing off my art and nature photography
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  margin-top: 20px;
}

.gallery-grid figure {
  margin: 0;
  text-align: center;
}

.gallery-grid img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.3s;
}

.gallery-grid img:hover {
  transform: scale(1.05);
}

.gallery-grid figcaption {
  margin-top: 8px;
  font-size: 0.9rem;
  color: #555;
}

/* Lightbox styles */
.lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.8);
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 10px;
}
<section id="Fishes">
  <h2>Fishes</h2>
  <div class="gallery">
    <!-- Add your art images here -->
  <img src="images/DSCN5563.JPG" width="400" height="800" alt="Miniellus procne - Swallowtail Shiner">
      <em>Miniellus procne - Swallowtail Shiner</em>
  <img src="images/chaetodton1531.JPG" width="400" height="800" alt="Enneacanthus chaetodon - Blackbanded Sunfish">
      <em>Enneacanthus chaetodon - Blackbanded Sunfish</em>
  </div>
</section>

<section id="fish">
<h2>Fish Photography</h2>
<div class="gallery">
<figure>
<img src="images/DSCN5563.JPG" alt="Miniellus procne - Swallowtail Shiner">
<figcaption>Miniellus procne - Swallowtail Shiner</figcaption>
</figure>
<figure>
<img src="images/chaetodton1531.JPG" alt="Enneacanthus chaetodon - Blackbanded Sunfish">
<figcaption>Enneacanthus chaetodon - Blackbanded Sunfish</figcaption>
</figure>
</div>
</section>

<section id="insects">
  <h2>Insects</h2>
  <div class="gallery">
      <!-- Add your insect photos here -->
    <img src="images/actias2953.JPG" width="400" height="800" alt="Reared A. luna">
      <em>Reared Actias luna</em>
    <img src="images/astyanax3282.JPG" width="400" height="800" alt="">
      <em>Wild Limenitis arthemis astyanax</em>
  </div>
</section>
<section id="plants">
  <h2>Plants</h2>
  <div class="gallery">
      <!-- Add your insect photos here -->
    <img src="images/platanthera2902.JPG" width="400" height="800" alt="Reared A. luna">
      <em>Platanthera peramoena, S1 in MD</em>
    <img src="images/cardinalis2212.JPG" width="400" height="800" alt="">
      <em>Lobelia cardinalis</em>
  </div>
</section>

<script>
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = document.getElementById('lightbox-img');

  document.querySelectorAll('.gallery-grid img').forEach(img => {
    img.addEventListener('click', () => {
      lightboxImg.src = img.src;
      lightbox.style.display = 'flex';
    });
  });

  lightbox.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });
</script>
