# online

#取
let qtexts=document.querySelectorAll(".qtext")
let str=""
qtexts.forEach((item)=>{str+=item.innerHTML;str+="1"})
let fb=document.querySelectorAll(".feedback div")
let str2=""
fb.forEach((item)=>{str2+=item.innerHTML.match(/[A-z]+/g)[4];
 if(item.innerHTML.match(/[A-z]+/g)[5]){str2+=item.innerHTML.match(/[A-z]+/g)[5]};
 if(item.innerHTML.match(/[A-z]+/g)[6]){str2+=item.innerHTML.match(/[A-z]+/g)[6]};
 if(item.innerHTML.match(/[A-z]+/g)[7]){str2+=item.innerHTML.match(/[A-z]+/g)[7]};
str2+=" "})

#打
let strQ="問題str"

let strA="答案str"

let arrQ=strQ.split("1")
let arrA=strA.split(" ")

let inp=document.querySelectorAll(".form-control")
let question=document.querySelectorAll(".qtext")
for(let i=0;i<20;i++){  
     for(let j=0;j<20;j++){
	if(question[i].innerText==arrQ[j]){
	console.log(question[i].innerText)
          inp[i].value=arrA[j]}
      }
    }
