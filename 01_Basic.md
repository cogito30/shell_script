# Basic

## 1. Hello, World!
1) chmod +x <file_name.sh>
```
#!/bin/bash
ps | grep $$
which bash
echo "Hello, World!"
```

## 2. Variables
- 셀 변수는 숫자, 문자, 문자열, 밑줄(_) 포함
- 변수명은 대소문자 구분
- = 기호 양옆에 공백 불가
- \로 특수 문자 표현
- $변수명으로 변수값 표현
- ${}로 문자열내 변수이름 포함
- ""는 공백 방지
- $()로 명령값 치환
- ``
```
PRICE=5
greeting='Hello World!'
echo "Price is \$PRICE"
echo "${greeting}"

#!/bin/bash
BIRTHDATE="Jan 1, 2000"
Presents=10
BIRTHDAY=`date -d "$BIRTHDATE" +%A`

if [ "$BIRTHDATE" == "Jan 1, 2000" ] ; then
    echo "BIRTHDATE is correct, it is $BIRTHDATE"
else
    echo "BIRTHDATE is incorrect - please retry"
fi
if [ $Presents == 10 ] ; then
    echo "I have received $Presents presents"
else
    echo "Presents is incorrect - please retry"
fi
if [ "$BIRTHDAY" == "Saturday" ] ; then
    echo "I was born on a $BIRTHDAY"
else
    echo "BIRTHDAY is incorrect - please retry"
fi
```

## 3. Passing Arguments to the Script
- $0은 현재 스크립트
- $1은 명령줄의 첫 인자
- $2는 이어지는 두번쨰 인자
- $#은 인자의 개수
- $@ 모든 매개변수를 공백 기준으로 나누어 처리
- $* 모든 파라미터를 한개의 단어로 취급
```
#!/bin/bash
function File {
    echo $#
}

if [ ! $# -lt 1 ]; then
    File $*
    exit 0
fi

bash prog.sh Shell is fun
```

## 4. Arrays
- 배열은 () 안에 공백으로 구분된 값을 할당
- 배열의 총 요소 수는 ${#배열명[@]}로 표기
```
#!/bin/bash
NAMES=( John Eric Jessica )
NUMBERS=( 1 2 3 )
STRINGS=( "hello" "world" )
NumberOfNames=${#NAMES[@]}
second_name=${NAMES[1]}
echo ${NUMBERS[@]}
echo ${STRINGS[@]}
echo "The number of names listed in the NAMES array: $NumberOfNames"
echo "The second name on the NAMES list is:" ${second_name}
```

## 5. Basic Operators
- a+b, a-b, a*b, a/b, a%b, a**b
```
#!/bin/bash
COST_PINEAPPLE=50
COST_BANANA=4
COST_WATERMELON=23
COST_BASKET=1
TOTAL=$(($COST_PINEAPPLE + $COST_BANANA + $COST_WATERMELON + $COST_BASKET))

echo "Total Cost is $TOTAL"
```

## 6. Basic String Operations

```
```

## 7. Decision Making

```
```

## 8. Loops

```
```

## 9. Array-Comparison

```
```

## 10. Shell Functions

```
```
