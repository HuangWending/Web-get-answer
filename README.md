# Web-get-answer
Web前端问答网页
<!DOCTYPE html>
<html>
<head>
    <title>问答程序</title>
</head>
<body>
这是HTML文档的基本结构，包括<!DOCTYPE html>声明、<html>根元素、<head>头部和<body>主体部分。
    <script>
这是一个JavaScript脚本的开始标签。
        // 定义问题和答案的数组
        var questions = [
            "你好",
            "你的名字是什么",
            "你的生日是什么时候",
            "你是中国人吗",
            "台湾是中国的吗",
            "你爱我吗",
            "你喜欢去哪里",
            "你有朋友吗",
            "你的心情怎么样"
        ];

        var answers = [
            "你好",
            "黄文定",
            "2009年7月18日",
            "我是中国人",
            "台湾是中国的",
            "这是一个由我决定的选项，我需要认真，但是我还是爱着你",
            "中国大陆和中国台湾",
            "没有",
            "自卑，孤独"
        ];
这部分定义了问题和答案的数组。questions数组包含了一系列问题，answers数组包含了对应的答案。
        function getAnswer(question) {
            // 将问题转换为小写
            question = question.toLowerCase();

            // 遍历问题数组，查找匹配的问题并返回对应的回答
            for (var i = 0; i < questions.length; i++) {
                if (question === questions[i]) {
                    return answers[i];
                }
            }

            // 如果没有匹配的问题，则返回默认回答
            return "抱歉，我黄文定无法回答这个问题。";
        }
这是一个名为getAnswer的函数。它接受一个问题作为输入，并返回相应的答案。该函数将问题转换为小写，然后遍历问题数组，找到匹配的问题并返回对应的答案。如果没有匹配的问题，则返回默认回答。
        function askQuestion() {
            // 获取用户输入的问题
            var question = prompt("请输入你的问题：");

            // 获取问题的回答
            var answer = getAnswer(question);

            // 显示回答
            alert(answer);
        }
这是一个名为askQuestion的函数。它提示用户输入问题，然后调用getAnswer函数获取问题的回答，并使用alert函数显示回答。
        // 调用askQuestion函数，开始问答过程
        askQuestion();
这行代码调用了askQuestion函数，开始问答过程。当页面加载完毕后，会自动弹出一个对话框，要求用户输入问题，并显示相应的回答。
