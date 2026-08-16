# Graal Online Era Levels
Brief overview of my personal work for GraalOnline

Code- 
code for city below platform image:
dontblock();
drawoverplayer();
//#CLIENTSIDE
function onCreated(){
  this.imgwidth = getimgwidth(this.image) / 16;
  this.imgheight = getimgheight(this.image) / 16;
  this.mode = 1;
  onTimeOut();
}
function onTimeOut(){
  if(client.player_screenshotting){
    this.alpha = 1;
    return setTimer(0.01);
  }
  //this.chat = format("X: %s End X: %s Y: %s End Y: %s Alpha: %s", this.x , this.x  + this.imgwidth, this.y , this.y  + this.imgheight, this.alpha);
  temp.inleft = player.x  + 1 in |0, 23| && player.y  + 1.5 in |49, 64|;
  temp.inright = player.x  + 1 in |64-23, 64| && player.y  + 1.5 in |49, 64|;
  if(inleft || inright) fadeOut();
   else fadeIn();
  setTimer(0.01);
}
function fadeOut(){
  if(this.alpha <= 0) return;
  this.alpha -= 0.1;
}
function fadeIn(){
  if(this.alpha >= 1) return;
  if(this.alpha < 1) this.alpha += 0.1;
}
Code for Black Files Below:
//#CLIENTSIDE
function onCreated(){
 dontblock();
 drawunderplayer();
  this.imgwidth = getimgwidth(this.image) / 16;
  this.imgheight = getimgheight(this.image) / 16;
  this.mode = 1;
  onTimeOut();
}
function onTimeOut(){
  if(client.player_screenshotting){
    this.alpha = 1;
    return setTimer(0.05);
  }
  //this.chat = format("X: %s End X: %s Y: %s End Y: %s Alpha: %s", this.x , this.x  + this.imgwidth, this.y , this.y  + this.imgheight, this.alpha);
  if(player.x  + 1 in |this.x , this.x  + this.imgwidth| && player.y  + 1.5 in |this.y , this.y  + this.imgheight|) fadeOut();
  else fadeIn();
  setTimer(0.05);
}
function fadeOut(){
  if(this.alpha <= 0) return;
  this.alpha -= 0.1;
}
function fadeIn(){
  if(this.alpha >= 1) return;
  if(this.alpha < 1) this.alpha += 0.1;
}
