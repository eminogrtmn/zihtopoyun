<!DOCTYPE html>
<html>
<head>
    <title>Zihinden Toplama Oyunu</title>
    <script>
        function yeniSoru() {
            let num1 = Math.random() < 0.5 ? 9 : 10;
            let num2 = Math.floor(Math.random() * 10);
            document.getElementById("soru").innerText = num1 + " + " + num2 + " = ?";
            document.getElementById("cevap").value = "";
            document.getElementById("dogruCevap").value = num1 + num2;
        }

        function kontrolEt() {
            let girilenCevap = document.getElementById("cevap").value;
            let dogruCevap = document.getElementById("dogruCevap").value;
            
            if (girilenCevap == dogruCevap) {
                alert("Tebrikler! Doğru cevap.");
            } else {
                alert("Yanlış! Doğru cevap: " + dogruCevap);
            }
            yeniSoru();
        }
    </script>
</head>
<body onload="yeniSoru()">
    <h2>Zihinden Toplama Oyunu</h2>
    <p id="soru"></p>
    <input type="number" id="cevap">
    <input type="hidden" id="dogruCevap">
    <button onclick="kontrolEt()">Cevabı Kontrol Et</button>
</body>
</html>
