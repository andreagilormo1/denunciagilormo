# denunciagilormo

<!DOCTYPE html>
<html>
<title>denuncia contro il fumo di gilormo</title>

<body  bgcolor="yellow">


  
   L'argomento di denuncia sociale che io e il mio gruppo vorremmo trattare è a riguardo del consumo di sigarette.    <br> 
In media una persona fuma 0,48 sigarette all'ora e l'emissione, in grammi, di CO2 è pari a 67.666.666g all'ora  <br> 
in più ogni ora muoiono 8,56 persone. Solo in Italia la quantità media di sigarette fumate e pari a 4.833.333 all'ora. <br> 
Purtroppo questo è un argomento molto complicato da trattare, le sigarette creano dipendenza e le persone non riescono più a farne a meno. <br> 
alcuni obbiettivi che sono imperativi da raggiungere secondo noi sono: <br> 
1) cercare in qualche modo di ridurre la quantità di CO2 emessa;  <br> 
2) trattare diversamente alcuni composti presenti nel fumo per ridurre il tasso di mortalità dovuto da esso; <br> 
3) perseverare per limitare ancora di più le aree dove si può fumare <br> 
ad esempio vietare di fumare alla fermata dell'autobus dato che a molte persone solo l'odore di sigaretta crea fastidio. <br> 
<br>
<br>
<h1><font color="red"> qui ci sono i link per le varie informazioni sui fumatori  </font>   </h1>

<br>
<br>
<a href="https://www.airc.it/cancro/prevenzione-tumore/il-fumo/smettere-di-fumare-si-puo#:~:text=In%20Italia%20si%20stima%20che,i%2035%20e%20i%2065%20anni.">  come smettere di fumare       </a>    <br> 
<a href="https://www.epicentro.iss.it/fumo/">   informazioni generali sul fumo       </a>         <br>
<a href="https://www.fondazioneveronesi.it/magazine/articoli/fumo/sempre-piu-fumatori-giovanissimi-sono-il-doppio-rispetto-al-1990"> come mai l'eta media dei fumatori sta diminuendo         </a>      <br>   
 <a href="https://www.airc.it/cancro/prevenzione-tumore/il-fumo/fumo-le-domande-piu-frequenti">  domande piu fatte sul fumo          </a>      
<br>
<br>
<h1><font color="red"> fumatori nelle varie aree geografiche  </font>   </h1>
<br>
<br>
<img src="https://www.redattoresociale.it/media/fumo_aree_geografiche_fumatori?s=65">
<br>
<br>
<h1><font color="red"> questi sono i fumatori in italia classificati per sesso ed eta         </font>   </h1>
<br>
<br>
<img src="https://www.redattoresociale.it/media/fumo_fumatori_x_eta_2013?s=65">
<br>
<br>
<br>
<br>
<button onclick="aggiornamento1()">Mostra il numero di morti mediamente in italia in base al numero di ore inserito</button>
<input type="text" id="num1" value="1">
<h2 id="somma1"></h2>
<br>
<br>
<input type="button" value ="numero di morti specifici"  name="numero di morti specifici"  onclick="fspec1()">
<br>
<br>

<button onclick="inizio2()">Mostra il numero di sigarette di ogni ora in base al numero di persone</button>
<input type="text" id="num2" value="1">
<h2 id="somma2"></h2>
<br>
<br>

<input type="button" value ="sigarette fumate specifiche"  name="sigarette fumate specifiche"  onclick="fspec2()">
<br>
<br>

<button onclick="inizio3()">Mostra il numero di ore di vita perse in base al numero di persone di cui teniamo conto</button>
<input type="text" id="num3" value="1">
<h2 id="somma3"></h2>
<br>
<br>

<input type="button" value ="ore di vita perse specifiche"  name="ore di vita perse specifiche"  onclick="fspec3()">
<br>
<br>

<button onclick="inizio4()">inserire la co2 che viene prodotta in media ogni ora</button>
<input type="text" id="num4" value="1">
<h2 id="somma4"></h2>
<br>
<br>

<input type="button" value ="co2 specifica prodotta"  name="co2 specifica prodotta"  onclick="fspec4()">
<br>
<br>
<a href="https://andreagilormo17.wixsite.com/my-site-6/sito-di-denuncia-contro-il-fumo"> link se si è interessati al codice di questo sito web </a>
<script>
var t2=0;
var k2=0.483;
var k3=0.0885;
var t3=0;
var t4=0;

function aggiornamento1 (){
var tempo =document.getElementById("num1").value;
var k=8.56;
tempo=tempo*1;
var risultato= tempo*k;
document.getElementById("somma1").innerHTML=risultato;

}

function fspec1(){
var tempo,k,risultato;
k=8.56;
tempo=prompt("inserire il tempo ");
tempo=tempo*1;
risultato=tempo*k;
alert("il numero di morti corrisponde a "+risultato);
}

function inizio2(){

setInterval(aggiornamento2,1000);

}


function aggiornamento2 (){
var num =document.getElementById("num2").value;
num=num*1;
k2=k2*1;
var risultato= num*k2*t2;
document.getElementById("somma2").innerHTML=risultato;
t2=t2+1;
}

function fspec2(){
var n2,t2,k2,risultato2;
n2=prompt("inserire il numero di persone");
k2=prompt("inserire sigarette che fuma mediamente una persona in un'ora");
t2=prompt("inserire il tempo");
risultato2=k2*n2*t2;
alert("il risultato è "+risultato2);
}
function inizio3(){

setInterval(aggiornamento3,1000);

}


function aggiornamento3 (){
var num =document.getElementById("num3").value;
num=num*1;
k=k3*1;
var risultato= num*k3*t3;
document.getElementById("somma3").innerHTML=risultato;
t3=t3+1;
}

function fspec3(){
var np,t,k,risultato3;
k=0.0885;
t=prompt("inserire il tempo");
np=prompt("inserire il numero di persone");
t=t*1;
np=np*1;
risultato3=k*t*np;
alert("il risultato è "+risultato3);
}
function inizio4(){

setInterval(aggiornamento4,1000);

}


function aggiornamento4 (){
var k =document.getElementById("num4").value;
k=k*1;
var risultato= k*t4;
document.getElementById("somma4").innerHTML=risultato;
t4=t4+1;
}

function fspec4(){
var t,risultato4,k;
k=prompt("inserire la quantita di co2 al ora");
k=k*1;
t=prompt("inserire il tempo");
t=t*1;
risultato4=k*t;
alert("il risultato è "+risultato4);
}


</script>

</body>
</html>
