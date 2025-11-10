# theodoi-tiendobaucuhdnd
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Theo dõi tiến độ công tác bầu cử cấp xã</title>
<style>
  body {
    font-family: "Segoe UI", sans-serif;
    background-color: #f4f6f8;
    padding: 30px;
    max-width: 800px;
    margin: auto;
  }
  h1 {
    text-align: center;
    color: #004aad;
  }
  .progress-container {
    background: #ddd;
    border-radius: 10px;
    overflow: hidden;
    margin: 20px 0;
    height: 20px;
  }
  .progress-bar {
    height: 100%;
    background: #28a745;
    width: 0%;
    transition: width 0.6s ease;
  }
  .step {
    display: flex;
    align-items: center;
    background: #fff;
    padding: 15px;
    border-radius: 10px;
    margin-bottom: 10px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  }
  .status {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    margin-right: 10px;
  }
  .done { background: #28a745; }
  .doing { background: #ffc107; }
  .todo { background: #dc3545; }
  .info {
    flex: 1;
  }
  .info p {
    margin: 3px 0;
  }
  .note {
    font-size: 0.9em;
    color: #555;
  }
</style>
</head>
<body>
  <h1>THEO DÕI TIẾN ĐỘ CÔNG TÁC BẦU CỬ CẤP XÃ</h1>

  <div class="progress-container">
    <div id="progressBar" class="progress-bar"></div>
  </div>
  <p style="text-align:center;">Tổng tiến độ: <span id="progressPercent">0%</span></p>

  <div id="steps">
    <div class="step">
      <div class="status done"></div>
      <div class="info">
        <p><b>1. Thành lập Ban Chỉ đạo công tác bầu cử</b></p>
        <p>Trạng thái: Hoàn thành</p>
        <p class="note">Ngày hoàn thành: 01/11/2025</p>
      </div>
    </div>

    <div class="step">
      <div class="status doing"></div>
      <div class="info">
        <p><b>2. Công bố ngày bầu cử</b></p>
        <p>Trạng thái: Đang thực hiện</p>
        <p class="note">Dự kiến hoàn thành: 15/11/2025</p>
      </div>
    </div>

    <div class="step">
      <div class="status todo"></div>
      <div class="info">
        <p><b>3. Hoàn tất danh sách thành phần các tổ bầu cử</b></p>
        <p>Trạng thái: Chưa bắt đầu</p>
      </div>
    </div>

    <div class="step">
      <div class="status todo"></div>
      <div class="info">
        <p><b>4. Hiệp thương lần thứ nhất</b></p>
        <p>Trạng thái: Chưa bắt đầu</p>
      </div>
    </div>

    <div class="step">
      <div class="status todo"></div>
      <div class="info">
        <p><b>5. Giới thiệu người ứng cử, tiếp nhận hồ sơ</b></p>
        <p>Trạng thái: Chưa bắt đầu</p>
      </div>
    </div>
  </div>

<script>
  // Tự tính phần trăm hoàn thành
  const steps = document.querySelectorAll(".step");
  const done = document.querySelectorAll(".done").length;
  const percent = Math.round((done / steps.length) * 100);
  ocument.getElementById("progressBar").style.width = percent + "%";
  document.getElementById("progressPercent").textContent = percent + "%";
</script>

</body>
</html>
