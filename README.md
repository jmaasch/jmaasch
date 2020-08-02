### J R M A M

- 🔭 I’m currently working on machine learning for protein informatics @ [Penn Machine Biology Group](https://delafuentelab.seas.upenn.edu).
- 🌱 I’m currently learning ```sklearn```, ```TensorFlow```.
- 👯 I’m looking to collaborate on ```R``` package development.
- 📫 How to reach me: [LinkedIn](www.linkedin.com/in/jmaasch)
- 😄 Pronouns: she / her / they / them


<meta charset="utf-8">
<body>
<script src="https://d3js.org/d3.v4.min.js"></script>
<script src="https://d3js.org/d3-timer.v1.min.js"></script>

<script>
var width = 3000,
    height = 500;

var svg = d3.select("body").append("svg")
    .attr("width", width)
    .attr("height", height)
    .style("background", "#000000")
    .append("g")
    .attr("transform", "translate(" + [width / 2, height / 2] + ")");

var lissajous = svg.append("path")
    .attr("fill", "none")
    .attr("stroke", "#ffffff")
    .attr("stroke-opacity", 0.4)
    .attr("stroke-width", 0.1);

// Equation adapted from http://goatlink.deviantart.com/art/lissajous-curves-338721857

var range = d3.range(-40 * Math.PI, 15 * Math.PI, 0.05);

d3.timer(function(t) {
    var d = "M";

    for (var i = 0; i < range.length; i++) {
        var p = range[i];
        d += 0.15 * width * (Math.sin(3 * p + t / 2000) + Math.sin(3.01 * p + t / 2000));
        d += ",";
        d += 0.15 * height * (Math.sin(6 * p + t / 4000) + Math.sin(1.01 * p + t / 2000));
        if (i != range.length - 1) d += "L";
    }

    d.length--;
    lissajous.attr("d", d);

    svg.attr("transform", "translate(250,250)rotate(" + 360 * (t % 100000 / 100000) + ")")})

</script>


-->
