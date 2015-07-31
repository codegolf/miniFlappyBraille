# miniFlappyBraille

golfed clone of http://flappybraille.ndre.gr/

Look at the URL.

Play with arrows up and down. 

demo (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

demo (golfed, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (264b)

````
b=[c=""];for(d=e=f=g=i=0;500>i;i++)c+="  "+"⡆⡅⡃⠇"[
b[i]=4*Math.random()|0];onkeyup=a=>d+=a.keyCode-39
,0>d&&(d=0),3<d&&(d=3);setInterval('3<e&&!(e%30)?b
[g++]==d?(h="⡇",f++):alert(f):h="⠁⠂⠄⡀"[d];history.
replaceState(0,0,"#"+(h+c.slice(e++/10)))',30)
````
