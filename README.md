# docker-vearch-image
docker-vearch-image



## 安装docker服务

```bash
# step 1: 安装必要的一些系统工具
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
 
# Step 2: 添加软件源信息
sudo yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
 
# Step 3: 更新并安装Docker-CE
sudo yum makecache fast
sudo yum -y install docker-ce
 
# Step 4: 开启Docker服务
sudo service docker start
```



## 测试环境



### 运行脚本 

```bash
sh init.sh
```



vearch docker 测试版本

```bash
docker run -itd --name=my_vearch --hostname=my_vearch -p 8817:8817 -p 9001:9002 -p 4101:4101 -v $PWD/config.toml:/vearch/config.toml -v $PWD/datas/:/datas/ registry.cn-hongkong.aliyuncs.com/sunny5156/my_vearch:3.2.6 sh /vearch/plugin/bin/run.sh image
```

  

### 测试服务

```bash
http://127.0.0.1:8817/  # 具体host根据自己情况修改

{
"cluster_name": "vearch",
"cluster_uuid": "",
"version": {
"build_version": "3.2.0",
"build_time": "2020-11-19 07:44.35",
"commit_id": "6e31264e97d05ff12758fe5ad5da0c9412fe28f3"
},
"tagline": "",
"name": "vearch"
}
```

