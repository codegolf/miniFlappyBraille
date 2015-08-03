# miniFlappyBraille

A clone of http://flappybraille.ndre.gr/

golfed by @xem, @ilesinge, @aemkei, @subzey, @p01, ...

- Look at the URL.
- Play with arrows up and down.

**demo 1** (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

**demo 2** (golfed, dirtier, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (204b / 188 chars)

````
g=b=[c=""];for(d=e=f=i=0;g;onkeyup=a=>d+=a.which-39)c+="  "+"⡆⡅⡃⠇"[b[i++]=(g=7*++g%97)%4];setInterval('e>3&&!(e%27)?i&&b[g++]==d?f++:i=0:i;location.hash=i?["⠈⠐⠠⢀"[d]]+c.slice(e++/9):f',27)
````

**demo 3** (golfed, obfuscated in braille): http://codegolf.github.io/miniFlappyBraille/index.min.braille.html

source code (758b / 282 chars) (not up to date)

````
eval(unescape(escape("⡢⠽⡛⡣⠽⠢⠢⡝⠻⡦⡯⡲⠨⡤⠽⡥⠽⡦⠽⡧⠽⡩⠽⠰⠻⠹⠹⠾⡩⠻⠩⡣⠫⠽⠢⠠⠠⠢⠫⠢⡜⡵⠲⠸⠴⠶⡜⡵⠲⠸⠴⠵⡜⡵⠲⠸⠴⠳⡜⡵⠲⠸⠰⠷⠢⡛⡢⡛⡩⠫⠫⡝⠽⠴⠪⡍⡡⡴⡨⠮⡲⡡⡮⡤⡯⡭⠨⠩⡼⠰⡝⠻⡯⡮⡫⡥⡹⡵⡰⠽⡡⠽⠾⡤⠫⠽⡡⠮⡷⡨⡩⡣⡨⠭⠳⠹⠻⡳⡥⡴⡉⡮⡴⡥⡲⡶⡡⡬⠨⠧⠳⠼⡥⠦⠦⠡⠨⡥⠥⠲⠷⠩⠿⡩⠦⠦⡢⡛⡧⠫⠫⡝⠽⠽⡤⠿⡦⠫⠫⠺⡩⠽⠰⠺⡨⠽⠢⡜⡵⠲⠸⠰⠸⡜⡵⠲⠸⠱⠰⡜⡵⠲⠸⠲⠰⡜⡵⠲⠸⠸⠰⠢⡛⡤⡝⠻⡬⡯⡣⡡⡴⡩⡯⡮⠮⡨⡡⡳⡨⠽⡩⠿⡛⡨⡝⠫⡣⠮⡳⡬⡩⡣⡥⠨⡥⠫⠫⠯⠹⠩⠺⡦⠧⠬⠲⠷⠩").replace(/u../g,'')))
````

Source code shaped like a pipe:

````

  eval(unescape(escape
  ('⡢⠽⡛⡣⠽⠢⠢⡝⠻⡦⡯⡲⠨⡤⠽⡥⠽\
  ⡦⠽⡧⠽⡩⠽⠰⠻⠹⠹⠾⡩⠻⠩⡣⠫⠽⠢⠠\
  ⠠⠢⠫⠢⡜⡵⠲⠸⠴⠶⡜⡵⠲⠸⠴⠵⡜⡵⠲\
  ⠸⠴⠳⡜⡵⠲⠸⠰⠷⠢⡛⡢⡛⡩⠫⠫⡝⠽⠴\
  ⠪⡍⡡⡴⡨⠮⡲⡡⡮⡤⡯⡭⠨⠩⡼⠰⡝⠻⡯\
       ⡮⡫⡥⡹⡵⡰⠽⡡⠽\
       ⠾⡤⠫⠽⡡⠮⡷⡨⡩\
       ⡣⡨⠭⠳⠹⠻⡳⡥⡴\
       ⡉⡮⡴⡥⡲⡶⡡⡬⠨\
       ⠧⠳⠼⡥⠦⠦⠡⠨⡥\
       ⠥⠲⠷⠩⠿⡩⠦⠦⡢\
       ⡛⡧⠫⠫⡝⠽⠽⡤⠿\
       ⡦⠫⠫⠺⡩⠽⠰⠺⡨\
       ⠽⠢⡜⡵⠲⠸⠰⠸⡜\
       ⡵⠲⠸⠱⠰⡜⡵⠲⠸\
       ⠲⠰⡜⡵⠲⠸⠸⠰⠢\
       ⡛⡤⡝⠻⡬⡯⡣⡡⡴\
       ⡩⡯⡮⠮⡨⡡⡳⡨⠽\
       ⡩⠿⡛⡨⡝⠫⡣⠮⡳\
       ⡬⡩⡣⡥⠨⡥⠫⠫⠯\
       ⠹⠩⠺⡦⠧⠬⠲⠷⠩'
       ).replace(
       /%20|u../g
       ,'')))//<3

````

**You can also play by executing the snippets above in your JS console!**
