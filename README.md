# DartPad-Bike-Example
https://dartpad.dartlang.org


void main() {
  
  var bike = new Bicycle(2, 100, 1);
  var mybike = new Bicycle(20, 1000, 110);
  
  bike.applyBrake(10);
  mybike.applyBrake(100);
  
  print(bike._speed);
  print(mybike._speed);
}


class Bicycle {
  int cadence;
  int _speed;
  int gear;
 
 Bicycle(this.cadence, this._speed, this.gear);

  @override
  String toString() => 'Bicycle: $_speed mph';
  
  int get speed => _speed;
  
  void applyBrake(int decrement) {
  _speed -= decrement;
}

void speedUp(int increment) {
  _speed += increment;
}
}
