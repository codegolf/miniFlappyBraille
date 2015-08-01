# miniFlappyBraille

a clone of http://flappybraille.ndre.gr/ golfed by @xem, @ilesinge, @aemkei, @subzey, @p01, ...

- Look at the URL.
- Play with arrows up and down.

demo 1 (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

source code

````
obstacles = [suffix = ""];

for(pos = frame = score = obstacle = i = 0; i < 999; i++){
    suffix += "  " + "⡆⡅⡃⠇"[obstacles[i] = 4 * Math.random() | 0];
}

onkeyup = function(e){
    pos += e.keyCode - 39;
    if(pos < 0) pos = 0;
    if(pos > 3) pos = 3;
}

s = setInterval(function(){

	// obstacle
	if(frame > 3 && !(frame % 30)){
    
		// pass
		if(obstacles[obstacle++] == pos){
			prefix = "⡇";
			score++;
		}
        
		// fail
		else {
			clearInterval(s);
			alert("☠" + score);
		}
	}
    
	// no obstacle
	else prefix = "⠁⠂⠄⡀"[pos];
    
	// draw current frame
    history.replaceState(0,0,"# "+(prefix + suffix.slice(frame++ / 10)).slice(0,99));
}, 30);
````

demo 2 (golfed, dirtier, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (213b / 197 chars)

````
b=[c=""];for(d=e=f=g=i=0;99>i;)c+="  "+"⡆⡅⡃⠇"[b[i++]=4*Math.random()|0];onkeyup=a=>d+=a.which-39;setInterval('3<e&&!(e%27)?i&&b[g++]==d?f++:i=0:h="⠈⠐⠠⢀"[d];location.hash=i?[h]+c.slice(e++/9):f',27)
````

demo 3 (golfed and obfuscated in braille): http://codegolf.github.io/miniFlappyBraille/index.min.braille.html

source code (758b / 282 chars)

````
eval(unescape(escape("⡢⠽⡛⡣⠽⠢⠢⡝⠻⡦⡯⡲⠨⡤⠽⡥⠽⡦⠽⡧⠽⡩⠽⠰⠻⠹⠹⠾⡩⠻⠩⡣⠫⠽⠢⠠⠠⠢⠫⠢⡜⡵⠲⠸⠴⠶⡜⡵⠲⠸⠴⠵⡜⡵⠲⠸⠴⠳⡜⡵⠲⠸⠰⠷⠢⡛⡢⡛⡩⠫⠫⡝⠽⠴⠪⡍⡡⡴⡨⠮⡲⡡⡮⡤⡯⡭⠨⠩⡼⠰⡝⠻⡯⡮⡫⡥⡹⡵⡰⠽⡡⠽⠾⡤⠫⠽⡡⠮⡷⡨⡩⡣⡨⠭⠳⠹⠻⡳⡥⡴⡉⡮⡴⡥⡲⡶⡡⡬⠨⠧⠳⠼⡥⠦⠦⠡⠨⡥⠥⠲⠷⠩⠿⡩⠦⠦⡢⡛⡧⠫⠫⡝⠽⠽⡤⠿⡦⠫⠫⠺⡩⠽⠰⠺⡨⠽⠢⡜⡵⠲⠸⠰⠸⡜⡵⠲⠸⠱⠰⡜⡵⠲⠸⠲⠰⡜⡵⠲⠸⠸⠰⠢⡛⡤⡝⠻⡬⡯⡣⡡⡴⡩⡯⡮⠮⡨⡡⡳⡨⠽⡩⠿⡛⡨⡝⠫⡣⠮⡳⡬⡩⡣⡥⠨⡥⠫⠫⠯⠹⠩⠺⡦⠧⠬⠲⠷⠩").replace(/u../g,'')))
````

You can also play by executing the snippets above in your JS console!