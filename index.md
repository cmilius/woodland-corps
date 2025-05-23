---
layout: home
---

{{ site.description }}

![I needed to fill some whitespace]({{ "assets/images/woodland-corps-transparent.png" | relative_url }})

{% raw %}
<!-- Lottie Library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/lottie-web/5.10.2/lottie.min.js"></script>
<div id="lottie-animation" style="width:300px;height:300px;margin:auto;"></div>
<script>
lottie.loadAnimation({
  container: document.getElementById('lottie-animation'),
  renderer: 'svg',
  loop: true,
  autoplay: true,
  path: '/assets/lottie/stat-test.json'
});
</script>
{% endraw %}