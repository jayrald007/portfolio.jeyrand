
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jayrald Angeles Lopez | Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #0f172a;
            color: white;
        }

        header {
            background: #1e293b;
            padding: 20px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
        }

        header h2 {
            color: #38bdf8;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
        }

        nav a:hover {
            color: #38bdf8;
        }

        section {
            padding: 80px 10%;
            min-height: 50vh;
        }

        .home {
            text-align: center;
            padding-top: 130px;
            min-height: 85vh;
        }

        .home h1 {
            font-size: 42px;
            color: #38bdf8;
            margin-bottom: 15px;
        }

        .home p {
            font-size: 20px;
            margin-bottom: 20px;
        }

        .btn {
            display: inline-block;
            background: #38bdf8;
            color: #0f172a;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
        }

        h2 {
            color: #38bdf8;
            margin-bottom: 25px;
            text-align: center;
        }

        .about, .project {
            background: #1e293b;
            border-radius: 15px;
            padding: 35px;
            margin-bottom: 20px;
            line-height: 1.8;
        }

        .project {
            text-align: center;
        }

        .project button {
            padding: 12px 20px;
            background: #38bdf8;
            border: none;
            border-radius: 7px;
            cursor: pointer;
            margin-top: 15px;
            font-weight: bold;
        }

        footer {
            background: #1e293b;
            text-align: center;
            padding: 20px;
            color: #cbd5e1;
        }

        /* Calculator */
        .calculator {
            background: #1e293b;
            max-width: 330px;
            margin: 25px auto;
            padding: 20px;
            border-radius: 15px;
        }

        #display {
            width: 100%;
            height: 60px;
            font-size: 25px;
            text-align: right;
            padding: 10px;
            margin-bottom: 15px;
            border: none;
            border-radius: 8px;
        }

        .keys {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        .keys button {
            height: 55px;
            font-size: 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            background: #334155;
            color: white;
        }

        .keys button:hover {
            background: #475569;
        }

        .keys .operator {
            background: #0284c7;
        }

        .keys .equal {
            background: #16a34a;
        }

        .keys .clear {
            background: #dc2626;
        }

        @media(max-width: 600px) {
            header {
                flex-direction: column;
                gap: 15px;
            }

            nav a {
                margin: 5px;
                font-size: 13px;
            }

            .home h1 {
                font-size: 30px;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->
    <header>
        <h2>My Portfolio</h2>

        <nav>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#calculator">Calculator</a>
        </nav>
    </header>

    <!-- Home -->
    <section class="home" id="home">
        <h1>Hello, I'm Jayrald Angeles Lopez!</h1>
        <p>BSIT 1C Student</p>
        <p>Welcome to my Personal Portfolio Website.</p>

        <a href="#about" class="btn">Explore My Portfolio</a>
    </section>

    <!-- About Me -->
    <section id="about">
        <h2>ABOUT ME</h2>

        <div class="about">
            <p>
                Hello! My name is <b>Jayrald Angeles Lopez</b>.
                I am a first-year Bachelor of Science in Information
                Technology student from <b>BSIT 1C</b>.
            </p>

            <p>
                I am interested in technology, computers, and
                programming. I enjoy learning new skills and
                discovering how websites and applications work.
            </p>

            <p>
                My goal is to improve my programming knowledge,
                develop useful applications, and become a
                successful IT professional in the future.
            </p>
        </div>
    </section>

    <!-- My Projects -->
    <section id="projects">
        <h2>MY WORK / PROJECTS</h2>

        <div class="project">
            <h3>My Calculator App</h3>

            <p>
                This is my first calculator project using
                HTML, CSS, and JavaScript. It can perform
                basic mathematical operations such as
                addition, subtraction, multiplication,
                and division.
            </p>

            <a href="#calculator" class="btn">
                View Calculator
            </a>
        </div>
    </section>

    <!-- Calculator -->
    <section id="calculator">
        <h2>MY CALCULATOR</h2>

        <div class="calculator">

            <input type="text" id="display"
                   placeholder="0" readonly>

            <div class="keys">
                <button class="clear" onclick="clearDisplay()">AC</button>
                <button onclick="deleteNumber()">DEL</button>
                <button class="operator" onclick="append('/')">÷</button>
                <button class="operator" onclick="append('*')">×</button>

                <button onclick="append('7')">7</button>
                <button onclick="append('8')">8</button>
                <button onclick="append('9')">9</button>
                <button class="operator" onclick="append('-')">-</button>

                <button onclick="append('4')">4</button>
                <button onclick="append('5')">5</button>
                <button onclick="append('6')">6</button>
                <button class="operator" onclick="append('+')">+</button>

                <button onclick="append('1')">1</button>
                <button onclick="append('2')">2</button>
                <button onclick="append('3')">3</button>
                <button class="equal" onclick="calculate()">=</button>

                <button onclick="append('0')">0</button>
                <button onclick="append('.')">.</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2026 Jayrald Angeles Lopez</p>
        <p>BSIT 1C | Personal Portfolio</p>
    </footer>

    <!-- JavaScript -->
    <script>
        const display = document.getElementById("display");

        function append(value) {
            display.value += value;
        }

        function clearDisplay() {
            display.value = "";
        }

        function deleteNumber() {
            display.value = display.value.slice(0, -1);
        }

        function calculate() {
            try {
                const expression = display.value;

                if (!expression ||
                    !/^[0-9+\-*/.() ]+$/.test(expression)) {
                    throw new Error("Invalid input");
                }

                const result = Function(
                    '"use strict"; return (' + expression + ')'
                )();

                if (!Number.isFinite(result)) {
                    throw new Error("Invalid calculation");
                }

                display.value = result;
            } catch {
                display.value = "Error";
            }
        }
    </script>

</body>
</html>
