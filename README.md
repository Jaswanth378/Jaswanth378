<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LinkedIn Banner - Jaswanth Kattubavi</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: #f0f2f5;
        }

        .banner-container {
            width: 1584px;
            height: 396px;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f172a 100%);
            animation: gradientShift 15s ease infinite;
        }

        @keyframes gradientShift {

            0%,
            100% {
                background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f172a 100%);
            }

            50% {
                background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #0a0e27 100%);
            }
        }

        /* Animated circuit board pattern */
        .circuit-pattern {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            background-image:
                linear-gradient(90deg, #00ffff 1px, transparent 1px),
                linear-gradient(180deg, #00ffff 1px, transparent 1px);
            background-size: 50px 50px;
            animation: circuitMove 20s linear infinite;
        }

        @keyframes circuitMove {
            0% {
                transform: translate(0, 0);
            }

            100% {
                transform: translate(50px, 50px);
            }
        }

        /* Floating particles */
        .particles {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .particle {
            position: absolute;
            background: radial-gradient(circle, rgba(0, 255, 255, 0.8) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 15s infinite ease-in-out;
        }

        @keyframes float {

            0%,
            100% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }

            10% {
                opacity: 1;
            }

            90% {
                opacity: 1;
            }

            100% {
                transform: translateY(-100px) translateX(100px);
                opacity: 0;
            }
        }

        .particle:nth-child(1) {
            width: 4px;
            height: 4px;
            left: 10%;
            top: 80%;
            animation-delay: 0s;
        }

        .particle:nth-child(2) {
            width: 6px;
            height: 6px;
            left: 30%;
            top: 70%;
            animation-delay: 2s;
        }

        .particle:nth-child(3) {
            width: 3px;
            height: 3px;
            left: 50%;
            top: 90%;
            animation-delay: 4s;
        }

        .particle:nth-child(4) {
            width: 5px;
            height: 5px;
            left: 70%;
            top: 60%;
            animation-delay: 6s;
        }

        .particle:nth-child(5) {
            width: 4px;
            height: 4px;
            left: 90%;
            top: 85%;
            animation-delay: 8s;
        }

        /* Main content */
        .content {
            position: relative;
            z-index: 10;
            height: 100%;
            display: flex;
            align-items: center;
            padding: 0 80px;
        }

        .left-section {
            flex: 1;
            max-width: 600px;
        }

        .name {
            font-size: 56px;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: -15px;
            letter-spacing: -1px;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .title {
            font-size: 24px;
            color: #00ffff;
            margin-bottom: 10px;
            font-weight: 400;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .specialties {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .specialty {
            padding: 8px 16px;
            background: rgba(0, 255, 255, 0.1);
            border: 1px solid rgba(0, 255, 255, 0.3);
            border-radius: 20px;
            color: #ffffff;
            font-size: 14px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .specialty::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .specialty:hover::before {
            left: 100%;
        }

        .specialty:hover {
            background: rgba(0, 255, 255, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 255, 255, 0.3);
        }


        /* Decorative elements */
        .code-snippet {
            position: absolute;
            left: 60px;
            bottom: 40px;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            color: rgba(0, 255, 255, 0.4);
            opacity: 0.6;
            animation: fadeIn 2s ease-out 1s both;
        }

        .geometric-shape {
            position: absolute;
            width: 100px;
            height: 100px;
            right: 100px;
            bottom: 50px;
            opacity: 0.1;
        }

        .geometric-shape::before,
        .geometric-shape::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            border: 2px solid #00ffff;
            border-radius: 10px;
            animation: rotateShape 20s linear infinite;
        }

        .geometric-shape::after {
            animation-delay: -10s;
            animation-direction: reverse;
        }

        @keyframes rotateShape {
            0% {
                transform: rotate(0deg) scale(1);
            }

            50% {
                transform: rotate(180deg) scale(1.2);
            }

            100% {
                transform: rotate(360deg) scale(1);
            }
        }
    </style>
</head>

<body>
    <div class="banner-container">
        <!-- Background effects -->
        <div class="circuit-pattern"></div>
        <div class="particles">
            <div class="particle"></div>
            <div class="particle"></div>
            <div class="particle"></div>
            <div class="particle"></div>
            <div class="particle"></div>
        </div>

        <!-- Main content -->
        <div class="content">
            <div class="left-section">
                <h1 class="name">Jaswanth Kattubavi</h1>
                <p class="title">Software Engineer</p>
                <div class="specialties">
                    <span class="specialty">Python</span>
                    <span class="specialty">AWS</span>
                    <span class="specialty">SQL</span>
                    <span class="specialty">Data Science</span>
                    <span class="specialty">ML</span>
                    <span class="specialty">Django</span>
                    <span class="specialty">Flask</span>
                    <span class="specialty">.Net Framework</span>
                    <span class="specialty">TensorFlow</span>
                    <span class="specialty">MySQL</span>
                    <span class="specialty">RESTful APi's</span>
                    <span class="specialty">CI/CD</span>
                    <span class="specialty">Git</span>
                    <span class="specialty">OOP</span>
                    <span class="specialty">JavaScript</span>
                    <span class="specialty">HTML</span>
                    <span class="specialty">CSS</span>
                </div>
            </div>


        </div>

        <!-- Code snippet decoration -->
        <div class="code-snippet">
            def innovate():<br>
            &nbsp;&nbsp;return "Building the future"
        </div>

        <!-- Geometric decoration -->
        <div class="geometric-shape"></div>
    </div>

    <!-- Download instruction -->
    <div
        style="text-align: center; margin-top: 30px; padding: 20px; background: white; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1);">
        <h3 style="margin-bottom: 15px; color: #333;">How to Save Your Banner:</h3>
        <ol style="text-align: left; max-width: 600px; margin: 0 auto; color: #666;">
            <li>Right-click on the banner above</li>
            <li>Select "Save image as..." or take a screenshot</li>
            <li>Upload to LinkedIn: Profile → Edit → Background photo</li>
        </ol>
        <p style="margin-top: 15px; color: #999; font-size: 14px;">
            Recommended LinkedIn banner size: 1584 x 396 pixels
        </p>
    </div>
</body>

</html>

Feel free to connect with me or check out my projects!

- **Email**: [jaswanthkattubavis@gmail.com](mailto:jaswanthkattubavis@gmail.com) 📧
- **LinkedIn**: [Jaswanth Kattubavi](https://linkedin.com/in/jaswanth-kattubavi) 🔗
- **Twitter**: [@jaswanth378](https://twitter.com/jaswanth378) 🐦
