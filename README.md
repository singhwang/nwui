# nwui

[![Gitter](https://img.shields.io/badge/GITTER-JOIN%20CHAT%20%E2%86%92-brightgreen.svg?style=flat)](https://gitter.im/go-nwui/nwui?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Go Walker](https://img.shields.io/badge/Go%20Walker-API%20Documentation-green.svg?style=flat)](https://gowalker.org/github.com/go-nwui/nwui)
[![GoDoc](https://img.shields.io/badge/GoDoc-API%20Documentation-blue.svg?style=flat)](http://godoc.org/github.com/go-nwui/nwui)

node-webkit UI for Go

## Screenshot

![screenshot](screenshot.png)

## Example

创建一个包含按钮的窗口：

```go
&Window{
	Title:  "window",
	Width:  800,
	Height: 600,
	OnExit: func() {
		fmt.Println("exit")
	},
	Controls: []interface{}{
		&Button{
			ID:   "btn0",
			Text: "button",
			OnClick: func() {
				text := GetConByID("btn0").(*Button).Text
				fmt.Println(text, "clicked!")
			},
		},
	},
}
```
