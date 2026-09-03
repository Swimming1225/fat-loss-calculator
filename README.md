# 电商KA销售减脂ing · GitHub Pages 版

一个可直接发布到 GitHub Pages 的静态减脂计算器网站：

- 访问者打开网址后自己填写性别、身高、体重、运动量，自动计算每日营养目标；
- 支持按训练日 / 有氧轻训日 / 休息日自动调整碳水目标；
- 内置五类食物库，可记录三餐和加餐；
- 每 10 天记录体重，自动判断减脂速度并给出调整方向；
- 纯前端实现，数据只保存在访问者自己的浏览器本地，无需数据库。

## 目录结构

```text
减脂计算器-github版/
├── index.html                  # 网站首页（唯一页面）
├── README.md                   # 说明文件
└── .github/
    └── workflows/
        └── pages.yml           # GitHub Pages 自动发布配置
```

## 发布到 GitHub Pages

### 方式一：网页上传（不需要安装 Git）

1. 打开 <https://github.com/new>，新建一个仓库（Repository），建议命名为 `fat-loss-calculator`，可见性选 Public；
2. 创建后进入仓库，点击 **Add file → Upload files**；
3. 把本文件夹内的内容全部拖进去，务必让 `index.html` 位于仓库根目录；
4. 提交（Commit changes）；
5. 进入仓库 **Settings → Pages**；
6. 在 **Build and deployment → Source** 中选择 **GitHub Actions**；
7. 等待 1–2 分钟，自动发布完成后会显示网址：

```text
https://你的GitHub用户名.github.io/fat-loss-calculator/
```

把这个网址发给别人即可打开使用。

### 方式二：用 Git 命令行上传

```bash
git init
git add .
git commit -m "feat: 减脂计算器网站版"
git branch -M main
git remote add origin https://github.com/你的用户名/fat-loss-calculator.git
git push -u origin main
```

推送完成后，按“方式一”的第 5–7 步在仓库 Settings → Pages 中选择 GitHub Actions 即可。

> 仓库名不一定要叫 `fat-loss-calculator`。网址里的仓库名会随实际仓库名变化。

## 以后如何更新

直接用文本编辑器修改 `index.html`，保存后重新上传覆盖同名文件，或再次 `git push`。工作流会自动重新发布，网址不变。

## 注意事项

- 内容定位是“饮食记录与参考计算工具”，请不要在页面中加入诊断、治疗、保证减重效果等表述，以免影响审核或引发误导。
- 每个访问者的数据保存在他自己的浏览器本地；清除浏览器数据或更换浏览器后记录会清空。
- 本项目不包含后端，也没有用户数据上传，因此适合直接部署到 GitHub Pages。
