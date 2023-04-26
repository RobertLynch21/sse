<script>
  // Add any JavaScript code here if needed
</script>

<section class="contact">
  <div class="contact-info">
    <div class="address-block">
      <h2>William Grill</h2>
      <address>
        Email: info@sseenterprise.com <br />
        Phone: +1 (484) 924-9521
      </address>
    </div>
    <div class="address-block">
      <h2>Kim Grill</h2>
      <address>
        Email: info@sseenterprise.com<br />
        Phone: +1 (484) 924-9525
      </address>
    </div>
  </div>

  <div class="social-media">
    <a href="https://www.facebook.com/solarcompany" target="_blank" rel="noopener noreferrer" class="social-link">
      <img src="/media/facebook.png" alt="Facebook" class="social-icon">
    </a>
    <a href="https://www.linkedin.com/company/solarcompany" target="_blank" rel="noopener noreferrer" class="social-link">
      <img src="/media/linkedin.png" alt="LinkedIn" class="social-icon">
    </a>
  </div>
</section>

<style>
  /* Contact section */
  .contact {
    text-align: center;
  }

  .contact-info {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }

  .address-block {
    display: inline-block;
    margin: 10px 20px;
    font-weight: bold;
  }

  .address-block h2 {
    margin-bottom: 5px;
  }
 /* social media icons */
 .social-media {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
  }

  .social-link {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    overflow: hidden;
  }

  .social-icon {
    width: 100%;
    height: auto;
    transition: 0.3s;
  }

  .social-link:hover .social-icon {
    transform: scale(1.1);
  }
</style>