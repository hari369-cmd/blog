---
layout: post
title: "Japan Travel Map"
date:   2024-12-25
categories: travel
---

Here's a map of the prefectures I've visited and plan to visit:

<div id="japan-map">
    <object id="japan-map" data="/blog/assets/images/japan_map/jp.svg" type="image/svg+xml" style="width: 100%; height: auto;"></object>
</div>

<script>
document.getElementById('japan-map').addEventListener('load', function() {
    const svgDoc = this.contentDocument;
    
    // First, remove any default styling that might exist
    const style = svgDoc.createElementNS("http://www.w3.org/2000/svg", "style");
    style.textContent = `
        path {
            fill: #e0e0e0;
            stroke: #ffffff;
            stroke-width: 1;
        }
    `;
    svgDoc.getElementsByTagName("svg")[0].appendChild(style);

    // Then highlight Tokyo
    const tokyo = svgDoc.getElementById('JP13');
    if (tokyo) {
        tokyo.style.fill = '#4CAF50';
    }

    // Add hover effect
    const allPaths = svgDoc.getElementsByTagName('path');
    for (let path of allPaths) {
        path.addEventListener('mouseover', function() {
            const currentColor = this.style.fill;
            this.style.fill = '#a0a0a0';
            this.style.cursor = 'pointer';
            
            // Show prefecture name
            console.log(this.getAttribute('title'));
        });
        
        path.addEventListener('mouseout', function() {
            if (this.id === 'JP13') {
                this.style.fill = '#4CAF50';
            } else {
                this.style.fill = '#e0e0e0';
            }
        });
    }
});
</script>