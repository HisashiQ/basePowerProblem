#include <iostream>
#include <cmath>

int getPower(int&, int&);
int getRemainder(int&, int&, int&);
bool isDivisableByBase(int&, int&);

int main(){
	int target, base;
	
	std::cin>>target;
	std::cin>>base;
	int i = getPower(target, base);
	int remainder = getRemainder(i, base, target);
	if (remainder != 0){
		if(isDivisableByBase(remainder, base))
		{
			int baseMultiplication = remainder / base;
			std::cout<<target<<" = "<< base << "^" << i << " + " << "(" << base << "*" << baseMultiplication<<")" <<std::endl;
		} else {
			std::cout<<target<<" = "<< base << "^" << i << " + " << remainder <<std::endl;
		}
	} else { 
		std::cout<<target<<" = "<< base << "^" << i <<std::endl;
	}
	
	return 0;
}

int getPower(int &target, int &base){
	int total = 0;
	int i = 0;
	while(total <= target){
		i++;
		total = std::pow(base, i);
	}
	return i-1;
}

int getRemainder(int &i, int &base, int &target){
	return target - std::pow(base, i);
}

bool isDivisableByBase(int &remainder, int &base){
	if(remainder % base == 0)
	{
		return true;
	}
	else
	{
	return false;
	}
}
