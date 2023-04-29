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
    <a href="https://www.facebook.com/sseenterprisellc/?show_switched_toast=0&show_invite_to_follow=0&show_switched_tooltip=0&show_podcast_settings=0&show_community_review_changes=0&show_community_rollback=0&show_follower_visibility_disclosure=0" target="_blank" rel="noopener noreferrer" class="social-link">
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