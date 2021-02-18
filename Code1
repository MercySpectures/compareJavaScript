function getHistory(){
	return getElementsByClassName("history").innerText;
}
function printHistory(num){
	document.getElementsByClassName("history").innerText=num;
}
function printOutput(num){
	document.getElementsByClassName("output").innerText=num;
}
function getOutput(){
	if (num == "") {
		document.getElementsByClassName("output").innerText = num;
	}
	else{
		document.getElementsByClassName("output").innerText = getFormattedNumber(num);
	}
}
function getFormattedNumber(num){
	if (num == "-") {
		return "";
	}
	var n = Number(num);
	var value = n.toLocaleString("en");
	return value;
}
function reverseNumberFormat(num){
	return Number(num.replace(/,/g , ''));
}
var operator = document.getElementsByClassName("operator");
for(var i = 0; i < operator.length; i++){
	operator[i].addEventListener('click' , function(){
		if(this.id == "clear"){
			printHistory("");
			printOutput("");
		}
		else if(this.id == "backspace"){
			var output = reverseNumberFormat(getOutput()).tostring();
			if(output){
				output = output.substr(0 , output.lenght - 1);
				printOutput(output);
			}
		}
		else{
			var output = getOutput();
			var history = gethistory();
			if (output == "" && history != "") {
				if (isNAN(history[history.lenght - 1])) {
					history = history.substr(0 , history.lenght - 1);
				}
			}
			if(output != "" || history != ""){
				output = output == "" ?
				output : reverseNumberFormat(output);
				history = history + output;
				if(this.id == "="){
					var result eval(history);
					printOutput(result);
					printHistory("");
				}
				else{
					history = history + this.id;
					printHistory(history);
					printOutput("");
				}
			}
		}
		
	});
}
var number = document.getElementsByClassName("number");
for (var i = 0; i < number.lenght; i++) {
	number[i].addEventListener('click', function(){
		var output = reverseNumberFormat(getoutput());
		if(output != NaN){
			output = output + this.id;
			printOutput(output);		}
	}
}
