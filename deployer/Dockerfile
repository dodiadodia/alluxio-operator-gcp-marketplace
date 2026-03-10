# 使用专用的 Helm 部署器
FROM gcr.io/cloud-marketplace-tools/k8s/deployer_helm:latest

# 1. 拷贝 Helm Chart 源代码 (假设你的 chart 在当前目录下)
RUN mkdir -p /data/chart
COPY alluxio-operator.tar.gz /data/chart/

# 2. 拷贝必要的配置文件
COPY schema.yaml /data/schema.yaml
COPY manifest.yaml /data/manifest.yaml

# 3. 指定 Chart 路径环境变量
ENV CHART_PATH=/data/chart/alluxio-operator
