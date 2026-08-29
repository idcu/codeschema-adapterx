# codeschema-adapterx

CodeSchema 解析适配器对外发布契约层（A 级生态资产）。

本仓是 `github.com/idcu/codeschema` 的 `contrib/adapterx` 独立发布抽取版。
**自包含（仅依赖标准库），可独立编译 / 测试 / 发布**，不依赖 `internal/*`。

## 包

`package adapterx` 沉淀 4 个解析适配器（tree-sitter / SCIP / CodeGraph / LSP）
的统一对外契约 `ParserPlugin` 及聚合 `BuiltinAdapters()`。第三方实现
`ParserPlugin` 即可与 CodeSchema 解析流水线无缝对接。

## 使用

```go
import "github.com/idcu/codeschema-adapterx"

// 取内置适配器聚合，或自行实现 ParserPlugin 注入
plugins := adapterx.BuiltinAdapters()
```

## 协议

MIT
