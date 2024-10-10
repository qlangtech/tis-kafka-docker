* 启动docker 实例

  ``` shell
   docker-compose up -d
  ```

* 编辑hosts： vi /etc/hosts

   ``` shell
    192.168.28.201 kafkabroker
   ```

* 开启kafka 消息监听

  ``` shell
  kcat -b kafkabroker:9092 -t test  -C
  ```

* 参考

  - hudi上有一个现成的基于docker的kafka启动方案： https://hudi.apache.org/docs/docker_demo/
  - github里有一个专门的docker kafka 方案，不过需要在本地build docker image，愣是没有构建成功，作罢了
