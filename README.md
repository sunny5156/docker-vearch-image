# docker-vearch-image
docker-vearch-image



## 安装docker服务



## 下载测试环境



### 运行脚本 

```bash
sh init.sh
```



vearch docker 测试版本

```bash
docker run -itd --name=my_vearch --hostname=my_vearch -p 8817:8817 -p 9001:9002 -p 4101:4101 -v $PWD/config.toml:/vearch/config.toml -v $PWD/datas/:/datas/ registry.cn-hongkong.aliyuncs.com/sunny5156/my_vearch:3.2.6 sh /vearch/plugin/bin/run.sh image
```

  