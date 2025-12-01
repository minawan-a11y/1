# 🚀 GitHub Pages 部署指南

将 VOC 分析报告部署为在线网站的完整步骤。

---

## 📋 前提条件

- ✅ 拥有 GitHub 账号（没有的话去 https://github.com 注册）
- ✅ 已安装 Git（检查：在终端输入 `git --version`）

---

## 🎯 部署步骤（5分钟完成）

### 步骤 1: 在 GitHub 上创建新仓库

1. **登录 GitHub**: 访问 https://github.com 并登录
2. **创建新仓库**:
   - 点击右上角 `+` 号 → 选择 `New repository`
   - **仓库名称**: 建议使用 `voc-analysis-report` 或 `solix-voc-report`
   - **描述**: `SOLIX/Anker VOC Analysis Report - User Feedback Insights`
   - **可见性**: 选择 `Public`（公开，这样才能使用免费的 GitHub Pages）
   - **不要勾选**: "Add a README file"、"Add .gitignore"、"Choose a license"
3. **点击**: `Create repository`

---

### 步骤 2: 推送代码到 GitHub

复制 GitHub 页面上显示的 **HTTPS** 地址（类似：`https://github.com/YOUR-USERNAME/voc-analysis-report.git`）

然后在**终端**中执行以下命令：

```bash
# 1. 进入项目文件夹
cd /Users/anker/Downloads/voc-report-website

# 2. 添加远程仓库（把下面的 URL 替换成你的）
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# 3. 推送代码到 GitHub
git branch -M main
git push -u origin main
```

**示例**（假设你的用户名是 `john-doe`，仓库名是 `voc-analysis-report`）：
```bash
git remote add origin https://github.com/john-doe/voc-analysis-report.git
git branch -M main
git push -u origin main
```

> 💡 **首次推送可能需要输入 GitHub 用户名和密码/token**

---

### 步骤 3: 启用 GitHub Pages

1. **进入仓库设置**:
   - 在 GitHub 仓库页面，点击 `Settings`（设置）

2. **找到 Pages 选项**:
   - 在左侧菜单中，找到并点击 `Pages`

3. **配置发布源**:
   - **Source**: 选择 `Deploy from a branch`
   - **Branch**: 选择 `main`
   - **文件夹**: 选择 `/ (root)`
   - 点击 `Save`（保存）

4. **等待部署**:
   - 大约 1-2 分钟后，页面会显示：
   ```
   ✅ Your site is live at https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
   ```

---

## 🎉 完成！访问你的网站

你的 VOC 分析报告现在可以通过以下地址访问：

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

例如：
- 用户名：`john-doe`
- 仓库名：`voc-analysis-report`
- 网址：`https://john-doe.github.io/voc-analysis-report/`

---

## 🔄 如何更新网站

如果你修改了报告，更新网站只需：

```bash
cd /Users/anker/Downloads/voc-report-website

# 添加修改
git add .

# 提交修改
git commit -m "Update report"

# 推送到 GitHub
git push
```

**等待 1-2 分钟，网站会自动更新！**

---

## ❓ 常见问题

### Q1: 推送时要求输入用户名和密码？

**答**: GitHub 已不再支持密码登录，需要使用 Personal Access Token：

1. 访问 https://github.com/settings/tokens
2. 点击 `Generate new token (classic)`
3. 勾选 `repo` 权限
4. 生成 token 并**保存**（只显示一次）
5. 推送时，用户名输入 GitHub 用户名，密码输入刚才的 token

### Q2: 网站显示 404 Not Found？

**答**: 可能原因：
- 等待时间不够（通常需要 1-2 分钟）
- 确认 GitHub Pages 已启用（Settings → Pages）
- 确认分支选择正确（应该是 `main`）
- 确认文件名是 `index.html`（已经是了）

### Q3: 图表没有显示？

**答**: 检查：
- `charts/` 文件夹是否已推送到 GitHub
- 在 GitHub 仓库页面查看是否有 `charts/` 目录
- 图片路径是否正确（当前使用相对路径 `charts/xxx.png`）

### Q4: 想使用自定义域名？

**答**:
1. 购买域名（如 `voc-report.com`）
2. 在域名 DNS 设置中添加 CNAME 记录，指向 `YOUR-USERNAME.github.io`
3. 在 GitHub Pages 设置中输入自定义域名

---

## 📚 更多资源

- [GitHub Pages 官方文档](https://docs.github.com/en/pages)
- [Git 基础教程](https://git-scm.com/book/zh/v2)
- [Markdown 语法](https://www.markdownguide.org/basic-syntax/)

---

## 🆘 需要帮助？

如果遇到问题，可以：
1. 检查 GitHub 仓库的 Actions 选项卡，查看部署日志
2. 在终端运行 `git status` 查看当前状态
3. 确保所有文件都已提交：`git log` 查看提交历史

---

**祝你部署成功！🎉**
