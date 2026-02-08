# ittmaline.<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desain & Komentar - Hadid Alfhat</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 500px;
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        /* Area Embed Canva */
        .canva-embed {
            position: relative;
            width: 100%;
            height: 0;
            padding-top: 444.4363%;
            overflow: hidden;
            border-radius: 10px;
            margin-bottom: 25px;
        }

        .canva-embed iframe {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%; border: none;
        }

        /* Area Input Komentar */
        .comment-box {
            border-top: 2px solid #eee;
            padding-top: 20px;
        }

        h3 { color: #333; font-size: 1.2rem; }

        input, textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-sizing: border-box; /* Agar padding tidak merusak lebar */
            font-family: inherit;
        }

        button {
            background-color: #0084ff;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: background 0.3s;
        }

        button:hover {
            background-color: #0066cc;
        }

        /* Daftar Komentar yang Muncul */
        #comment-list {
            margin-top: 20px;
            list-style: none;
            padding: 0;
        }

        .comment-item {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            border-left: 4px solid #0084ff;
            animation: fadeIn 0.5s ease-in;
