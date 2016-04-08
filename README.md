# ramp-up-js
#ramp up for wdk

//=============CHANGE HEADER=============
var myHeading = document.querySelector('p');
myHeading.textContent = 'Hello Kev!';
=========================================


//============CHANGE BG COLOR====================================
document.querySelector('html').style.backgroundColor = '#D0D0CD';
=================================================================

//=====INTERACT WITH WEBPAGE=================
document.querySelector('html').onclick=function () {
//	alert('You\'re clicking on this page');
};
===========================================

//==============CHANGE IMAGE==============
myImage = document.querySelector('img');
myImage.onclick = function () {
	var mySrc = myImage.getAttribute('src');
	
	if(mySrc === 'images/intel.jpg'){ 
		myImage.setAttribute('src', 'images/android_intel.png');
	} else {
		myImage.setAttribute('src','images/intel.jpg');
	}
}
//========================================================

//=====Request name and change the header to your name=======
var myButton = document.querySelector('button');
var myHeading = document.querySelector('h1');

function setUserName() {
	var myName = prompt('Please enter in your name.');
	localStorage.setItem('name',myName);
	myHeading.textContent = 'Welcome ' + myName + "!";
}

if (!localStorage.getItem('name')) {
	setUserName();
} else {
	var storedName = localStorage.getItem('name');
	myHeading.textContent = 'Welcome ' + storedName + "!";
}

myButton.onclick = function() {
	setUserName();
}
//======================================================





