[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/funnythingfunnylove-mcp-server-v2ex-badge.png)](https://mseep.ai/app/funnythingfunnylove-mcp-server-v2ex)

# Mcp-server-v2ex

## Description
This mcp server simply wrap the offical Api 2.0, implement all api actions.


## Feature
- notifications  获取最新提醒
- delete notifications 删除指定提醒
- member profile   获取当前用户档案 即生成token的用户
- token    查看当前的token
- create new token  生成新token
- nodes   获取指定节点
- nodes topics  获取指定节点下的话题
- topic detail  获取指定话题的内容
- topic comments  获取指定话题下的回复

## How to use
- 在 https://www.v2ex.com/settings/tokens 获取 token
- Install the Pakcage via npm
```
  npm install -g mcp-server-v2ex
```
- 在 claude 的 config 的 json 中添加
```
  "v2ex": 
    {"command": "%APP_DATA%\\local\\nvm\\v22.14.0\\node.exe",
     "args": ["%APP_DATA%\\Local\\nvm\\v22.14.0\\node_modules\\mcp-server-v2ex\\dist\\index.js"],
      "env": {
         "V2EX_API_KEY": "{替换自己的 token}",
          "NODE_TLS_REJECT_UNAUTHORIZED": "0" // 如运用了 surge 之类的 MitM
      }
     }
```

## Change log
- v0.1.1  /  2025.04.02
    - 新增今日热点总结
    ![img](./img/v2ex_today_summerize.png)
- v0.1.0
    - 完成基本功能实现

## Plan
- Considering add daily hot topic simply via ask what hot topic in v2ex in claude desktop.

---
