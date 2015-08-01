# miniFlappyBraille

golfed clone of http://flappybraille.ndre.gr/

Look at the URL.

Play with arrows up and down. 

demo (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

demo (golfed, dirtier, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (213b / 197 chars)

````
b=[c=""];for(d=e=f=g=i=0;99>i;)c+="  "+"⡆⡅⡃⠇"[b[i++]=4*Math.random()|0];onkeyup=a=>d+=a.which-39;setInterval('3<e&&!(e%27)?i&&b[g++]==d?f++:i=0:h="⠈⠐⠠⢀"[d];location.hash=i?[h]+c.slice(e++/9):f',27)
````
