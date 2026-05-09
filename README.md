# Umami Analytics Deployment

这是 Umami Analytics 的 Docker 部署配置文件。

## 部署说明

本项目采用官方镜像进行部署，并连接到外部的 Supabase 数据库。

### 环境要求
- Docker
- Docker Compose

### 快速开始

1. **配置环境变量**
   参考 `.env.ghcr.example` 创建 `.env` 文件，并填写您的数据库连接信息（建议使用 Supabase 的直连端口 5432 进行首次迁移，或开启 `SKIP_DB_MIGRATION=1`）。

2. **启动服务**
   ```bash
   docker compose -f docker-compose.ghcr.yml up -d
   ```

3. **访问服务**
   服务默认运行在 `127.0.0.1:3001`。

## 维护

- **升级 Umami**:
  ```bash
  docker compose -f docker-compose.ghcr.yml pull
  docker compose -f docker-compose.ghcr.yml up -d
  ```

---
*Powered by [Umami](https://umami.is/)*
