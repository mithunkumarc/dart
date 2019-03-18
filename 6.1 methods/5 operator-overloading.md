class Player{
  var score;
  operator + (Player p) => this.score + p.score;
  operator - (Player p) => this.score - p.score;
  operator * (Player p) => this.score * p.score;
  operator / (Player p) => this.score / p.score;
  bool operator == (dynamic other) => this.score == other.score; 
}

main(List<String> args) {
  var p1 =Player();
  var p2 =Player();
  p1.score = 100;
  p2.score = 50;
  print(p1 + p2);//150
  print(p1 - p2);//50
  print(p1 * p2);//5000
  print(p1 / p2);//2.0
  print(p1 == p2);//false
}


operator allowed on following operators 

< 	  + 	  | 	  []
> 	  / 	  ^ 	  []=
<= 	  ~/ 	  &   	~
>= 	  * 	  << 	  ==
– 	  % 	
