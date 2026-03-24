# Sabre-de-luz
Projeto eletrônico inspirado em um sabre de luz, com detecção automática de impactos utilizando um circuito analógico com microfone.

Funcionamento

Detecta o impacto através do microfone
Identifica padrões de onda sonora
Conta pontos automaticamente
Exibe no display de 7 segmentos
Ao atingir 3 pontos, reinicia o sistema

Tecnologias

Arduino
Eletrônica analógica
Display de 7 segmentos
LEDs e buzzer

Resultado

Sistema funcional com detecção em tempo real, contagem automática e feedback visual e sonoro.


https://github.com/user-attachments/assets/b12187c0-f3b3-443f-854e-ee786afc281e

Código 

#define fuhrer 5
#define arroz 6
#define vaicorinthians 2
#define reltih 3
#define aaa 8
#define bbb 9
#define ccc 10
#define ddd 11
#define eee 12
#define fff 13 
#define ggg 7
int pontos = 0;
int adolfo;
bool tdb = 0;
//////////////////////////////////////////////
#define som 1
#define btp 4
#define aaah A0
#define bbbh A1
#define ccch A2
#define dddh A3
#define eeeh A4
#define fffh A5
#define gggh 0
int pt = 0;
bool lg = 0;
int fd = 0;
int fdo;
int fdot = 450;
int louco;
int x;

void setup()
{
  pinMode(aaah, OUTPUT);
  pinMode(bbbh, OUTPUT);
  pinMode(ccch, OUTPUT);
  pinMode(dddh, OUTPUT);
  pinMode(eeeh, OUTPUT);
  pinMode(fffh, OUTPUT);
  pinMode(gggh, OUTPUT);
  pinMode(btp, INPUT);
  pinMode(som, OUTPUT); 
  pinMode(arroz, OUTPUT);
  ///////////////////////////////////  
  pinMode(aaa, OUTPUT);
  pinMode(bbb, OUTPUT);
  pinMode(ccc, OUTPUT);
  pinMode(ddd, OUTPUT);
  pinMode(eee, OUTPUT);
  pinMode(fff, OUTPUT);
  pinMode(ggg, OUTPUT);
  pinMode(fuhrer, OUTPUT);
  
  pinMode(vaicorinthians, INPUT_PULLUP);
  pinMode(reltih, INPUT);	
}

void loop()
{
  if(digitalRead(vaicorinthians) == 0){
   tdb = !tdb;
   x++;
   }
  if(x == 1){
   x++;
   digitalWrite(som, HIGH);
   delay(500);
   digitalWrite(som, LOW);  
  }
  if(tdb == 1){
   contagem();
   ctm();
   
   
  
  }
  if(tdb  == 0){
   x = 0; 
   digitalWrite(arroz, LOW);
   digitalWrite(fuhrer, LOW);
   desliga();
   delay(50);
   dl();
   delay(50);
   }
////////////////////////////////////////////////
  
}   
     
void contagem(){
 for (adolfo ;adolfo <= 250; adolfo++) {
   analogWrite(fuhrer, (map(adolfo, 0, 1023,0, 127)));
   delay(5);
 }
  for (adolfo ;adolfo <= 450; adolfo++) {
   analogWrite(fuhrer, (map(adolfo, 0, 1023,127, 255 )));
   delay(2);  
  
 }
  if(digitalRead(reltih) == 1){
   pontos++;
   delay(500);
   }
  if(pontos == 0){
   tres();
   delay(10);
   } 
  
  if(pontos == 1){
   zero();
   delay(10);
   }
  if(pontos == 2){
   um();
   delay(10);
   }
  if(pontos == 3){
   dois();
   delay(10);
   }
  if(pontos == 3){
    louco = 6;
    drt();
    delay(50);
    pt = 0;
    pontos = 0;
    tres();
    delay(10);
    
  }
}  
 

void zero(){
  
  digitalWrite(aaa, HIGH);
  digitalWrite(bbb, LOW);
  digitalWrite(ccc, LOW);
  digitalWrite(ddd, HIGH);
  digitalWrite(eee, HIGH);
  digitalWrite(fff, HIGH);
  digitalWrite(ggg, HIGH);
} 
  
void um(){
   digitalWrite(aaa, LOW);
  digitalWrite(bbb, LOW);
  digitalWrite(ccc, HIGH);
  digitalWrite(ddd, LOW);
  digitalWrite(eee, LOW);
  digitalWrite(fff, HIGH);
  digitalWrite(ggg, LOW);
}

void dois(){
  digitalWrite(aaa, LOW);
  digitalWrite(bbb, LOW);
  digitalWrite(ccc, LOW);
  digitalWrite(ddd, LOW);
  digitalWrite(eee, HIGH);
  digitalWrite(fff, HIGH);
  digitalWrite(ggg, LOW);
}  
void tres(){
  digitalWrite(aaa, LOW);
  digitalWrite(bbb, LOW);
  digitalWrite(ccc, LOW);
  digitalWrite(ddd, LOW);
  digitalWrite(eee, LOW);
  digitalWrite(fff, LOW);
  digitalWrite(ggg, HIGH);
  }
  void desliga(){
    
   digitalWrite(fuhrer, LOW);
   delay(100); 
   digitalWrite(aaa, HIGH);
   digitalWrite(bbb, HIGH);
   digitalWrite(ccc, HIGH);
   digitalWrite(ddd, HIGH);
   digitalWrite(eee, HIGH);
   digitalWrite(fff, HIGH);
   digitalWrite(ggg, HIGH);
   delay(10);
   adolfo = 0; 
  }

void ctm(){
 for (fd ;fd <= 250; fd++) {
   analogWrite(arroz, (map(fd, 0, 1023,0, 127)));
   delay(5);
 }
  for (fd ;fd <= 450; fd++) {
   analogWrite(arroz, (map(fd, 0, 1023,127, 255)));
   delay(2);  
  
 }
  if(digitalRead(btp) == 1){
   pt++;
   delay(500);
   }
  if(pt == 0){
   ttte();
   delay(5);
   } 
  
  if(pt == 1){
   zzze();
   delay(5);
   }
  if(pt == 2){
   uuue();
   delay(5);
   }
  if(pt == 3){
   ddde();
   delay(5);
   }
  if(pt == 3){
    louco = 5;
    delay(5);
    drt();
    pontos = 0;
    pt = 0;
   
   
  }
 } 
void dl(){
    
   digitalWrite(arroz, LOW);
   delay(100); 
   digitalWrite(aaah, HIGH);
   digitalWrite(bbbh, HIGH);
   digitalWrite(ccch, HIGH);
   digitalWrite(dddh, HIGH);
   digitalWrite(eeeh, HIGH);
   digitalWrite(fffh, HIGH);
   digitalWrite(gggh, HIGH);
   delay(100);
   fd = 0; 
  }
void zzze(){
  
  digitalWrite(aaah, HIGH);
  digitalWrite(bbbh, LOW);
  digitalWrite(ccch, LOW);
  digitalWrite(dddh, HIGH);
  digitalWrite(eeeh, HIGH);
  digitalWrite(fffh, HIGH);
  digitalWrite(gggh, HIGH);
} 
  
void uuue(){
   digitalWrite(aaah, LOW);
  digitalWrite(bbbh, LOW);
  digitalWrite(ccch, HIGH);
  digitalWrite(dddh, LOW);
  digitalWrite(eeeh, LOW);
  digitalWrite(fffh, HIGH);
  digitalWrite(gggh, LOW);
}

void ddde(){
  digitalWrite(aaah, LOW);
  digitalWrite(bbbh, LOW);
  digitalWrite(ccch, LOW);
  digitalWrite(dddh, LOW);
  digitalWrite(eeeh, HIGH);
  digitalWrite(fffh, HIGH);
  digitalWrite(gggh, LOW);
}  
void ttte(){
  digitalWrite(aaah, LOW);
  digitalWrite(bbbh, LOW);
  digitalWrite(ccch, LOW);
  digitalWrite(dddh, LOW);
  digitalWrite(eeeh, LOW);
  digitalWrite(fffh, LOW);
  digitalWrite(gggh, HIGH);
  }

void drt(){
 
  
  for (fdo = 450 ;fdo >= 250; fdo--) {
   analogWrite(louco, (map(fdo, 0, 1023,255, 127 )));
   delay(2);
 }
  for (fdo = 250  ;fdo >= 0; fdo--) {
   analogWrite(louco, (map(fdo, 0, 1023,127, 0)));
   delay(5);  
  }
  digitalWrite(louco, LOW);
  fd = 0;
  delay(3000);
  
  for (fd ;fd <= 250; fd++) {
   analogWrite(louco, (map(fd, 0, 1023,0, 127)));
   delay(5);
 }
  for (fd ;fd <= 450; fd++) {
   analogWrite(louco, (map(fd, 0, 1023,127, 255)));
   delay(2);  
  
 }
}



