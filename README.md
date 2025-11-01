# Youreln素材共享平台

一个专为大疆OSMO Nano相机用户设计的素材分享平台，支持按日期查询、下载共享的摄影素材，并提供用户权限管理功能。

## 功能特点

### 前台功能
- 按日期和类别筛选素材
- 用户鉴权后下载素材
- 响应式设计，适配各种设备

### 后台功能
- 素材管理：添加、编辑、删除素材信息
- 用户管理：添加、删除用户
- 系统设置：修改管理员密码

## 技术栈

- **前端**：HTML5, CSS3, JavaScript (ES6+), Tailwind CSS v3, Font Awesome
- **后端**：LeanCloud (BaaS平台，提供数据存储和用户认证)
- **部署**：GitHub Pages

## 项目结构

```
/
├── index.html          # 前台页面
├── admin-login.html    # 后台登录页面
├── admin.html          # 后台管理页面
└── README.md           # 项目说明文档
```

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/yourusername/youreln-material-sharing.git
cd youreln-material-sharing
```

### 2. 配置LeanCloud

1. 注册/登录 [LeanCloud](https://leancloud.cn/)
2. 创建应用
3. 在应用设置中获取 AppID、AppKey 和服务器地址
4. 修改代码中的 LeanCloud 配置：

```javascript
AV.init({
    appId: '你的AppID',
    appKey: '你的AppKey',
    serverURL: '你的服务器地址'
});
```

### 3. 创建数据模型

在 LeanCloud 中创建以下数据表：

#### Material 表（素材表）
- `title` (String): 素材标题
- `description` (String): 素材描述
- `date` (Date): 拍摄日期
- `category` (String): 素材类别
- `thumbnail` (String): 缩略图URL
- `cloudLink` (String): 云盘链接

#### User 表（用户表）
- `username` (String): 用户名
- `isAdmin` (Boolean): 是否为管理员

#### Setting 表（系统设置表）
- `adminPassword` (String): 管理员密码

### 4. 部署到GitHub Pages

1. 将项目推送到GitHub仓库
2. 在仓库设置中启用GitHub Pages
3. 选择分支和目录（通常为 `main` 分支和 `/` 目录）
4. 保存设置，等待部署完成

## 默认账户

- **管理员密码**：Youreln（首次登录后建议修改）
- **测试用户**：admin, user1, user2, test

## 浏览器支持

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

## 许可证

MIT License