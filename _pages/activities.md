---
layout: default
title: Activities
---

<style>
.project {
    width:280px;
    height:200px;
    margin:10px;
    padding:0px;
    position:relative;
    display:inline-block;
    text-align:left;
}

.overlay {
	width:100%;
    height:100%;
    position:absolute;
    top:0;
    left:0;
    display:inline-block;
    -webkit-box-sizing:border-box;
    -moz-box-sizing:border-box;
    box-sizing:border-box;
    color:white;
}

.overlay_title {
    font-size:1.25em;
    background:rgba(0,0,0,0.7);
    padding:7px;
}
/*
.overlay_description {
    font-size:1.1em;
    background:rgba(0,0,0,0.7);
    margin-top:0px;
    padding:4px;
    width: 100%;
    border-top: 1px solid rgba(255,255,255,0.45);
}*/
.overlay_summary {
    font-size:0.95em;
    background:rgba(0,0,0,0.7);
    display: none;
    margin-top:8px;
    /*padding:10px;*/
    width: 100%;
}
.project a:hover .overlay_summary {
    display:inline-block;
}
.overlay .overlay_summary li {
    padding:2px;
}



#platforms {
	margin-top:10px;
	margin-bottom:20px;
}
.platform {
	border: 1px solid #aaa;
	padding-bottom: 8px;
	padding-top: 8px;
	padding-left: 24px;
	padding-right: 24px;
	margin: 2px;
	display:inline-block;
}

</style>



<div id="platforms">
	<div id="platform_all" class="platform"><a href="javascript:displayAll();">All</a></div>
	<div id="platform_python" class="platform"><a href="javascript:displayByKey('python');"></a></div>
	<div id="platform_openframeworks" class="platform"><a href="javascript:displayByKey('openframeworks');"></a></div>
</div>




{% include guide_preview.md name="blaxtarlines01" %}







<script>


function highlightButton(keyword){
	document.getElementById("platform_python").style.border = "none";
	document.getElementById("platform_openframeworks").style.border = "none";
	document.getElementById("platform_all").style.border = "none";
	document.getElementById("platform_"+keyword).style.border = "1px solid #1abc9c";
}
function displayAll() {
	var d = document.getElementsByClassName("project");
	for(var i = 0; i < d.length; i++){ d[i].style.display = "inline-block"; }
	highlightButton('all');
};
function hideAll() {
	var d = document.getElementsByClassName("project");
	for(var i = 0; i < d.length; i++){ d[i].style.display = "none"; }	
};
function displayByKey(keyword) {
	hideAll();
	d = document.getElementsByClassName("project "+keyword);
	for(var i = 0; i < d.length; i++){ d[i].style.display = "inline-block"; }
	highlightButton(keyword);
};
displayAll();

</script>