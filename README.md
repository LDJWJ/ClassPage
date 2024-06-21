# Class 수업
https://ldjwj.github.io/ClassPage/

<div id="stopwatch">00:00:00</div>
<button onclick="startStopwatch()">Start</button>
<button onclick="stopStopwatch()">Stop</button>
<button onclick="resetStopwatch()">Reset</button>

<script>
let startTime, interval;

function startStopwatch() {
  startTime = new Date().getTime();
  interval = setInterval(updateStopwatch, 10);
}

function stopStopwatch() {
  clearInterval(interval);
}

function resetStopwatch() {
  clearInterval(interval);
  document.getElementById("stopwatch").textContent = "00:00:00";
}

function updateStopwatch() {
  const currentTime = new Date().getTime() - startTime;
  const seconds = Math.floor((currentTime / 1000) % 60);
  const minutes = Math.floor((currentTime / (1000 * 60)) % 60);
  const hours = Math.floor((currentTime / (1000 * 60 * 60)) % 24);

  document.getElementById("stopwatch").textContent =
    `${hours.toString().padStart(2, "0")}:${minutes.toString().padStart(2, "0")}:${seconds.toString().padStart(2, "0")}`;
}
</script>


### 수업
![프로젝트 수행](class_status01.png)
<br>
<br>
![쉬는 시간](class_status02.png)
<br>
<br>
![실습 시간](class_status03.png)
