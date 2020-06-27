
## 目标功能

- http框架
    - [x] [gin] (web框架)
    - [ ] validate
- 权限
    - [ ] JWT
    - [ ] [Casbin] (鉴权)
- 日志
    - [ ] Metrics
    - [ ] Access Log
    - [ ] Tracing Opentracing+TraceID
- 配置中心
    - [ ] XConf
- 领域驱动
	- [x] 整洁架构
- ORM
	- [x] gorm

- 发布
	- [ ] 灰度
	- [ ] 蓝绿
	    - *注:由于 micro 默认的 api 和 web 网关均不支持**服务筛选**，需要自己改造，方案参考[微服务协作开发、灰度发布之流量染色](http://hbchen.com/post/microservice/2019-11-30-go-micro-service-chain/)，此方案仅适用于测试，具体 asim 在 [PR#1388](https://github.com/micro/go-micro/pull/1388) 给了反馈，但可以自定义 Router 实现*
	    - 自定义 Router 实现网关对服务筛选的支持，因为 micro 有 internal 库所以需要在 micro 内实现，参考我 fork 的分支版本 [hb-chen/micro/gateway](https://github.com/hb-chen/micro/tree/gateway-2.4.0/gateway)，[gateway](gateway) 模块使用的便是此方案，可以快速实现流量染色
- 部署
	- K8S
		- [ ] [helm](/deploy/k8s/helm)
	- [ ] Docker
	    - 示例[console](/console/docker-compose.yml)
- 安全
- CI/CD
	- [Drone](https://drone.io/) [README](/deploy/docker/drone)
	    - [ ] Go & Node编译
	    - [ ] Docker镜像
	    - [ ] Kubernetes发布
	    - [ ] 缓存
	- [ ] Jenkins
- 基础服务
	- 日志收集
	    - [Fluentbit](https://fluentbit.io/) + Elasticsearch
		    - [ ] [docker-compose](/console/docker-compose-fb-es.yml)
		    - [ ] Kubernetes
	- [ ] 监控告警
		- Prometheus
		- Grafana
	- [ ] Tracing
		- Jaeger
- ...

