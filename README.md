# miniFlappyBraille

A clone of http://flappybraille.ndre.gr/

golfed by @xem, @ilesinge, @aemkei, @subzey, @p01, ...

- Look at the URL.
- Play with arrows up and down.

**demo 1** (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

**demo 2** (golfed, dirtier, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (201b / 185 chars)

````
g=b=[c=""];for(d=e=f=i=0;g;onkeyup=a=>d+=a.which-39)c+="  "+"⡆⡅⡃⠇"[b[i++]=(g=7*++g%97)%4];setInterval('e<4||e%27?i:i&&b[g++]==d?f++:i=0;location.hash=i?["⠈⠐⠠⢀"[d]]+c.slice(e++/9):f',27)
````

**demo 3** (golfed, obfuscated in braille): http://codegolf.github.io/miniFlappyBraille/index.min.braille.html

(update soon)



**You can also play by executing the snippets above in your JS console!**
