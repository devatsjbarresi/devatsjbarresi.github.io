---
layout: default
title: Contact
nav_exclude: true
---

# Contact

Feedback, bug reports and feature requests are always well received.

Please include as much detail as you can.

Captures are extremely useful (I love them) for testing and development, but they can be huge so let me know and we can arrange a way to upload.

This is a personal project, so while I do my best to respond to all messages, please be patient if response times are longer than expected.

<form id="contact-form" action="https://formspree.io/f/mreegkqp" method="POST" style="max-width: 600px; margin: 2rem 0;">
  
  <div style="margin-bottom: 1.5rem;">
    <label for="email" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Your Email Address</label>
    <input type="email" name="email" id="email" required
           style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem;">
  </div>
  
  <div style="margin-bottom: 1.5rem;">
    <label for="subject" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Subject</label>
    <input type="text" name="subject" id="subject"
           style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem;">
  </div>
  
  <div style="margin-bottom: 1.5rem;">
    <label for="message" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Message</label>
    <textarea name="message" id="message" rows="6" required
              style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; resize: vertical;"></textarea>
  </div>
  
  <button type="submit" id="submit-btn"
          style="background: #b19cd9; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500;">
    Send Message
  </button>
  
  <div id="form-status" style="margin-top: 1rem; padding: 0.75rem; border-radius: 4px; display: none;"></div>
</form>

<script>
document.getElementById('contact-form').addEventListener('submit', function(e) {
  e.preventDefault();
  
  const form = this;
  const submitBtn = document.getElementById('submit-btn');
  const status = document.getElementById('form-status');
  
  submitBtn.textContent = 'Sending...';
  submitBtn.disabled = true;
  
  fetch(form.action, {
    method: 'POST',
    body: new FormData(form),
    headers: {
      'Accept': 'application/json'
    }
  })
  .then(response => {
    if (response.ok) {
      status.style.display = 'block';
      status.style.background = '#d4edda';
      status.style.color = '#155724';
      status.style.border = '1px solid #c3e6cb';
      status.textContent = 'Thank you! Your message has been sent successfully.';
      form.reset();
    } else {
      throw new Error('Network response was not ok');
    }
  })
  .catch(error => {
    status.style.display = 'block';
    status.style.background = '#f8d7da';
    status.style.color = '#721c24';
    status.style.border = '1px solid #f5c6cb';
    status.textContent = 'Sorry, there was an error sending your message. Please try again.';
  })
  .finally(() => {
    submitBtn.textContent = 'Send Message';
    submitBtn.disabled = false;
  });
});
</script>