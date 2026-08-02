# docker配置
点开设置， 点开engine
```
{
  "builder": {
    "gc": {
      "defaultKeepStorage": "20GB",
      "enabled": true
    }
  },
  "experimental": false,
  "registry-mirrors": [
    "https://docker.m.daocloud.io",
    "https://mirror.ccs.tencentyun.com",
    "https://docker.nju.edu.cn",
    "https://dockerproxy.com"
  ]
}
```
- 进入docker目录 将.env.example 修改成.env
- 进入dify/docker目录 , 执行命令, docker desktop会提示授权，点同意
```
docker compose up -d
```
- 访问登陆  http://localhost/install 

# 配置本地大模型
- 下载ollama，本地下载跑一个小模型例如 qwen:2.5:3b
- 打开dify页面，配置ollama
```
模型名称： qwen2.5:3b
模型类型： llm
基础url： 本地：http://host.docker.internal:11434, 远程：http://远程ip:11434
```

