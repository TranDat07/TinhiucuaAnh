
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tình iu của em</title>
    <link rel="stylesheet" href="1.css" />
  </head>
  <body>
    <div class="wrapper">
      <h1 class="question">Ngoài em raa anhh còn cô nào khác hay khôngg?<br><span style="font-style: italic; font-size: 67%;">Anh mà không chọn mà thoát ra thì đừng nhìn mặt em nữa🙂</span></h1>


      <img
        class="gif"
        alt="gif"
        src="https://media.giphy.com/media/2weSkZg9hvQW5Zv2fk/giphy.gif"
      />
      <div class="btn-group">
        <button class="yes-btn">Có Nhìu lắm</button>
        <button class="no-btn">Chỉ có em</button>
        
      </div>
      <p class="additional-message" style="display:none;">Dòng chữ mới không xuất hiện khi ấn vào có nhìu lắm</p>
    </div>
    <script src="1.js"></script>
  </body>
</html>

const wrapper = document.querySelector(".wrapper");
const question = document.querySelector(".question");
const gif = document.querySelector(".gif");
const yesBtn = document.querySelector(".yes-btn");
const noBtn = document.querySelector(".no-btn");
const additionalMessage = document.querySelector(".additional-message");

yesBtn.addEventListener("click", () => {
  question.innerHTML = "Tới công chuyện với bà mày rồi =)))))";
  gif.src =
    "https://media.giphy.com/media/MFkTITj69pMOPlbfeX/giphy.gif";
  // Ẩn cả hai nút "Yes" và "No"
  yesBtn.style.display = "none";
  noBtn.style.display = "none";
});

noBtn.addEventListener("mouseover", () => {
  const noBtnRect = noBtn.getBoundingClientRect();
  const maxX = window.innerWidth - noBtnRect.width;
  const maxY = window.innerHeight - noBtnRect.height;

  const randomX = Math.floor(Math.random() * maxX);
  const randomY = Math.floor(Math.random() * maxY);

  noBtn.style.left = randomX + "px";
  noBtn.style.top = randomY + "px";
});
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: rgb(243, 225, 237);
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  
  .gif {
    height: 70%;
    width: 70%;
  }
  
  h1{
    text-align: center;
    font-size: 1.7em;
    color: #e94d58;
    margin: 15px 0;
  }
  .btn-group {
    width: 100%;
    height: 50px;
    display: flex;
    justify-content: center;
    margin-top: 50px;
  }
  button {
    position: absolute;
    width: 150px;
    height: inherit;
    color: rgb(235, 229, 229);
    font-size: 1.2em;
    border-radius: 30px;
    outline: none;
    cursor: pointer;
    box-shadow: 0 2px 4px gray;
    border: 2px solid #c0d6e4;
    font-size: 1.2em;
  }
  button:nth-child(1) {
    margin-left: -200px;
    background: #e26878;
  }
  button:nth-child(2) {
    margin-right: -200px;
    background: rgb(235, 224, 224);
    color: #e22242;
  }
