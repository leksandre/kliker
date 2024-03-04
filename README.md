# kliker
экономит кучу времени на интерфейсах где разрабы хотели заставить тебя кликать до посинения





const delay = (delayInms) => {
  return new Promise(resolve => setTimeout(resolve, delayInms));
};

async function dalall1(){

//await document.getElementsByClassName("VfPpkd-vQzf8d")[0].click();

var els1 = document.getElementsByTagName("span");
let len = els1.length;
for (i=0; i < len; i++) {
textContentOutput = els1[i].textContent;
innerTextOutput = els1[i].innerText;
if (textContentOutput=='Удалить все' || innerTextOutput=='Удалить все')
  await els1[i].click();
}


await delay(3000);

els1 = document.getElementsByTagName("input");
len = els1.length;
for (i=0; i < len; i++) {
  await els1[i].click();
}

 await delay(3000);

els1 = document.getElementsByTagName("button");
len = els1.length;
for (i=0; i < len; i++) {
textContentOutput = els1[i].textContent;
innerTextOutput = els1[i].innerText;
if (textContentOutput=='Удалить' || innerTextOutput=='Удалить')
  await els1[i].click();
}

}

setInterval(dalall1, 10000);
