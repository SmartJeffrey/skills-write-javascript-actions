<header>

<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses MIT license.
-->

[English](https://github.com/skills/write-javascript-actions) | 中文

> 本课程翻译自 Github Skills，全部课程请点击 [这里查看](https://www.github-zh.com/getting-started)

# 编写 JavaScript Actions

_编写属于自己的 GitHub JavaScript Action，用它来自动化你的工作流程。_

</header>

<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 2: 配置你的 Action

_很好! 继续 :bike:_

我们已经完成前期准备工作，接下来就来创建我们的 **joke-action** 吧。

### :keyboard: 实操环节

接下来的所有步骤都在 `.github/actions/joke-action` 目录下进行。

我们先定义 Action 所**必需的参数**，后续随着功能演进，再逐步添加可选参数。

1. 在 `.github/actions/joke-action` 目录下创建一个新文件 `action.yml`
2. 打开该文件并添加以下内容：

   ```yaml
   name: "my joke action"

   description: "use an external API to retrieve and display a joke"

   runs:
     using: "node16"
     main: "main.js"
   ```

   这段配置的含义是：

   * `name`：Action 的名称（这里叫“my joke action”）；
   * `description`：Action 的简单描述；
   * `runs`：定义运行环境为 Node.js 16，并指定入口文件为 `main.js`。

3. 保存 `action.yml` 文件。
4. 将修改提交并推送到 `main` 分支：

   ```shell
   git add action.yml
   git commit -m 'create action.yml'
   git pull
   git push
   ```

5. 等待大约 20 秒后刷新本页面。[GitHub Actions](https://docs.github.com/en/actions) 会自动检测更新，并跳转到下一步。

<footer>

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/write-javascript-actions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
