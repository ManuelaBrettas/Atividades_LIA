# Montagem Básica com LEDs e Botão
### Descrição
Este projeto demonstra como controlar um LED usando um botão conectado a um Arduino. Ao pressionar o botão, o LED integrado no pino 13 da placa Arduino será ligado. A configuração utiliza um resistor pull-up de 10 kΩ para garantir que a entrada digital seja lida corretamente pelo Arduino.
### Funcionamento
**Botão não pressionado:** Quando o botão não está pressionado, o pino 2 da placa Arduino é conectado à terra através do resistor pull-up, fazendo com que a entrada seja LOW (0V). O LED permanece desligado.
**Botão pressionado:** Quando o botão é pressionado, a entrada digital se torna HIGH (5V), e o LED é ligado.
Além disso, é possível inverter o circuito, utilizando um resistor pull-down para manter a entrada HIGH por padrão e torná-la LOW quando o botão é pressionado, invertendo assim o comportamento do LED.



### Código

const int buttonPin = 2;    
const int ledPin = 13;      

int buttonState = 0;        

void setup() {
  pinMode(ledPin, OUTPUT);      
  pinMode(buttonPin, INPUT_PULLUP);   pull-up
}

void loop() {
  
  buttonState = digitalRead(buttonPin);

 (estado LOW)
  if (buttonState == LOW) {
    digitalWrite(ledPin, HIGH);  
  } else {
    digitalWrite(ledPin, LOW);   
  }
}
}
![Diagrama](https://www.tinkercad.com/things/a2thU9i1WKs-swanky-kasi-rottis)
