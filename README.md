<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thử Thách TikTok Xanh</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #d4edda; }
        .container { max-width: 600px; margin: 50px auto; padding: 20px; background: white; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); }
        h1 { color: #28a745; }
        .question { font-size: 18px; margin: 20px 0; }
        input { padding: 10px; width: 80%; margin-bottom: 10px; }
        button { padding: 10px 20px; background: #28a745; color: white; border: none; cursor: pointer; }
        button:hover { background: #218838; }
        .result { margin-top: 20px; font-weight: bold; }
        .tiktok-link { color: #007bff; text-decoration: none; font-weight: bold; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Thử Thách TikTok Xanh 🎉</h1>
        <p><a class="tiktok-link" href="https://www.tiktok.com/@clb_xanh.hcmus?_t=ZS-8v3nK9pBqSu&_r=1" target="_blank">🔗 Xem TikTok CLB Xanh tại đây!</a></p>
        <p class="question" id="question"></p>
        <input type="text" id="answer" placeholder="Nhập câu trả lời...">
        <button onclick="checkAnswer()">Trả lời</button>
        <p class="result" id="result"></p>
    </div>

    <script>
        const questions = [
            { q: "Video TikTok gần đây nhất của CLB Xanh nói về chủ đề gì?", a: "tái chế" },
            { q: "Trong video ngày 20/03, CLB Xanh đã thực hiện hành động gì?", a: "nhặt rác" },
            { q: "Câu slogan xuất hiện ở cuối video là gì?", a: "sống xanh cùng nhau" }
        ];

        let currentQuestion = 0;
        document.getElementById("question").innerText = questions[currentQuestion].q;

        function checkAnswer() {
            let answer = document.getElementById("answer").value.trim().toLowerCase();
            if (answer === questions[currentQuestion].a) {
                currentQuestion++;
                if (currentQuestion < questions.length) {
                    document.getElementById("question").innerText = questions[currentQuestion].q;
                    document.getElementById("answer").value = "";
                    document.getElementById("result").innerText = "✅ Đúng! Tiếp tục nào!";
                } else {
                    document.getElementById("result").innerHTML = "🎉 Chúc mừng! Bạn đã hoàn thành Thử Thách TikTok Xanh! Hãy comment 'Mật mã Xanh' trên TikTok CLB Xanh để nhận quà!";
                    document.getElementById("answer").style.display = "none";
                    document.querySelector("button").style.display = "none";
                }
            } else {
                document.getElementById("result").innerText = "❌ Sai rồi! Hãy xem lại video TikTok của CLB để tìm câu trả lời!";
            }
        }
    </script>
</body>
</html>
