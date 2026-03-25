---
layout: default
title: Download
permalink: /download/
---


<h1 align="center">Downloads</h1>

  
<div style="text-align: center; margin-top: 1.5rem;">
  <p style="margin-bottom: 1.5rem;"><strong>Latest ShowShark:</strong> Version 1.0.BETA4</p>
  
  <p style="margin-top: 0;">
    <a href="#" id="download-btn" class="button" style="background-color: #8561E7; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold; cursor: pointer;">Download ShowShark</a>
  </p>

  <br>
  
  <p style="margin-bottom: 1.5rem;"><strong>Requires:</strong> Wireshark 4.0 or later</p>
  
  <p style="margin-top: 0;">
    <a href="https://www.wireshark.org/download.html" target="_blank" rel="noopener noreferrer" class="button" style="background-color: #1D72C4; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold;">Download Wireshark</a>
  </p>

  <br>
</div>

{::nomarkdown}
{% include version_history.html %}
{:/}

{::nomarkdown}
<hr>
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/">← About</a></div>
  <div style="text-align: right;"><a href="/docs/setup/">Documentation →</a></div>
</div>
{:/}

{::nomarkdown}
<!-- Download Modal -->
<div id="download-modal" style="display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.5);">
  <div style="background-color: white; margin: 10% auto; padding: 2rem; border-radius: 8px; max-width: 500px; position: relative;">
    <span id="close-modal" style="position: absolute; right: 1rem; top: 1rem; font-size: 28px; font-weight: bold; cursor: pointer; color: #999;">&times;</span>
    
    <h2 style="margin-top: 0;">Just quickly...</h2>
    <form id="download-form" action="https://formspree.io/f/meeeenyy" method="POST" novalidate>
      <input type="hidden" name="_subject" value="ShowShark Download">
      <input type="hidden" name="message" value="ShowShark download">
      <input type="hidden" name="version" value="v1.0.BETA4">
      <input type="hidden" name="info" id="hidden-info" value="Not provided">
      
      <div style="margin-bottom: 1rem;">
        <label for="user-info" style="display: block; margin-bottom: 0.5rem; color: #666;">A little bit about you (optional).<br>This helps me understand how ShowShark is being used.</label>
        <textarea id="user-info" rows="4" placeholder="eg. name, company, intended use" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box; resize: vertical;"></textarea>
      </div>
      
      <div style="margin-bottom: 1.5rem;">
        <label for="user-email" style="display: block; margin-bottom: 0.5rem; color: #666;">If you'd like to keep up with releases, pop your email address in here. You won't be spammed.</label>
        <input type="text" id="user-email" placeholder="keepmeposted@example.com" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
      </div>
      
      <button type="submit" style="background: #8561E7; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500; width: 100%;">
        Download Now
      </button>
    </form>
  </div>
</div>
{:/}

<script>
(function() {
  var downloadBtn = document.getElementById('download-btn');
  var modal = document.getElementById('download-modal');
  var closeBtn = document.getElementById('close-modal');
  var form = document.getElementById('download-form');
  var downloadUrl = 'https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0.BETA4/ShowShark_v1_0_BETA4.zip';


  if (!downloadBtn || !modal) return;
  
  downloadBtn.onclick = function(e) {
    e.preventDefault();
    modal.style.display = 'block';
    return false;
  };
  
  if (closeBtn) {
    closeBtn.onclick = function() {
      modal.style.display = 'none';
    };
  }
  
  window.onclick = function(event) {
    if (event.target == modal) {
      modal.style.display = 'none';
    }
  };
  
  if (form) {
    form.onsubmit = function(e) {
      e.preventDefault();
      
      var info = document.getElementById('user-info');
      var email = document.getElementById('user-email');
      
      var infoValue = info ? info.value.trim() : '';
      var emailValue = email ? email.value.trim() : '';
      
      var hiddenInfo = document.getElementById('hidden-info');
      if (hiddenInfo) {
        hiddenInfo.value = infoValue || 'Not provided';
      }
      
      var formData = new FormData(form);
      if (emailValue) {
        formData.append('contact_email', emailValue);
      }
      
      var xhr = new XMLHttpRequest();
      xhr.open('POST', 'https://formspree.io/f/meeeenyy', true);
      xhr.setRequestHeader('Accept', 'application/json');
      
      xhr.onload = function() {
        window.location.href = downloadUrl;
        modal.style.display = 'none';
      };
      
      xhr.onerror = function() {
        window.location.href = downloadUrl;
        modal.style.display = 'none';
      };
      
      xhr.send(formData);
      
      return false;
    };
  }
})();
</script>
