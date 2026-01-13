---
layout: default
title: Download
permalink: /download/
---


<h1 align="center">Downloads</h1>

  
<div style="text-align: center;">
  <p><strong>Latest ShowShark:</strong> Version 1.0.BETA1</p>
  
  <p>
    <a href="#" id="download-btn" class="button" style="background-color: #4f2581; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold; cursor: pointer;">Download ShowShark</a>
  </p>

  <br>
  
  <p><strong>Requires:</strong> Wireshark 4.0 or later</p>
  
  <p>
    <a href="https://www.wireshark.org/download.html" class="button" style="background-color: #1679a7; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold;">Download Wireshark</a>
  </p>
</div>

{::nomarkdown}
<!-- Download Modal -->
<div id="download-modal" style="display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.5);">
  <div style="background-color: white; margin: 10% auto; padding: 2rem; border-radius: 8px; max-width: 500px; position: relative;">
    <span id="close-modal" style="position: absolute; right: 1rem; top: 1rem; font-size: 28px; font-weight: bold; cursor: pointer; color: #999;">&times;</span>
    
    <h2 style="margin-top: 0;">A little bit about you</h2>
    <p style="color: #666; margin-bottom: 1.5rem;">This helps me understand how ShowShark is being used. You won't be spammed.</p>
    
    <form id="download-form" action="https://formspree.io/f/meeeenyy" method="POST" novalidate>
      <input type="hidden" name="_subject" value="ShowShark Download">
      <input type="hidden" name="message" value="Downloaded ShowShark v1.0.BETA1">
      <input type="hidden" name="info" id="hidden-info" value="Not provided">
      
      <div style="margin-bottom: 1rem;">
        <label for="user-info" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">A little bit about you.</label>
        <textarea id="user-info" rows="4" placeholder="eg. name, company and your intended use of ShowShark (or just leave it blank)." style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box; resize: vertical;"></textarea>
      </div>
      
      <div style="margin-bottom: 1.5rem;">
        <label for="user-email" style="display: block; margin-bottom: 0.5rem; font-weight: 500;">If you'd like to keep up with releases, pop your email address in here.</label>
        <input type="text" id="user-email" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
      </div>
      
      <button type="submit" style="background: #4f2581; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500; width: 100%;">
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
  var downloadUrl = 'https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0.BETA1/ShowShark_v1_0_BETA1.zip';
  
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
