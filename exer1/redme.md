
bom primeiramente eu separei todos os materiais que eram necessarios,como arduino uno,os resistores,o led RGB,o potenciômetro,enfim tudo que era necessario,logo depois fui ligando os fios como eu aprendi em aulas anteiores,usei a ajuda do professor,
e fui me guiando pelo exemplo que o professor havia disponibilizado no classroom,e no codigo a mesma coisa fui me guiando através de outros códigos que fiz e fui tentando errando até que consegui,fiquei bem feliz que consegui concluir a atividade.

// C++ code
//
int pote_A2 = 0;

int pote_A1 = 0;

int pote_A0 = 0;

void setup()
{
  pinMode(A0, INPUT);
  pinMode(A1, INPUT);
  pinMode(A2, INPUT);
  Serial.begin(9600);
  pinMode(11, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(9, OUTPUT);
}

void loop()
{
  pote_A2 = analogRead(A0);
  pote_A1 = analogRead(A1);
  pote_A2 = analogRead(A2);
  Serial.println(pote_A0);
  analogWrite(11, map(pote_A0, 0, 1023, 0, 180));
  analogWrite(10, map(pote_A1, 0, 1023, 0, 180));
  analogWrite(9, map(pote_A2, 0, 1023, 0, 180));
  delay(10); // Delay a little bit to improve simulation performance
}
