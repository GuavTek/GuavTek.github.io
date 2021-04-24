<html>
 <h1> Top Text </h1>
 
 <p> 
Personal project display incoming maybe
</p>

<p>
<a href="https://GuavTek.github.io/testing"> testing sub-repositories </a>
</p>

<div style="width:90%">
 <button type="button" style="width:45%" onclick="changeContent('GameDev.html')"> wot </button>
 <button type="button" style="width:45%" onclick="changeContent('Synthesizer.html')"> wat </button>
</div>

<div id="content">  </div>

<p> Bottom text </p>

<script>
async function changeContent(page) {
  const contentDiv = document.getElementById("content");
 contentDiv.innerHTML = await fetchHtmlAsText(page);
}  
 
async function fetchHtmlAsText(url) {
    return await (await fetch(url)).text();
}
</script>

</html>
