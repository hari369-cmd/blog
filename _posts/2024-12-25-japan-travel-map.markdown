---
layout: post
title: "Japan Travel Map"
date:   2024-12-25
categories: travel
---

{% include japan-map.html %}

<script>
    highlightPrefectures(['JP03', 'JP04', 'JP06', 'JP07', 'JP08', 'JP10', 'JP11', 'JP12', 
    'JP13', 'JP15', 'JP16', 'JP17', 'JP18', 'JP19', 'JP20', 'JP22', 'JP23', 'JP25', 'JP26',
    'JP27', 'JP28', 'JP29', 'JP36', 'JP37', 'JP38', 'JP39'], 'Visited');
    highlightPrefectures([], 'VisitingSoon');
    highlightPrefectures(['JP01', 'JP09', 'JP21', 'JP24', 'JP30', 'JP32', 'JP47'], 'PlanningToVisit');
</script>