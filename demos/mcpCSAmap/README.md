# McpCSAmap

高德地图 MCP client & server

![](imgs/2025-05-22-22-26-03.png)

## Workflow

### Common

- AI agent: 接入 DeepSeek + 高德 MCP server

### As Client

- 通过聊天窗口触发

### As Server

- 给 cursor agent 使用

## 通过聊天窗口触发

![](imgs/2025-05-22-21-26-19.png)

## AI agent llm

![](imgs/2025-05-22-21-27-44.png)
![](imgs/2025-05-22-21-28-04.png)
![](imgs/2025-05-22-21-28-21.png)

## Amap MCP

![](imgs/2025-05-22-21-31-13.png)
![](imgs/2025-05-22-21-31-26.png)
![](imgs/2025-05-22-21-31-38.png)

- 创建 MCP list tools 节点

![](imgs/2025-05-22-21-32-29.png)
![](imgs/2025-05-22-21-35-10.png)

- 高德 MCP: https://lbs.amap.com/api/mcp-server/gettingstarted

- API Key: https://console.amap.com/dev/key/app

![](imgs/2025-05-22-21-38-22.png)
![](imgs/2025-05-22-21-38-56.png)
![](imgs/2025-05-22-21-41-09.png)

- 创建 Execute Tool 节点

![](imgs/2025-05-22-21-42-44.png)
![](imgs/2025-05-22-21-45-58.png)

## 作为 MCP Client

- 通过第一个 chat 节点提问

![](imgs/2025-05-22-21-52-37.png)

## 作为 MCP Server

- 为 AI Agent 添加外部 workflow 的 Trigger

![](imgs/2025-05-22-21-56-33.png)
![](imgs/2025-05-22-21-57-21.png)

- input schema name 需要是 'chatInput'，为了与 AI Agent 接收的参数保持一致
![](imgs/2025-05-22-21-58-53.png)
![](imgs/2025-05-22-21-59-22.png)


- 添加 MCP Server Trigger（记得先保存 workflow Trigger）

![](imgs/2025-05-22-21-53-34.png)
![](imgs/2025-05-22-21-54-27.png)
![](imgs/2025-05-22-21-55-15.png)
![](imgs/2025-05-22-22-06-39.png)
![](imgs/2025-05-22-22-19-08.png)

- 将 SSE 服务配置到 cursor

![](imgs/2025-05-22-22-20-04.png)
![](imgs/2025-05-22-22-20-20.png)
![](imgs/2025-05-22-22-22-12.png)
![](imgs/2025-05-22-22-22-29.png)
![](imgs/2025-05-22-22-23-59.png)

- 生产 SSE: 生产环境可以用 Production URL

![](imgs/2025-05-22-22-25-20.png)