# miniFlappyBraille
golfed clone of http://flappybraille.ndre.gr/

demo: http://codegolf.github.io/miniFlappyBraille

demo (golfed): http://codegolf.github.io/miniFlappyBraille/index.min.html

source code (393b)

````
b=[c=d=e=f=0];for(i=0;999>i;i++)b.push(4*Math.random()|0);onkeyup=function(
a){38==a.keyCode&&0<c&&c--;40==a.keyCode&&3>c&&c++};s=setInterval(function(
){3<d&&!(d%30)?b[f++]==c?(g="⡇",e++):(clearInterval(s),alert(e)):g="⠁⠂⠄⡀"[c
];h="";for(i=0;999>i;i++)h+="  "+"⡆⡅⡃⠇"[b[i]];history.replaceState(0,0,"# "
+(g+h.slice(d++/10)).slice(0,99))},30)
````
