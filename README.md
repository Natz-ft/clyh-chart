# Chart



##1. 初始化Chart





## 2. 新增应用约束

### 1.命名规范	


1. Deployment:    xxxxxx.yaml

1. ConfigMap:  xxxxx-configmap.yaml

1. Service: xxxxxx-svc.yaml

1. PersistentVolumeClaim: xxxxxx-pvc.yaml

1. StatefulSet: xxxxx-statefulset.yaml

1. DaemonSet: xxxxxx-daemonset.yaml

###     2.Configuration

| Parameter                                         | Description                                                                        | Default                                                          |
| ------------------------------------------------- | -------------------------------                                                    | ---------------------------------------------------------------- |
| `imageRegistry`                                           | 镜像仓库   | `registry.cn-chengdu.aliyuncs.com/517la_product2`                                       |
| `dockerTag`                                 | 全局版本号(适用于本地化时每个镜像包都是同一个版本号时)                                                         | `{VERSION}`                                                   |
| `environment`                                   | 应用程序环境(formal:正式环境 test:测试环境)                                              | `formal:正式环境 test:测试环境`                                                      |
| `hostManager.volumes.hostPath`                                    | 应用程序hostpath挂载盘,默认是/app                                                | `hard`                                                           |
| `configMapManger.db.serviceroute.url`                   | 服务路由mysql连接  | `1`                                                              |
| `configMapManger.db.serviceroute.username`                         |服务路由mysql用户名   | `requests:memory=256Mi,cpu=10m,limits:memory=2048Mi,cpu=1000m`   |
| `configMapManger.db.serviceroute.password`                          |服务路由mysql密码   | `1`                                                              |
| `configMapManger.db.writeroute.url`                   | 数据路由mysql写连接  | `1`                                                              |
| `configMapManger.db.writeroute.username`                         |  数据路由mysql写账号  | `requests:memory=256Mi,cpu=10m,limits:memory=2048Mi,cpu=1000m`   |
| `configMapManger.db.writeroute.password`            |数据路由mysql写密码   | `1`                                                              |
| `configMapManger.db.readroute.url`                  | 数据路由mysql读连接  | `requests:memory=256Mi,cpu=10m,limits:memory=2048Mi,cpu=1000m`   |
| `configMapManger.db.readroute.username`                | 数据路由mysql读账号  | `1`                                                              |
| `configMapManger.db.readroute.password`                       |数据路由mysql读密码   | `2`                                                              |
| `configMapManger.redis.url`                 |redis地址   | `false`                                                          |
| `configMapManger.redis.username`                      | redis用户名  | `requests:memory=2048Mi,cpu=1000m,limits:memory=2048Mi,cpu=1000m`|
| `configMapManger.redis.password`                    |redis密码   | `false`                                                          | 
| `configMapManger.redis.dbname`               | redis库  | `-`                                                              |
| ``                 |   | `ReadWriteOnce`                                                  |
| ``                       |   | `50Gi`                                                           |
| ``                    |   | `false`                                                          | 
| ``               |   | `-`                                                              |
| ``                 |   | `ReadWriteOnce`                                                  |
| ``                       |   | `200Gi`                                                          |





