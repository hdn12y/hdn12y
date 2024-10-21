<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAPPY BIRTHDAY TO LAMLAM</title>
    <style>
        /* 設置全局樣式 */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url(background.jpg); /* 背景圖片的路徑 */
            background-size: 500px;
            background-position: center;
            background-attachment: fixed;
        }

        /* 頂部導航欄 */
        .navbar {
            background-color: rgba(255, 255, 255, 0.8); /* 半透明背景 */
            border-bottom: 1px solid #eaeaea;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .navbar div {
            font-size: 18px;
            font-weight: bold;
        }

        .navbar a {
            text-decoration: none;
            color: #333;
            margin: 0 30px;
            font-size: 16px;
            cursor: pointer;
        }

        .navbar a:hover {
            color: gray;
        }

        /* 主標題區域 */
        .header {
            text-align: center;
            padding: 40px 0;
        }

        .header h1 {
            font-size: 32px;
            color: rgb(59, 59, 199);
            margin-bottom: 10px;
        }

        .header p {
            font-size: 18px;
            color: rgb(59, 59, 199);
        }

        /* 卡片佈局 */
        .card-container {
            background-color: rgba(255, 255, 255, 0.8); /* 半透明背景 */
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .card {
            background-color: rgba(255, 255, 255, 0.8); /* 半透明背景 */
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
        }

        .card img {
            width: 40px;
            height: 40px;
            margin-bottom: 10px;
        }

        .card h3 {
            font-size: 20px;
            color: #333;
            margin-bottom: 10px;
        }

        .card p {
            font-size: 16px;
            color: #777;
        }

          /* 滑動卡片佈局 */
        .scroll-container {
            display: flex;
            overflow-x: scroll;
            gap: 20px;
            scroll-snap-type: x mandatory;
            padding: 20px;
        }

        .scroll-card {
            background-color: rgba(255, 255, 255, 0.8);
            scroll-snap-align: start;
            flex: 0 0 400px;
            height: 500px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .scroll-card:hover {
            transform: scale(1.1);
        }

        .scroll-card img {
            width: 40px;
            height: 40px;
            margin-bottom: 10px;
        }

        .scroll-card img[src="1st.png"] {
            width: 150px;  /* Adjust the width as needed */
            height: auto;  /* Keep aspect ratio */
            max-width: 100%;  /* Ensure it doesn't overflow the container */
            object-fit: contain;  /* Prevent distortion */
        }

        .scroll-card img[src="2nd.jpg"] {
            width: 150px;  /* Adjust the width as needed */
            height: auto;  /* Maintain aspect ratio */
            max-width: 100%;  /* Prevent the image from overflowing the card */
            object-fit: contain;  /* Ensure the image does not get distorted */
        }

        .scroll-card img[src="3rd.jpg"] {
            width: 165px;  /* Adjust the width as needed */
            height: auto;  /* Maintain aspect ratio */
            max-width: 100%;  /* Prevent the image from overflowing the card */
            object-fit: contain;  /* Ensure the image does not get distorted */
        }


        
        /* 隱藏內容區 */
        .content-section {
            display: none;
            text-align: center;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8); 
            margin: 20px 0;
            border: 1px solid #eaeaea;
        }

        /* 顯示內容區 */
        .active {
            display: block;
        }

        audio {
        position: fixed;
        bottom: 20px; /* 距離頁面底部20px */
        right: 20px;  /* 距離頁面右側20px */
        z-index: 1000; /* 保證播放器在最上層 */
    }
    </style>

    <script>
        // JavaScript 函數，用於切換內容顯示
        function showContent(sectionId) {
            // 隱藏所有內容區
            var sections = document.querySelectorAll('.content-section');
            sections.forEach(function(section) {
                section.classList.remove('active');
            });

            // 顯示點擊的內容區
            document.getElementById(sectionId).classList.add('active');
        }
            // 背景音樂
        function playMusic() {
        var audio = document.getElementById('backgroundMusic');
        audio.play();
    }
    </script>
    
</head>
<body>

    <!-- 背景音樂 -->
    <audio controls="controls" >
        <source src="陳蕾 Panther Chan - 念 Light In Your Heart (Official Lyric Video).mp3" type="audio/mp3">
        <source src="陳蕾 Panther Chan - 念 Light In Your Heart (Official Lyric Video).mp3" type="audio/wav">
    </audio>


    <!-- 導航欄 -->
    <div class="navbar">
        <div>送給21嵗的LAM</div>
        <div>
            <a onclick="showContent('home')">首頁</a>
            <a onclick="showContent('about')">關於我們</a>
            <a onclick="showContent('beautiful')">我眼中的LAMLAM</a>
            <a onclick="showContent('message')">想對你說的話</a>
            <a onclick="showContent('ramblings')">關於這個網頁</a>
        </div>
    </div>

    <!-- 主標題 -->
    <div class="header">
        <h1>HAPPY BIRTHDAY TO LAMLAM</h1>
        <p>生日快樂 歲數只是一個僞命題 祝你永遠不受年齡限制 永遠快樂自由做自己</p>
    </div>

    <!-- 內容區塊 -->
    <div id="home" class="content-section active">
        <h2>希望你新的一嵗</h2>
        <p>身心健康 心想事成</p>
        <p>你的快樂比一切重要</p>
        <p>生日快樂！開心萬歲! ♥</p>

    </div>

    <div id="about" class="content-section">
        <h2>我們的故事</h2>
        <div class="scroll-container">
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>開始</h3>
                <p>我們第一次見面是在番禺 記不記得第一次見面我還遲到了哈哈(不可抗力)</p>
                <p>上車之後覺得你好局促啊 我有努力帶動一下氣氛的</p>
                <p>但是好像話太多 讓你更尷尬了哈哈</p>
                <img src="1st.png">
            </div>
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>惠州</h3>
                <p>跟住我們就去了惠州衝浪啦</p>
                <p>真心覺得你好勁!居然試兩三次就企到起身啦!</p>
                <p>燒烤都好勁!腸仔勁好食!</p>
                <p>同埋當時的你很不開心 每天的眼都是腫的</p>
                <p>想你開心的種子應該是那個時候種下的</p>
                <img src="2nd.jpg" >
            </div>
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>廣州</h3>
                <p>你來廣州之後我們正式開始了我們的友誼</p>
                <p>電雞揾食,livehouse,廣場舞,夜爬白雲山,打機...</p>
                <p>一起嘻嘻哈哈吃喝玩樂忘掉煩惱</p>
                <p>那段時間的所有事情到現在想起也是覺得快樂的存在 很高興認識你 你真的很棒</p>
                <img src="3rd.jpg">
            </div>
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>香港</h3>
                <p>有幸參與了你的20嵗</p>
            </div>
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>雲南</h3>
                <p>救命 雲南的粉真的太好吃啦</p>
            </div>
            <div class="scroll-card">
                <img src="frog icon.png" alt="icon">
                <h3>廣州</h3>
                <p>情人節</p>
            </div>
        </div>
    </div>

    <div id="beautiful" class="content-section">
        <h2>完美這個詞似乎是爲你量身訂造的</h2>
        <p>人美心善 上帝最滿意的作品 人間最完美的存在</p>
        <div class="card-container">
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>聰明</h3>
                <p>第一印象就覺得這個人一定很聰明</p>
                <p>眼睛大大圓碌碌的</p>
                <p>相處下來確實很聰明 很有創意 很精靈鬼馬</p>
                <p>很多東西你都能舉一反三</p>
                <p>好多位都覺得你轉數好快</p>
                <p>尤其玩游戲 跟住你實冇得輸</p>
            </div>
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>細膩</h3>
                <p>理智又感性 情感很細膩的一個人</p>
                <p>會爲電影裏的情節而落淚</p>
                <p>會為美景而發自内心的笑</p>
                <p>愛小動物 愛大自然 會用心觀察這個世界</p>
                <p>喜歡用相機和文字記錄下日常</p>
                <p>情感十分細膩的小女孩</p>
            </div>
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>可愛</h3>
                <p>不得不説你真的很可愛</p>
                <p>名字可愛 lamlam</p>
                <p>説話可愛 很溫柔</p>
                <p>長得可愛 很柔和的面相</p>
                <p>第一眼會覺得是個沒有距離感而且一定很善良沒有壞心思的人</p>
            </div>
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>可靠</h3>
                <p>可愛不代表柔弱 相反十分可靠</p>
                <p>你很會照顧別人的感受 洞察能力很强</p>
                <p>我覺得關鍵時刻你是能帶領一隊人走出困境的那個人</p>
                <p>有觀點有見地 面對困境總能提出一個一陣見血的堅決方案</p>
                <p>有你在就很安心</p>
            </div>
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>爲食</h3>
                <p>哈哈爲食貓</p>
                <p>你是我第一個認識會用心品嘗食物的人</p>
                <p>有品味 對食物有要求</p>
                <p>每次見到你發自内心不自覺的笑我就知呢樣野一定好好食</p>
                <p>美食家本家 可以盲跟你的推薦</p>
                <p>有冇考慮過做美食博主</p>
            </div>
            <div class="card">
                <img src="Eyes Emoji PNG.jpg" alt="icon">
                <h3>頑强</h3>
                <p>這絕對是個褒義詞</p>
                <p>你給我的感覺是雖然看著可能很穨</p>
                <p>或者看著很痛苦很想放棄</p>
                <p>盡管如此 你從來都沒有放棄過 頂著壓力不斷往前衝</p>
                <p>其實你的内心非常强大 你有非常頑强的生命力</p>
                <p>你不會輕易放棄一件事的精神和總能做到絕處逢生是最令我敬佩的</p>
            </div>
        </div>
    </div>


    <div id="message" class="content-section">
        <h2>想對你說</h2>
        <p>祝你不止生日快樂 祝你天天快樂</p>
        <p>新的一歲 心想事成 身心健康 早日發達 （雖然很老土 但最實際!) </p>
        <p>你一定會成爲你想成爲的人的</p>
        <p>但這個過程請你一定要多愛自己一點一定要開心</p>
        <p>你的感受比對錯重要 你的感受應該放在頭位</p>
        <p>傷害到你</p><h4>對不起</h4>
        <p>過去一段時間我都在反思自責 我知對不起沒用</p>
        <p>但還是懇求你的原諒</p>
        <p>能做你的朋友真的很幸運</p>
        <p>我還有機會繼續做你的朋友嗎</p>
        <p>我們可以保持聯絡嗎</p>
    </div>

    <div id="ramblings" class="content-section">
        <h2>碎碎念</h2>
        <p>這裏是小黃的碎碎念和這個網頁誕生的理由:)好囉嗦啊我哈哈</p>
        <video width="600" controls>
            <source src="9up.mp4" type="video/mp4">
            <source src="9up.mp4" type="video/ogg">
        </video>
    </div>
    
</body>
</html>
 
