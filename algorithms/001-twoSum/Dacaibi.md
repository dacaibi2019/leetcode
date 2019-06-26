
```go

package main

import (
	"fmt"
	"strconv"
)

func main()  {
a :=[]int{1,3,4,78,9,10,22,13,34}
var b = 13
getele(a,b)

}

func getele(a []int,b int)  {
	result :=make(map[int]int)
	myMap := make(map[int]int)
	temp :=make(map[int]int)
	data :=make([]int,0)
	for i,v :=range a{
		myMap[v]=i
	}

	for j,value :=range a {
		ret :=b-value
		if _, ok := myMap[ret]; ok {
			temp[j]=myMap[ret]
		}
	}
	for key,value := range temp{
		if key < value{
			result[key]=value
		}else {
			result[value]=key
		}
	}
	fmt.Println(result)
	for i,v :=range result{
		data =append(data,i)
		data = append(data,v)
	}
	fmt.Println("结果：",data)
}
```

