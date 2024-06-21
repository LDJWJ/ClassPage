# Class 수업
https://ldjwj.github.io/ClassPage/

<div id="stopwatch">00:00:00</div>
<button onclick="startStopwatch()">Start</button>
<button onclick="stopStopwatch()">Stop</button>
<button onclick="resetStopwatch()">Reset</button>

<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.29.1/moment.min.js"></script>
<script>
let startTime, interval;

function startStopwatch() {
  startTime = moment();
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
  const currentTime = moment().diff(startTime);
  const duration = moment.duration(currentTime);
  document.getElementById("stopwatch").textContent =
    `${duration.hours().toString().padStart(2, "0")}:${duration.minutes().toString().padStart(2, "0")}:${duration.seconds().toString().padStart(2, "0")}`;
}
</script>



<script>
// JavaScript 코드
</script>


### 수업
![프로젝트 수행](class_status01.png)
<br>
<br>
![쉬는 시간](class_status02.png)
<br>
<br>
![실습 시간](class_status03.png)
