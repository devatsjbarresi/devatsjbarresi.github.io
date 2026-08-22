---
layout: default
title: Download
permalink: /download/
---


<h1 align="center">Download</h1>
{::nomarkdown}
<style>
  .download-products {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-template-areas:
      "shark-title squid-title"
      "shark-description squid-description"
      "shark-action squid-action";
    column-gap: 1.5rem;
    row-gap: 0;
    max-width: 50rem;
    margin: 1.5rem auto 2.5rem;
    text-align: center;
  }
  .download-products h2,
  .download-products p { margin: 0; }
  .download-products h2 + * { margin-top: 0; }
  .shark-title { grid-area: shark-title; }
  .shark-description { grid-area: shark-description; }
  .shark-action { grid-area: shark-action; }
  .squid-title { grid-area: squid-title; }
  .squid-description { grid-area: squid-description; }
  .squid-action { grid-area: squid-action; }
  .shark-title,
  .squid-title {
    margin-bottom: 0 !important;
    padding: 1.5rem 1.875rem 0.75rem;
    border: 1px solid #d8d8dc;
    border-bottom: 0;
    border-radius: 10px 10px 0 0;
  }
  .shark-description,
  .squid-description {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding: 0 1.875rem;
    border-right: 1px solid #d8d8dc;
    border-left: 1px solid #d8d8dc;
  }
  .shark-action,
  .squid-action {
    padding: 0.75rem 1.875rem 1.5rem;
    border: 1px solid #d8d8dc;
    border-top: 0;
    border-radius: 0 0 10px 10px;
  }
  .wireshark-download {
    width: fit-content;
    max-width: calc(100% - 3rem);
    margin: 0 auto 2.5rem;
    padding: 1.5rem 1.875rem;
    text-align: center;
    border: 1px solid #d8d8dc;
    border-radius: 10px;
  }
  .wireshark-download p { margin: 0; }
  .wireshark-download h2 {
    margin: 0 0 0.75rem;
  }
  .wireshark-download p + p { margin-top: 1.5rem; }
  .wireshark-download p:last-child {
    display: flex;
    justify-content: center;
  }
  @media (max-width: 700px) {
    .download-products {
      grid-template-columns: 1fr;
      grid-template-areas:
        "shark-title"
        "shark-description"
        "shark-action"
        "squid-title"
        "squid-description"
        "squid-action";
      row-gap: 0;
      max-width: 28rem;
    }
    .squid-title { margin-top: 1.5rem !important; }
  }
</style>
<div class="download-products">
  <h2 class="shark-title">ShowShark</h2>
  <h2 class="squid-title">ShowSquid</h2>
  <div class="shark-description">
    <p><strong style="display: inline-block; font-size: 1.25rem; margin-bottom: 0.35rem;">1.0</strong><br>Includes example capture file.</p>
  </div>
  <div class="squid-description">
    <p><strong style="display: inline-block; font-size: 1.25rem; margin-bottom: 0.35rem;">1.0.1</strong><br><a href="/docs/showsquid/">ShowSquid</a> is a desktop companion app that gives ShowShark more network traffic to analyse.</p>
  </div>
  <p class="shark-action">
    <button type="button" id="download-btn" class="button" style="background-color: #8561E7; color: white; padding: 15px 30px; border: none; border-radius: 25px; font: inherit; font-weight: bold; cursor: pointer; display: inline-block;">Download ShowShark</button>
  </p>
  <p class="squid-action">
    <button type="button" id="showsquid-download-btn" class="button" style="background-color: #8561E7; color: white; padding: 15px 30px; border: none; border-radius: 25px; font: inherit; font-weight: bold; cursor: pointer; display: inline-block;">Download ShowSquid</button>
  </p>
</div>
<div class="wireshark-download">
  <h2>Wireshark</h2>
  <p>ShowShark requires Wireshark 4.0 or later.</p>
  <p>
    <a href="https://www.wireshark.org/download.html" target="_blank" rel="noopener noreferrer" class="button" style="background-color: #1D72C4; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold; display: inline-block;">Download Wireshark</a>
  </p>
</div>
{:/}

### Known Issues

- Editing manufacturer and protocol filters manually may not update correctly in the Filter Builder.
- Some captures may still show incomplete hostnames for noisy discovery traffic.

{::nomarkdown}
<hr>
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/">← About</a></div>
  <div style="text-align: right;"><a href="/docs/guide/">Guide →</a></div>
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
      <input type="hidden" name="version" value="v1.0">
      <input type="text" name="_gotcha" tabindex="-1" autocomplete="off" aria-hidden="true" style="position: absolute; left: -9999px;">
      <p style="margin-top: 0; margin-bottom: 1rem; color: #666;">A little bit about you.<br>This helps me understand how ShowShark is being used.</p>

      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 0.75rem; margin-bottom: 0.75rem;">
        <input type="text" id="first-name" name="first_name" placeholder="First name" aria-label="First name" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
        <input type="text" id="last-name" name="last_name" placeholder="Last name" aria-label="Last name" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
      </div>

      <div style="margin-bottom: 1rem;">
        <input type="text" id="user-info" name="about" placeholder="Where do you work, what do you do?" aria-label="Where do you work, what do you do?" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
      </div>

      <div style="margin-bottom: 1.5rem;">
        <label for="user-email" style="display: block; margin-bottom: 0.5rem; color: #666;">If you'd like to keep up with releases, pop your email address in here. You won't be spammed.</label>
        <input type="email" id="user-email" name="contact_email" placeholder="keepmeposted@example.com" style="width: 100%; padding: 0.75rem; border: 1px solid #ddd; border-radius: 4px; font-size: 1rem; box-sizing: border-box;">
      </div>

      <button type="submit" style="background: #8561E7; color: white; padding: 0.75rem 2rem; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer; font-weight: 500; width: 100%;">
        Download Now
      </button>
    </form>
  </div>
</div>
{:/}

{::nomarkdown}
<!-- ShowSquid Download Modal -->
<iframe name="showsquid-tracking-frame" title="ShowSquid download notification" style="display: none;"></iframe>
<div id="showsquid-download-modal" style="display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.5);">
  <div style="background-color: white; margin: 10% auto; padding: 2rem; border-radius: 8px; max-width: 560px; position: relative;">
    <span id="close-showsquid-modal" style="position: absolute; right: 1rem; top: 1rem; font-size: 28px; font-weight: bold; cursor: pointer; color: #999;">&times;</span>

    <h2 style="margin-top: 0; margin-bottom: 1rem; text-align: center;">Select ShowSquid Download</h2>

    <div style="display: grid; gap: 0.75rem;">
      <strong>macOS</strong>
      <a href="https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0/ShowSquid_1.0.1_osx-x64.dmg" data-download-product="ShowSquid" data-download-version="v1.0.1" data-download-platform="macOS x64" class="button" style="background-color: #8561E7; color: white; padding: 12px 18px; border-radius: 8px; text-decoration: none; font-weight: bold; text-align: center;">macOS Intel / x64</a>
      <a href="https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0/ShowSquid_1.0.1_osx-arm64.dmg" data-download-product="ShowSquid" data-download-version="v1.0.1" data-download-platform="macOS arm64" class="button" style="background-color: #8561E7; color: white; padding: 12px 18px; border-radius: 8px; text-decoration: none; font-weight: bold; text-align: center;">macOS Apple Silicon / arm64</a>
      <strong style="margin-top: 0.5rem;">Windows</strong>
      <a href="https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0/ShowSquid_1.0.1_win-x64_setup.exe" data-download-product="ShowSquid" data-download-version="v1.0.1" data-download-platform="Windows x64 setup" class="button" style="background-color: #8561E7; color: white; padding: 12px 18px; border-radius: 8px; text-decoration: none; font-weight: bold; text-align: center;">Windows x64 installer</a>
      <a href="https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0/ShowSquid_1.0.1_win-arm64_setup.exe" data-download-product="ShowSquid" data-download-version="v1.0.1" data-download-platform="Windows arm64 setup" class="button" style="background-color: #8561E7; color: white; padding: 12px 18px; border-radius: 8px; text-decoration: none; font-weight: bold; text-align: center;">Windows arm64 installer</a>
    </div>
  </div>
</div>
{:/}

<script>
(function() {
  var showSharkTrackingEndpoint = 'https://formspree.io/f/meeeenyy';
  var showSquidTrackingEndpoint = 'https://formspree.io/f/xbdvpyzr';
  var downloadBtn = document.getElementById('download-btn');
  var modal = document.getElementById('download-modal');
  var showSquidDownloadBtn = document.getElementById('showsquid-download-btn');
  var showSquidModal = document.getElementById('showsquid-download-modal');
  var closeBtn = document.getElementById('close-modal');
  var closeShowSquidBtn = document.getElementById('close-showsquid-modal');
  var form = document.getElementById('download-form');
  var showSquidLinks = document.querySelectorAll('#showsquid-download-modal a[data-download-product]');
  var downloadUrl = 'https://github.com/devatsjbarresi/ShowShark-Releases/releases/download/1.0/ShowShark_v1_0.zip';

  function trackDownload(payload, endpoint) {
    var trackingForm = document.createElement('form');
    trackingForm.method = 'POST';
    trackingForm.action = endpoint;
    trackingForm.target = 'showsquid-tracking-frame';
    trackingForm.style.display = 'none';

    var fields = {
      _subject: 'ShowSquid Website Download',
      product: payload.product || 'Unknown',
      version: payload.version || 'Unknown',
      platform: payload.platform || 'Unknown',
      asset_url: payload.assetUrl || 'Unknown',
      page: window.location.href,
      user_agent: navigator.userAgent,
      timestamp: new Date().toISOString()
    };

    Object.keys(fields).forEach(function(name) {
      var input = document.createElement('input');
      input.type = 'hidden';
      input.name = name;
      input.value = fields[name];
      trackingForm.appendChild(input);
    });

    document.body.appendChild(trackingForm);
    trackingForm.submit();
    trackingForm.remove();
  }

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

  if (showSquidDownloadBtn && showSquidModal) {
    showSquidDownloadBtn.onclick = function(e) {
      e.preventDefault();
      showSquidModal.style.display = 'block';
      return false;
    };
  }

  if (closeShowSquidBtn && showSquidModal) {
    closeShowSquidBtn.onclick = function() {
      showSquidModal.style.display = 'none';
    };
  }
  
  window.onclick = function(event) {
    if (event.target == modal) {
      modal.style.display = 'none';
    }
    if (showSquidModal && event.target == showSquidModal) {
      showSquidModal.style.display = 'none';
    }
  };

  if (form) {
    form.onsubmit = function(e) {
      e.preventDefault();

      var formData = new FormData(form);

      var xhr = new XMLHttpRequest();
      xhr.open('POST', showSharkTrackingEndpoint, true);
      xhr.setRequestHeader('Accept', 'application/json');

      xhr.send(formData);

      modal.style.display = 'none';
      window.location.assign(downloadUrl);

      return false;
    };
  }

  if (showSquidLinks && showSquidLinks.length) {
    Array.prototype.forEach.call(showSquidLinks, function(link) {
      link.addEventListener('click', function(e) {
        e.preventDefault();
        trackDownload({
          product: link.getAttribute('data-download-product') || 'ShowSquid',
          version: link.getAttribute('data-download-version') || 'v1.0',
          platform: link.getAttribute('data-download-platform') || 'Unknown',
          assetUrl: link.href
        }, showSquidTrackingEndpoint);
        showSquidModal.style.display = 'none';
        window.location.assign(link.href);
        return false;
      });
    });
  }

})();
</script>
