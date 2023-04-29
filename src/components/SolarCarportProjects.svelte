<script>
    let selectedImage = null;
  
    const handleImageClick = (image) => {
      selectedImage = selectedImage === image ? null : image;
    };
  </script>
  
  <style>
    .image-container {
      position: relative;
    }
  
    .image {
      width: 100%;
      transition: transform 0.3s ease;
    }
  
    .image.selected {
      transform: scale(1.5);
      z-index: 1;
    }
  
    .title {
      text-align: center;
      margin-top: 1rem;
    }
  </style>
  
  <div class="image-container">
    <img
      src="/path/to/image1.jpg"
      alt="Image 1"
      class="image {selectedImage === 'image1' ? 'selected' : ''}"
      on:click={() => handleImageClick('image1')}
    />
    <div class="title">Image 1 Title</div>
  </div>
  
  <div class="image-container">
    <img
      src="/path/to/image2.jpg"
      alt="Image 2"
      class="image {selectedImage === 'image2' ? 'selected' : ''}"
      on:click={() => handleImageClick('image2')}
    />
    <div class="title">Image 2 Title</div>
  </div>
  
  <!-- Add more image containers as needed -->
  
  