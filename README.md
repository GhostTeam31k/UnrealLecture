# UnrealLecture
![back](https://github.com/GhostTeam31k/UnrealLecture/assets/148298741/4a86bcba-ce22-4ea5-9aec-206d3b8c9d68)

#include <iostream>
#include <ctime> 
#include <cstdlib>

int main() {
	// 랜덤 숫자 생성을 위한 시드 설정
	std::srand(static_cast<unsigned>(std::time(nullptr)));

	int randomNumber = std::rand() % 100 + 1; // 1부터 100 사이의 랜덤 숫자 생성
	int guess;
	int attempts = 0;

	std::cout << "1부터 100 사이의 숫자를 맞추어 보세요." << std::endl;

	do {
		std::cout << "추측한 숫자를 입력하세요: ";
		std::cin >> guess;
		attempts++;

		if (guess < randomNumber) {
			std::cout << "숫자가 너무 작습니다. 다시 시도하세요." << std::endl;
		}
		else if (guess > randomNumber) {
			std::cout << "숫자가 너무 큽니다. 다시 시도하세요." << std::endl;
		}
		else {
			std::cout << "축하합니다! " << attempts << "번 만에 숫자를 맞췄습니다." << std::endl;
		}
	} while (guess != randomNumber);

	return 0;
}
