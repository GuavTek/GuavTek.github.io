<html>
 <h1> Top Text </h1>
 
 <p> 
Personal project display incoming maybe
</p>

<div style="width:90%">
 <button type="button" style="width:30%" onclick="changeContent('GameDev/GameDev.html')"> Game Development </button>
 <button type="button" style="width:30%" onclick="changeContent('Synth/Synthesizer.html')"> Synthesizer </button>
 <button type="button" style="width:30%" onclick="changeContent('Electronics/Electronics.html')"> Electronics </button>
 <a href="https://GuavTek.github.io/testing">
  <button type="button" style="width:30%"> Testing </button>
 </a>
</div>

<div id="content">  </div>

<p> Bottom text </p>

<script>
async function changeContent(page) {
  const contentDiv = document.getElementById("content");
 contentDiv.innerHTML = await fetch(page);
}  
 
async function fetchHtmlAsText(url) {
    return await (await fetch(url)).text();
}
</script>

</html>
