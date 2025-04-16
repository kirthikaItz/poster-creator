# poster-creator
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1">
 <title>Poster Creator</title>
 <style>
 body {
 font-family: Arial, sans-serif;
 margin: 20px;
 background: #f4f4f4;
 }
 h1 {
 text-align: center;
 }
 .container {
 display: flex;
 flex-wrap: wrap;
 gap: 20px;
 justify-content: center;
 }
 .form-section, .poster-preview {
 flex: 1 1 300px;
 padding: 20px;
 background: white;
 border-radius: 12px;
 box-shadow: 0 4px 10px rgba(0,0,0,0.1);
 }
 input, textarea, select {
 width: 100%;
 padding: 10px;
 margin: 10px 0;
 border-radius: 6px;
 border: 1px solid #ccc;
 }
 .poster {
 height: 500px;
 border: 2px dashed #ddd;
 display: flex;
 flex-direction: column;
 justify-content: center;
 align-items: center;
 padding: 20px;
 text-align: center;
 border-radius: 12px;
 }
 .poster h2 {
 margin: 10px 0;
 font-size: 2em;
 }
 .poster h3 {
 font-size: 1.5em;
 margin-bottom: 10px;
 }
 .poster p {
 font-size: 1em;
 }
 </style>
</head>
<body>
<h1>Poster Creator</h1>
<div class="container">
 <!-- Form -->
 <div class="form-section">
 <label>Title</label>
 <input type="text" id="titleInput" placeholder="Enter title">
 <label>Subtitle</label>
 <input type="text" id="subtitleInput" placeholder="Enter subtitle">
 <label>Description</label>
 <textarea id="descInput" rows="4" placeholder="Enter description"></textarea>
 <label>Background Color</label>
 <input type="color" id="bgColorInput" value="#ffffff">
 <label>Text Color</label>
 <input type="color" id="textColorInput" value="#000000">
 </div>
 <!-- Poster Preview -->
 <div class="poster-preview">
 <div id="poster" class="poster">
 <h2 id="posterTitle">Your Title</h2>
 <h3 id="posterSubtitle">Your Subtitle</h3>
 <p id="posterDesc">Your description will appear here.</p>
 </div>
 </div>
</div>
<script>
 const titleInput = document.getElementById('titleInput');
 const subtitleInput = document.getElementById('subtitleInput');
 const descInput = document.getElementById('descInput');
 const bgColorInput = document.getElementById('bgColorInput');
 const textColorInput = document.getElementById('textColorInput');
 const poster = document.getElementById('poster');
 const posterTitle = document.getElementById('posterTitle');
 const posterSubtitle = document.getElementById('posterSubtitle');
 const posterDesc = document.getElementById('posterDesc');
 function updatePoster() {
 posterTitle.textContent = titleInput.value || 'Your Title';
 posterSubtitle.textContent = subtitleInput.value || 'Your Subtitle';
 posterDesc.textContent = descInput.value || 'Your description will appear here.';
 poster.style.backgroundColor = bgColorInput.value;
 poster.style.color = textColorInput.value;
 }
 titleInput.addEventListener('input', updatePoster);
 subtitleInput.addEventListener('input', updatePoster);
 descInput.addEventListener('input', updatePoster);
 bgColorInput.addEventListener('input', updatePoster);
 textColorInput.addEventListener('input', updatePoster);
</script>
</body>
</html>
