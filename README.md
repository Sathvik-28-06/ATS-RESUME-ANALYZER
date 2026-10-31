
/* General page styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    font-family: 'Poppins', sans-serif;
    color: #ffffff;

    background: linear-gradient(
        -45deg,
        #1f1c2c,
        #494568,
        #0f2027,
        #2c5364
    );
    background-size: 400% 400%;
    animation: gradientMove 10s ease infinite;
}

/* Animated gradient background */
@keyframes gradientMove {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

/* Main container */
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 40px 20px;
    margin: 40px auto;
    width: 100%;
}

/* Main heading */
h1 {
    text-align: center;
    font-size: 32px;
    margin-bottom: 25px;
    color: #ffffff;
}

/* Upload and result boxes */
.upload-box,
.result-box {
    width: 100%;
    max-width: 400px;
    padding: 25px;
    margin-bottom: 25px;
    text-align: center;

    background: rgba(255, 255, 255, 0.08);
    border: 1px solid rgba(255, 255, 255, 0.15);
    border-radius: 16px;

    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);

    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
}

/* Box headings */
.upload-box h2,
.result-box h2 {
    margin-bottom: 15px;
    font-size: 22px;
}

/* Input fields */
input,
select,
textarea {
    display: block;
    width: 100%;
    padding: 12px;
    margin: 12px 0;

    background: rgba(15, 20, 30, 0.85);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 8px;

    color: #ffffff;
    font-family: inherit;
    font-size: 14px;
}

/* File input */
input[type="file"] {
    padding: 10px;
    cursor: pointer;
}

/* Input focus */
input:focus,
select:focus,
textarea:focus {
    outline: none;
    border-color: #00adb5;
    box-shadow: 0 0 8px rgba(0, 173, 181, 0.4);
}

/* Buttons */
button {
    display: block;
    width: 100%;
    padding: 12px;
    margin-top: 12px;

    background: #00adb5;
    border: none;
    border-radius: 8px;

    color: #ffffff;
    font-family: inherit;
    font-size: 16px;
    font-weight: 600;

    cursor: pointer;
    transition: background 0.3s ease,
                transform 0.2s ease;
}

/* Button hover effect */
button:hover {
    background: #019ca3;
    transform: translateY(-2px);
}

/* Result text */
.result-box p {
    margin: 10px 0;
    line-height: 1.6;
    overflow-wrap: anywhere;
}

/* Score highlight */
.score {
    color: #00e5cc;
    font-size: 28px;
    font-weight: bold;
}

/* Mobile responsive design */
@media (max-width: 480px) {
    .container {
        padding: 20px 15px;
        margin: 20px auto;
    }

    h1 {
        font-size: 25px;
    }

    .upload-box,
    .result-box {
        padding: 20px;
    }
}

/* Accessibility: reduce animation when requested */
@media (prefers-reduced-motion: reduce) {
    body {
        animation: none;
    }

    button {
        transition: none;
    }
}
