let quest= document.createElement("div");
let box1 =document.createElement("div");
let box2 =document.createElement("div");
let box3 =document.createElement("div"); 
let box4 =document.createElement("div");
let head= document.querySelector("#head");
let next = document.querySelector("#next");
let card =document.querySelector("#card");
quest.setAttribute("id","quest");
box1.setAttribute("class","box");
box2.setAttribute("class","box");
box3.setAttribute("class","box");
box4.setAttribute("class","box");

box1.setAttribute("id","box1");
box2.setAttribute("id","box2");
box3.setAttribute("id","box3");
box4.setAttribute("id","box4");
quest.setAttribute("id","quest");
quest.innerText= " 1. Which is the largest animal in the the world ?";
head.after(quest);
quest.after(box1);
box1.after(box2);
box2.after(box3);
box3.after(box4);
box1.innerText ="Shark";
box2.innerText ="Blue Whale";
box3.innerText ="Elephant";
box4.innerText ="Giraffe";
let box= document.querySelectorAll(".box");
const quiz=[
    {
     question:" 1. which is the largest desert in the world",
        a:"kalahari",
        b:"Gobi",
        c:"sahara",
        d:"Antartica",
        correct:"sahara"
        
    },
    {
        question:"2. which is the largest animal in the world",
       
            a:"shark",
            b:"Blue Whale",
            c:"Elephant",
            d:"Giraffe",
            correct:"Blue Whale"



    },
    {
        question:"3. which is the smallest continent in the world?",
       
            a:"Asia",
            b:"Artic",
            c:"Australia",
            d:"Agfica",
            correct:"Australia"
            
       
    },
    {
        question:"4. which is the smallest country in the world?",
        
            a:"Vatican City",
            b:"Bhutan",
            c:"Nepal",
            d:"Shri Lanka",
            correct:"Vatican City"
        
    }

]
 let index=0;
let score= 0;
const loadQuestion =()=>{
    

   quest.innerText = quiz[index].question;




   box1.innerText =quiz[index].a;
   box2.innerText =quiz[index].b;
   box3.innerText =quiz[index].c;
   box4.innerText =quiz[index].d;
}


box.forEach((event=>{
    event.addEventListener("click",(e)=>{
        
        handledAnswer(e.target);

    })
}))


function handledAnswer(selectedBox){
    if(selectedBox.innerText===quiz[index].correct){
        console.log("correct");
        
        selectedBox.style.backgroundColor = "green";
        score++;        

    }else{
        selectedBox.style.backgroundColor ="red"; 
        console.log("incorrect");
       
        
    }
};


next.addEventListener("click",()=>{
    
       box1.style.backgroundColor ="white"; 
   box2.style.backgroundColor ="white"; 
   box3.style.backgroundColor ="white"; 
   box4.style.backgroundColor ="white"; 

    
    if(index<quiz.length-1){
        index++;
        loadQuestion();
       
    }else{
        console.log("Quiz is completed");
        console.log(`your score is ${score}`);
        quest.remove();
        head.remove();
        box1.remove();
        box2.remove();
        box3.remove();
        box4.remove();
        next.remove();
        let answer =document.createElement("div");
        let ans= document.createElement("div");
        ans.innerHTML= "<h1>Quiz Ended</h1>";
        answer.innerHTML= `<h1>Your Scored ${score} out of 4</h1> `;
     
        card.prepend(answer);
        card.prepend(ans);
        answer.style.marginLeft ="5rem";
        ans.style.marginLeft ="9rem";
        answer.style.marginTop ="5rem";
        ans.style.marginTop ="5rem";
    }
    

});

    loadQuestion();


