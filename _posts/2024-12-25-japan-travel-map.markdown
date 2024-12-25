---
layout: post
title: "Japan Travel Map"
date:   2024-12-25
categories: travel
---

Here's a map of the prefectures I've visited and plan to visit:

<div id="japan-map">
    <object id="japan-map" data="/blog/assets/images/japan_map/japan.svg" type="image/svg+xml" style="width: 100%; height: auto;"></object>
</div>

<script>
document.getElementById('japan-map').addEventListener('load', function() {
    const svgDoc = this.contentDocument;
    const tokyo = svgDoc.getElementById('tokyo');  // assuming your SVG has IDs for prefectures
    if (tokyo) {
        tokyo.style.fill = '#4CAF50';  // green for visited
    }
});
</script>