---
layout: default
---

<div class='container'>
    <h1 class='text-primary'>Projects</h1>
    <p>Here's where you can find out about the projects of hack club members!</p>
    <br>
</div>

<div class="container">
  <div class="row">
    <div class="col-sm">
      <div class="card" style="width: 18rem;">
        <img class="card-img-top" id="crd1" src="data:image/gif;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs%3D" alt="Pretend this has color...">
        <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
      </div>
    </div>
    <div class="col-sm">
      <div class="card" style="width: 18rem;">
        <img class="card-img-top" id="crd1" src="assets/kekw.png" alt="Pretend this has color...">
        <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
      </div>
    </div>
    <div class="col-sm">
      {% include project-card.html
      title = "QAE without Phase Estimation"
      description = "My final project for BWSI 2021, implementing QAE with no phase estimation in Qiskit and Q#."
      repo = "https://github.com/Borris-the-real-OG/quantsoft-final-project" %}
    </div>
  </div>
  <script>
      var stringToColor = function(str) {
        var hash = 0;
        for (var i = 0; i < str.length; i++) {
            hash = str.charCodeAt(i) + ((hash << 5) - hash);
        }
        var colour = '#';
        for (var i = 0; i < 3; i++) {
            var value = (hash >> (i * 8)) & 0xFF;
            colour += ('00' + value.toString(16)).substr(-2);
        }
        return colour;
      }
      var getElementByXpath = function(path) {
        return document.evaluate(path, document, null, XPathResult.ORDERED_NODE_ITERATOR_TYPE, null);
      }
      var upath = getElementByXpath("//div[@class='card-body']/a[1]");
      var ipath = getElementByXpath("//img[@class='card-img-top']");
      var urls = []
      var url = upath.iterateNext();
      while (url) {
          urls.push(url);
          url = upath.iterateNext();
      }
      var imgs = []
      var img = ipath.iterateNext();
      while (img) {
          imgs.push(img);
          img = ipath.iterateNext();
      }
      for (let i = 0; i < imgs.length; i++) {
          if (imgs[i].src == "data:image/gif;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs%3D")
            imgs[i].style.backgroundColor = stringToColor(urls[i].href);
      }
  </script>
</div>