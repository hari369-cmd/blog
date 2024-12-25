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
    
    // Set default color for all paths
    const allPaths = svgDoc.getElementsByTagName('path');
    for (let path of allPaths) {
        path.style.fill = '#e0e0e0';  // light gray for unvisited
        path.style.stroke = '#ffffff'; // white borders
        path.style.strokeWidth = '1';
    }

    // Highlight Tokyo
    const tokyo = svgDoc.getElementById('JP-13');
    if (tokyo) {
        tokyo.style.fill = '#4CAF50';  // green for visited
    }
});
</script>