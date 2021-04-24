<html>
Personal project display incoming maybe

<a href="https://GuavTek.github.io/testing"> testing sub-repositories </a>

 <button type="button" onclick="changeContent()"> wot </button>

<div id="content">  </div>

<script>
async function changeContent() {
  const contentDiv = document.getElementById("content");
 contentDiv.innerHTML = await fetchHtmlAsText("GameDev.html");
}  
 
async function fetchHtmlAsText(url) {
    return await (await fetch(url)).text();
}
</script>

</html>
