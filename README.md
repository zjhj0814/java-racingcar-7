# java-racingcar-precourse

## 🚗RacingCar

-[X] RacingCar 생성자
    - 자동차 이름
    - 현재 전진 기록
-[X] RacingCar 전진 시도
    - `camp.nextstep.edu.missionutils.Randoms의 pickNumberInRange()` 사용하여 전진 여부 결정

### RacingCarValidator

-[X] 자동차 이름 글자 수(1 이상 5 이하) 검증
- 유효하지 않을 경우 `IllegalArgumentException` 발생

## 🚖RacingCars🚘

-[X] RacingCars 생성자
    - RacingCar 리스트
    - 현재까지 시도 횟수
    - 시도 횟수
    - 우승자 정보
-[X] RacingCars 1회 진행
-[X] 우승자 결정
-[X] 시도 횟수만큼 시도했는지 확인

## WinnerDto

-[X] WinnerDto 생성자
    - WinnerName

## RacingCarController

-[X] InputView에서 이름, 시도 횟수 입력 받기
-[X] UserInputProcessor에서 입력값 재가공 후 RacingCars 생성
-[X] RacingCars를 통해 시도 횟수만큼 시도
    - OutputView에서 실행 결과 출력
    - OutputView에서 차수별 실행 결과 출력
-[X] RacingCars를 통해 우승자 결과 받고 WinnerDto로 변환
    - OutputView에서 우승자 출력

## UserInputProcessor

-[X] 자동차 이름 재가공
    - 자동차 이름 입력에서 이름 추출 및 공백 제거
    - 이름 쉼표(,) 기준으로 구분
-[X] 시도 횟수 재가공
    - 공백 제거

### UserInputProcessorValidator

-[X] 총 시도횟수가 정수 범위를 넘어가거나 음수일 경우
- `IllegalArgumentException` 발생

## InputView

-[X] 자동차 이름 입력 받기
    - 중복, 숫자, 특수기호 허용
    - `경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)`
    - ` camp.nextstep.edu.missionutils.Console의 readLine()` 사용
-[X] 시도할 횟수 입력 받기
    - 0부터 Integer.MaxValue 허용
    - `시도할 횟수는 몇 회인가요?`
    - ` camp.nextstep.edu.missionutils.Console의 readLine()` 사용

### InputViewValidator

-[X] 사용자 입력이 빈 문자열이거나 공백일 경우
-[X] 사용자 입력이 숫자가 아닐 경우
- 사용자 입력이 유효하지 않을 경우 `IllegalArgumentException` 발생

## OutputView

-[X] 실행 결과 출력
    - `실행 결과`
-[X] 차수별 실행 결과 출력
    - `<자동차 이름> : <전진 횟수(-)>`
-[X] 우승자 안내 문구 출력
    - `최종 우승자 : `
    - 우승자가 여러 명일 때는 쉼표 구분