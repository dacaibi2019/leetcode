
```go
package main

import (
	"fmt"
	"strconv"
)

func main()  {
c :=[]int{3,4,5}
d :=[]int{6,7,8}
getResult(c,d)
}

func getResult(c []int,d []int)  {
	sum :=getInter(c)+getInter(d)
	value := Int2Str(sum)
	temp :=reverseString(value)
	result :=Str2Int(temp)
	fmt.Println("结果：",result)
}

func getInter(temp []int)int{
	var ret =0
	for i:=0;i<len(temp);i++{
		ret =temp[len(temp)-i-1]+ret*10
	}
	return ret
}

//整形转字符串
func Int2Str(i int) string {
	return strconv.Itoa(i)
}

//字符串转整形
func Str2Int(s string) int {
	i, _ := strconv.Atoi(s)
	return i
}

func reverseString(s string) string {
	runes := []rune(s)
	for from, to := 0, len(runes)-1; from < to; from, to = from+1, to-1 {
		runes[from], runes[to] = runes[to], runes[from]
	}
	return string(runes)

```

