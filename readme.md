# golang-sl-json

json 防腐层，以便将来切换 json 的相关实现

## 使用
```go
package main
import json "github.com/ijustyce/go-sl-json"

func main() {

	json.Marshal()
	json.Unmarshal()
	json.MarshalIndent()
	json.NewDecoder()
	json.Marshal()
}
```
支持以上 5 个方法，最终均调用 encoding/json 里对应的方法，相关实现参考 gin，具体如下：
```go
package json

import "encoding/json"

var (
	Marshal       = json.Marshal
	Unmarshal     = json.Unmarshal
	MarshalIndent = json.MarshalIndent
	NewDecoder    = json.NewDecoder
	NewEncoder    = json.NewEncoder
)
```