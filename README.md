# 图标集成服务器 Hugeicons

Hugeicons MCP Server是一个基于TypeScript的服务器，提供Hugeicons图标库的集成工具和资源，支持多种平台的图标搜索、获取和使用指南。
Hugeicons MCP Server is a TypeScript based server that provides integrated tools and resources for the Hugeicons icon library, supporting icon search, retrieval, and usage guides for multiple platforms.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| list_icons | Get a list of all available Hugeicons icons |
| search_icons | Search for icons by name or tags. Use commas to search for multiple icons (e.g. 'home, notification, settings') |
| get_platform_usage | Get platform-specific usage instructions for Hugeicons |
| get_icon_glyphs | Get all glyphs (unicode characters) for a specific icon across all available styles |
| get_icon_glyph_by_style | Get the glyph (unicode character) for a specific icon with a particular style |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659866627](https://mcp.xiaobenyang.com/inspector/1777316659866627)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659866627](https://mcp.xiaobenyang.com/inspector/1777316659866627)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "图标集成服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659866627/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "图标集成服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659866627/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "图标集成服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659866627",
          },
          "transport": "stdio"
        }
      }
}

```
