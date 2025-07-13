# PopQuiz 🎯

**AI驱动的实时演讲互动问答系统**

一个创新的教育科技解决方案，通过AI自动生成问题，让演讲、授课和培训变得更加互动和高效。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5+-blue.svg)](https://www.typescriptlang.org/)

## 🌟 项目亮点

- **🤖 AI智能出题**: 基于讯飞星火AI，自动分析演讲内容生成高质量选择题
- **⚡ 实时互动**: 基于Socket.io的实时问答系统，支持多用户同步
- **📁 多格式支持**: 支持PDF、PPT、Word、音频、视频等多种文件格式
- **📊 数据可视化**: 实时统计分析，提供详细的答题数据和趋势图表
- **👥 多角色管理**: 支持组织者、演讲者、听众三种角色的完整工作流
- **💬 讨论互动**: 每道题目都有专属讨论区，促进深度交流
- **📱 响应式设计**: 完美适配桌面端和移动端设备

## 🎯 应用场景

### 教育培训
- **大学课堂**: 教授可以实时检测学生理解程度，提高课堂参与度
- **企业培训**: 培训师能够及时获得学员反馈，调整培训节奏
- **在线教育**: 增强远程教学的互动性和效果

### 会议演讲
- **技术分享**: 演讲者可以确保听众跟上技术要点
- **产品发布**: 实时了解观众对产品特性的理解程度
- **学术会议**: 促进学者间的深度交流和讨论

## 🚀 快速开始

### 一键部署（推荐）

```bash
# 新机器部署
cd PopQuiz
"Step up\start-popquiz.bat"

# 已有环境快速启动
"Step up\quick-start.bat"
```

### 手动安装

#### 系统要求
- Node.js 18+
- PostgreSQL 13+
- Windows 10/11
- 4GB+ 内存

#### 安装步骤

1. **克隆项目**
```bash
git clone https://github.com/your-username/popquiz.git
cd popquiz
```

2. **安装依赖**
```bash
npm run setup
```

3. **配置环境变量**
```bash
# 复制环境变量模板
cp server/.env.example server/.env
```

4. **设置数据库**
```bash
# 创建数据库
createdb popquiz

# 运行数据库迁移
cd server
npx prisma migrate dev
```

5. **启动服务**
```bash
# 开发模式
npm run dev

# 生产模式
npm run build
npm start
```

## 📁 项目结构

```
PopQuiz/
├── client/                 # Next.js 前端应用
│   ├── src/
│   │   ├── app/            # 页面路由
│   │   ├── components/     # React 组件
│   │   ├── contexts/       # React Context
│   │   ├── lib/           # 工具库
│   │   └── types/         # TypeScript 类型
│   └── package.json
├── server/                 # Node.js 后端服务
│   ├── src/
│   │   ├── routes/        # API 路由
│   │   ├── services/      # 业务逻辑
│   │   ├── middleware/    # 中间件
│   │   └── types/         # TypeScript 类型
│   ├── prisma/            # 数据库模式
│   └── package.json
├── Step up/               # 一键部署脚本
├── develop/               # 开发文档
└── package.json           # 根配置文件
```

## 🛠️ 技术栈

### 前端
- **框架**: Next.js 14 + React 18
- **语言**: TypeScript
- **样式**: Tailwind CSS
- **UI组件**: Radix UI
- **状态管理**: React Context + Hooks
- **实时通信**: Socket.io Client
- **图表**: Chart.js
- **HTTP客户端**: Axios

### 后端
- **运行时**: Node.js 18+
- **框架**: Express.js
- **语言**: TypeScript
- **数据库**: PostgreSQL + Prisma ORM
- **实时通信**: Socket.io
- **认证**: JWT + bcrypt
- **文件处理**: Multer + pdf-parse + mammoth
- **AI服务**: 讯飞星火API
- **安全**: Helmet + CORS

### 开发工具
- **包管理**: npm
- **代码规范**: ESLint + Prettier
- **测试**: Jest
- **构建**: TypeScript Compiler
- **部署**: 自动化脚本

## 🎮 使用指南

### 组织者工作流
1. **创建演讲活动**: 设置演讲基本信息和参与者
2. **邀请演讲者**: 分配演讲者权限和资源
3. **监控活动**: 实时查看参与情况和统计数据
4. **分析报告**: 获取详细的活动效果分析

### 演讲者工作流
1. **上传材料**: 支持PDF、PPT、Word等格式
2. **AI生成题目**: 系统自动分析内容生成选择题
3. **开始演讲**: 实时发布问题给听众
4. **查看反馈**: 获取听众答题情况和建议

### 听众体验
1. **加入演讲**: 通过邀请码或链接参与
2. **实时答题**: 在限定时间内回答问题
3. **查看结果**: 获取个人成绩和排名
4. **参与讨论**: 在题目讨论区交流观点

## 📊 核心功能

### AI智能出题
- 基于讯飞星火大语言模型
- 自动分析文档内容和语音转录
- 生成符合教学目标的选择题
- 支持难度调节和题型定制

### 实时互动系统
- WebSocket长连接保证实时性
- 支持千人同时在线答题
- 自动同步所有用户状态
- 断线重连和状态恢复

### 多模态内容处理
- **文档解析**: PDF、PPT、Word、TXT
- **音频处理**: MP3、WAV语音转文字
- **视频分析**: MP4视频内容提取
- **图像识别**: OCR文字识别

### 数据分析与可视化
- 实时答题统计
- 个人和群体表现分析
- 趋势图表和热力图
- 导出详细报告

## 🔧 配置说明

### 环境变量配置

```env
# 数据库配置
DATABASE_URL="postgresql://username:password@localhost:5432/popquiz"

# JWT密钥
JWT_SECRET="your-super-secret-jwt-key"

# 讯飞星火AI配置
XFYUN_APP_ID="your-app-id"
XFYUN_API_SECRET="your-api-secret"
XFYUN_API_KEY="your-api-key"

# 服务端口
PORT=5000
CLIENT_URL="http://localhost:3000"
```

### 数据库配置

系统使用PostgreSQL作为主数据库，支持以下主要数据模型：

- **用户管理**: 支持组织者、演讲者、听众三种角色
- **演讲管理**: 演讲信息、参与者关系、权限控制
- **问答系统**: 题目、选项、答案、统计数据
- **讨论系统**: 评论、回复、点赞等社交功能

## 🧪 测试

### 运行测试

```bash
# 运行所有测试
npm test

# 前端测试
npm run client:test

# 后端测试
npm run server:test

# 监听模式
npm run test:watch
```

### 测试覆盖

- **单元测试**: 核心业务逻辑测试
- **集成测试**: API接口和数据库交互测试
- **端到端测试**: 完整用户流程测试
- **性能测试**: 并发用户和大数据量测试

## 📈 性能优化

### 前端优化
- React组件懒加载
- 图片和资源压缩
- CDN加速静态资源
- Service Worker缓存

### 后端优化
- 数据库查询优化
- Redis缓存热点数据
- API响应压缩
- 连接池管理

### 实时通信优化
- Socket.io房间管理
- 消息批量处理
- 心跳检测机制
- 负载均衡支持

## 🔒 安全特性

- **身份认证**: JWT令牌 + 密码哈希
- **权限控制**: 基于角色的访问控制(RBAC)
- **数据验证**: 输入验证和SQL注入防护
- **安全头**: Helmet.js安全中间件
- **HTTPS支持**: SSL/TLS加密传输
- **敏感信息**: 环境变量管理

## 🚀 部署指南

### Docker部署

```bash
# 构建镜像
docker-compose build

# 启动服务
docker-compose up -d
```

### 云服务部署

支持部署到以下平台：
- **Vercel**: 前端静态部署
- **Heroku**: 全栈应用部署
- **AWS**: EC2 + RDS部署
- **阿里云**: ECS + RDS部署

## 🤝 贡献指南

我们欢迎所有形式的贡献！

### 开发流程

1. Fork项目到你的GitHub账户
2. 创建功能分支: `git checkout -b feature/amazing-feature`
3. 提交更改: `git commit -m 'Add amazing feature'`
4. 推送分支: `git push origin feature/amazing-feature`
5. 创建Pull Request

### 代码规范

- 遵循ESLint和Prettier配置
- 编写清晰的提交信息
- 添加必要的测试用例
- 更新相关文档

## 📝 更新日志

### v1.0.0 (2025-07-21)
- ✨ 首次发布
- 🎯 完整的AI问答系统
- 📱 响应式用户界面
- 🔄 实时数据同步
- 📊 数据分析功能

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

## 👥 团队

- **项目负责人**: PopQuiz Team
- **前端开发**: 小张 - UI/UX设计与实现
- **后端开发**: 小李 - API与AI集成
- **全栈开发**: 小王 - 系统集成与测试

## 📞 联系我们

- **项目主页**: https://github.com/your-username/popquiz
- **问题反馈**: https://github.com/your-username/popquiz/issues
- **邮箱**: popquiz-team@example.com

## 🙏 致谢

感谢以下开源项目和服务：

- [Next.js](https://nextjs.org/) - React全栈框架
- [Prisma](https://www.prisma.io/) - 现代数据库工具
- [Socket.io](https://socket.io/) - 实时通信库
- [Tailwind CSS](https://tailwindcss.com/) - CSS框架
- [讯飞星火](https://www.xfyun.cn/) - AI语言模型

---

**让每一次演讲都充满互动，让每一次学习都更加高效！** 🎉
