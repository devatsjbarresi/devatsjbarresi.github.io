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
  <div id="form-status" style="margin-bottom: 1rem; padding: 0.75rem; border-radius: 4px; display: none;"></div>
  <div style="text-align: center;">
  <button type="submit" id="submit-btn" style="background: #8561E7; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500;">Send Message</button>
  </div>
</form>
{:/}

<script>
document.addEventListener('DOMContentLoaded', function() {
  var form = document.getElementById('contact-form');
  if (!form) return;
  
  form.onsubmit = function(e) {
    e.preventDefault();
    
    var submitBtn = document.getElementById('submit-btn');
    var status = document.getElementById('form-status');
    
    submitBtn.textContent = 'Sending...';
    submitBtn.disabled = true;
    
    var xhr = new XMLHttpRequest();
    xhr.open('POST', form.action);
    xhr.setRequestHeader('Accept', 'application/json');
    
    xhr.onreadystatechange = function() {
      if (xhr.readyState !== XMLHttpRequest.DONE) return;
      
      if (xhr.status === 200) {
        status.style.display = 'block';
        status.style.background = '#d4edda';
        status.style.color = '#155724';
        status.style.border = '1px solid #c3e6cb';
        status.textContent = 'Thank you! Your message has been sent successfully.';
        form.reset();
      } else {
        status.style.display = 'block';
        status.style.background = '#f8d7da';
        status.style.color = '#721c24';
        status.style.border = '1px solid #f5c6cb';
        status.textContent = 'Sorry, there was an error. Please try again.';
      }
      
      submitBtn.textContent = 'Send Message';
      submitBtn.disabled = false;
    };
    
    xhr.send(new FormData(form));
    return false;
  };
});
</script>


