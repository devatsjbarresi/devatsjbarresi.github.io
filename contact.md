---
layout: default
title: Contact
nav_exclude: true
permalink: /contact/
---

# Contact

> Captures are extremely useful for testing and development, but they can be huge so drop me a message and we can arrange a way to upload.
{: .note}

This is a personal project, so while I do my best to respond to all messages, please be patient if response times are longer than expected.

{::nomarkdown}
<form id="contact-form" action="https://formspree.io/f/mreegkqp" method="POST" style="width: 100%; margin: 2rem 0;">
  <div style="margin-bottom: 1.5rem;">
    <label for="email" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Your Email Address</label>
    <input type="email" name="_replyto" id="email" required placeholder="tellme@example.com" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem;">
  </div>
  <div style="margin-bottom: 1.5rem;">
    <label for="subject" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Subject</label>
    <input type="text" name="_subject" id="subject" placeholder="eg. Bug report, Feature request, I have a capture..." style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem;">
  </div>
  <div style="margin-bottom: 1.5rem;">
    <label for="message" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">Message</label>
    <textarea name="message" id="message" rows="6" required placeholder="Feedback, bug reports and feature requests are always well received. Please include as much detail as you can." style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; resize: vertical;"></textarea>
  </div>
  <div class="g-recaptcha" data-sitekey="6Ld9PmAtAAAAACLBUJv_7njjR30l4V5fvsmOLEyY" style="margin-bottom: 1.5rem;"></div>
  <div id="form-status" role="status" style="margin-bottom: 1rem; padding: 0.75rem; border-radius: 4px; display: none;"></div>
  <div style="text-align: center;">
  <button type="submit" id="submit-btn" style="background: #8561E7; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500;">Send Message</button>
  </div>
</form>
{:/}

<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
  var form = document.getElementById('contact-form');
  var submitBtn = document.getElementById('submit-btn');
  var status = document.getElementById('form-status');

  if (!form) return;

  function showStatus(type, message) {
    var colours = {
      success: { background: '#d4edda', colour: '#155724', border: '#c3e6cb' },
      warning: { background: '#fff3cd', colour: '#856404', border: '#ffeeba' },
      error: { background: '#f8d7da', colour: '#721c24', border: '#f5c6cb' }
    };
    var style = colours[type];

    status.style.display = 'block';
    status.style.background = style.background;
    status.style.color = style.colour;
    status.style.border = '1px solid ' + style.border;
    status.style.fontWeight = '600';
    status.style.textAlign = 'center';
    status.textContent = message;
  }

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    var captchaResponse = form.querySelector('[name="g-recaptcha-response"]');
    if (!captchaResponse || !captchaResponse.value) {
      showStatus('warning', 'Please complete the CAPTCHA before sending.');
      return;
    }

    submitBtn.textContent = 'Sending...';
    submitBtn.disabled = true;

    fetch(form.action, {
      method: 'POST',
      body: new FormData(form),
      headers: { 'Accept': 'application/json' }
    }).then(function(response) {
      return response.json().then(function(data) {
        if (!response.ok) {
          var message = data.errors && data.errors.length
            ? data.errors.map(function(error) { return error.message; }).join(' ')
            : 'Submission failed';
          throw new Error(message);
        }
      });
    }).then(function() {

      showStatus('success', '✓ Message sent successfully! Thank you for getting in touch.');
      form.reset();
      grecaptcha.reset();
    }).catch(function(error) {
      showStatus('error', 'Message not sent: ' + error.message);
      if (window.grecaptcha) grecaptcha.reset();
    }).finally(function() {
      submitBtn.textContent = 'Send Message';
      submitBtn.disabled = false;
    });
  });
});
</script>
