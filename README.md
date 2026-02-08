
HTML
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Postingan Interaktif - Canva & Komentar</title>
    <style>
      
        body {
            background-color: #f4f7f9;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
            margin: 0;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        
</head>
<body>

<div class="container">
    <div class="canva-embed">
        <iframe src="https://www.canva.com/design/PLAYHOLDER/view?embed" 
                allowfullscreen="allowfullscreen" allow="fullscreen">
        </iframe>
    </div>

  
</div>

<script>
   
    window.onload = function() {
        loadComments();
    };

    function saveComment() {
        const name = document.getElementById('nameInput').value;
        const text = document.getElementById('commentInput').value;

        if (!name || !text) {
            alert("Harap isi nama dan komentar ya!");
            return;
        }

        const newComment = {
            id: Date.now(),
            name: name,
            text: text
        };

        
        const comments = JSON.parse(localStorage.getItem('myComments') || '[]');
        comments.unshift(newComment); // Tambah ke paling atas
        localStorage.setItem('myComments', JSON.stringify(comments));

       
        document.getElementById('nameInput').value = '';
        document.getElementById('commentInput').value = '';
        loadComments();
    }

    function loadComments() {
        const list = document.getElementById('comment-list');
        const comments = JSON.parse(localStorage.getItem('myComments') || '[]');
        
        list.innerHTML = comments.map(c => `
            <div class="comment-item">
                <strong>@${c.name}</strong>
                <p>${c.text}</p>
            </div>
        `).join('');
    }
</script>

</body>
</html>
