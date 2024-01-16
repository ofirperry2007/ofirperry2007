
const int trigPin = 9;
const int echoPin = 10;

float duration, distance;

void setup(){
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  Serial.begin(9600);
}
 void ultrasonic(){
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);
  distance = (duration*.0343)/2;
  if (distance < 20);
  Serial.print("Distance: ");
  Serial.println(distance);
  delay(100);
  if (distance > 20);
  Serial.print("NO: ");
  Serial.println(NO);

 }
 
void loop(){
  ultrasonic();
}

