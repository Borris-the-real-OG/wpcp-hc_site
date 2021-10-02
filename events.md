---
layout: default
---

<div class='container'>
    <div class="row">
        <div class="col-sm">
            <div class="card text-center" style="width: 18rem;">
                <div class='card-body'>
                    <h1 class="card-title">1st USACO Contest</h1>
                    <p class='card-text'>December 18-21</p>
                    <h3 class='card-text' id='usaco_count'></h3>
                    <a href="https://usaco.guide/dashboard/" class="btn btn-primary" id='usaco_btn'>Practice</a>
                </div>
            </div>
        </div>
        <br><br>
        <div class="col-sm">
            <div class="card text-center" style="width: 18rem;">
                <div class='card-body'>
                    <h1 class="card-title">Congressional App Challenge</h1>
                    <p class='card-text'>November 1</p>
                    <h3 class='card-text' id='cap_count'></h3>
                    <a href="https://www.congressionalappchallenge.us/" class="btn btn-primary" id='cap_btn'>Register</a>
                </div>
            </div>
        </div>
        <br><br>
        <div class="col-sm">
            <div class="card text-center" style="width: 18rem;">
                <div class='card-body'>
                    <h1 class="card-title">CodeDay</h1>
                    <p class='card-text'>November 13-14</p>
                    <h3 class='card-text' id='code_count'></h3>
                    <a href="https://www.codeday.org/" class="btn btn-primary" id='code_btn'>Register</a>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    var now = new Date().getTime();

    var usaco_cnt = document.getElementById("usaco_count");
    var cap_cnt = document.getElementById("cap_count");
    var code_cnt = document.getElementById("code_count");

    var usaco_date = new Date("Dec 18, 2021 00:00:00").getTime();
    var to_usaco = usaco_date - now;

    var cap_date = new Date("Nov 1, 2021 00:00:00").getTime();
    var to_cap = cap_date - now;

    var code_date = new Date("Nov 13, 2021 00:00:00").getTime();
    var to_code = code_date - now;

    var timer = setInterval(function() {
        now = new Date().getTime();

        to_usaco = usaco_date - now;
        to_cap = cap_date - now;
        to_code = code_date - now;

        usaco_cnt.innerHTML = `${Math.floor(to_usaco / (1000*60*60*24))}d ${Math.floor((to_usaco % (1000*60*60*24)) / (1000*60*60))}h ${Math.floor((to_usaco % (1000*60*60)) / (1000*60))}m ${Math.floor((to_usaco % (1000* 60)) / 1000)}s`;
        cap_cnt.innerHTML = `${Math.floor(to_cap / (1000*60*60*24))}d ${Math.floor((to_cap % (1000*60*60*24)) / (1000*60*60))}h ${Math.floor((to_cap % (1000*60*60)) / (1000*60))}m ${Math.floor((to_cap % (1000* 60)) / 1000)}s`;
        code_cnt.innerHTML = `${Math.floor(to_code / (1000*60*60*24))}d ${Math.floor((to_code % (1000*60*60*24)) / (1000*60*60))}h ${Math.floor((to_code % (1000*60*60)) / (1000*60))}m ${Math.floor((to_code % (1000* 60)) / 1000)}s`;

        if (to_usaco < 0) {
            usaco_cnt.innerHTML = "In Progress"

            var usaco_but = document.getElementById("usaco_btn");
            usaco_but.innerHTML = "Gogogogo!";
            usaco_but.href = "http://www.usaco.org/index.php?page=contests";
        }
        if (to_cap < 0) {
            cap_cnt.innerHTML = "Contest Over";
            document.getElementById("cap_btn").style.display = "none";
        }
        if (to_code < 0 && to_code > -172799000) {
            code_cnt.innerHTML = "Ongoing";
        } else if (to_code < -172799000) {
            code_cnt.innerHTML = "Ended";
            document.getElementById("code_btn").style.display = "none";
        }
    }, 1000);
</script>