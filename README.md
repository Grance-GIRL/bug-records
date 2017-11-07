# bug-records# bug-records
 **`Honesty, diligence and specialization`**

### after argument with the courier with my apples,now 22:43,I begin to write the Programming; want your love;



> just import parts for Programmer ，the Seamless rolling（无缝滚动）；
>



window.onload=function(){

​	var box=document.getElementById("all");

​	var screen=document.getElementById("screen");

​	var imgWidth=screen.offsetWidth;

​	var ul=document.getElementById("ul");

​	var ulLiArr=ul.children;

​	var ol=document.getElementById("ol");

​	var arr=document.getElementById("arr");

​	var left=document.getElemetById("left");

​	var right=document.getElementById("right");

//one

​	for(var i=0;i<ulLiArr.length;i++){

​		var li=document.createElement("li");

​		li.innerHTML=i+1;

​		ol.appendChild(li);

​	}

​	var olLiArr=ol.children;

​	olLiArr[0].className="current";

​	var newLi=ulLiArr[0].cloneNode(true);

​	ul.appendChild(newLi);



//two

​	for(var i=0;i<olLiArr.length;i++){

​	 	olLiArr[i].index=i;

​		olLiArr[i].onmouseover=function(){

​		olLiArr[j].className="";

​        	}

​		this.className="current";

​		var sss=-imgWidth*this.index;

​		animate(ul,sss);

##### //bug2

​		console.log(this.index);

​		if(square===4&&this.index===0){

​			animate(ul,sss-imgWidth*(ulLiArr.length-1));

​		}

##### //bug2

​		if(square===4&&this.index===1){

​			animate(ul,-imgWidth*(ulLiArr.length-1),function(){

​				ul.style.left=0;

​				animate(ul,-imgWidth*1);

​			});	

​		}

##### //bug2

​		if(square===5&&this.index===1&&this.index===2&&this.index===0){

​			ul.style.left=0;

​			animate(ul,-imgWidth*1);

​		}

##### //bug2

​		if(key===0&&(this.index==4 || this.index==3 )){

​				ul.style.left=-(ulLiArr.length-1)*imgWidth+"px";

​				animate(ul,-imgWidth*this.index);

​		}



##### //bug1

​		key=this.index;

​		square=this.index;

​	}



​	//three

​	var key=0;

​	var square=0;

​	right.onclick=autoPlay;



​	//four

​	left.onclick=function(){

​		key--;

​		square--;

​		if(square===-1){

​			square=olLiArr.length-1;

​		}

​		if(key===-1){

​			ul.style.left=-(ulLiArr.length-1)*imgWidth+"px";

​			key=ulLiArr.length-2;

​		}

​		for(var j=0;j<olLiArr.length;j++){

​			olLiArr[j].className="";

​		}

​		olLiArr[square].className="current";

​		var sss=-imgWidth*key;

​		animate(ul,sss);

​	}

//five

​	var timer=setInterval(autoPlay,1500);

​	box.onmouseenter=function(){

​		arr.style.display="block";

​		clearInterval(timer);

​	}

​	box.onmouseleave=function(){

​		arr.style.display="none";

​		timer=setInterval(autoPlay,1500);

​	}



​	//four-logical

​	function autoPlay(){

​		key++;

​		square++;

​		if(square===olLiArr.length){

​			square=0;

​		}

​		if(key===ulLiArr.length){

​			ul.style.left=0;

​			key=1;

​		}

​		for(var j=0;j<olLiArr.length;j++){

​			olLiArr[j].className="";

​		}

​		olLiArr[square].className="current";

​		var sss=-imgWidth*key;

​		animate(ul,sss);s

​	}

}


 Honesty, diligence and specialization
