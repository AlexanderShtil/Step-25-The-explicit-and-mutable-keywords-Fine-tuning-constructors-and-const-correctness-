# Step-25-The-explicit-and-mutable-keywords-Fine-tuning-constructors-and-const-correctness-
#include <iostream>
#include <windows.h>
#include <string>
#include <memory>

class Weapon {
private:
	int damage;
	mutable int use_count{ 0 };
public:

	explicit Weapon(int dmg) : damage{dmg} {}

	void fire() const {
		std::cout << "Выстрел! Урон: " << damage << std::endl;
		use_count++;
		std::cout << "Оружие использовано раз: " << use_count << std::endl;
	}

};

 int main(){
	 SetConsoleCP(1251);
	 SetConsoleOutputCP(1251);
	 
	 Weapon sword{ 25 };

	 sword.fire();

	 
	 return 0;
 }
