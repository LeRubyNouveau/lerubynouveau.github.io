---
---
<script src="svg.js"></script>

<script>
function sly() {

var draw = SVG('filigrane'); // .size(300, 300);
var rect = draw.rect(100, 100).attr({ fill: '#f06' });

}

// document.addEventListener("DOMContentLoaded", function(event) {

window.addEventListener("load", function(event) {
  sly();
})();

</script>

<!--
  path
  <path d="M10 10 C 20 20, 40 20, 50 10" stroke="black" fill="transparent"/>

  S - same/symetric point in a path
  <path d="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80" stroke="black" fill="transparent"/>

  Q - quadratic only has 1 control point
  <path d="M10 80 Q 95 10 180 80" stroke="black" fill="transparent"/>

  T - several quadratics
  <path d="M10 80 Q 52.5 10, 95 80 T 180 80" stroke="black" fill="transparent"/>


  Also, arcs
  https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#Bezier_Curves

  rect circle text ellipse line polyline polygon
  https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Basic_Shapes
-->

<div id="filigrane" style="width:300px; height:300px; border: 1px solid silver;">
</div>
