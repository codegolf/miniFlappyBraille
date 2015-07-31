# miniFlappyBraille
golfed clone of http://flappybraille.ndre.gr/

demo (unminified, ES5): http://codegolf.github.io/miniFlappyBraille

demo (golfed, ES6): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (348b)

````
b=[c=d=e=f=0];for(i=0;999>i;i++)b.push(4*Math.random()
|0);onkeyup=a=>{c+=a.keyCode-39;0>c&&(c=0);3<c&&(c=3)}
;s=setInterval(a=>{3<d&&!(d%30)?b[f++]==c?(g="⡇",e++):
alert(e):g="⠁⠂⠄⡀"[c];h="";for(i=0;999>i;i++)h+="  "+"⡆
⡅⡃⠇"[b[i]];history.replaceState(0,0,"#"+(g+h.slice(d++
/10)).slice(0,99))},30)
````
