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
  <<< Author notes: Step 5 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 5: 在 workflow 文件中引用你的 Action

_干得漂亮! :tada:_

接下来的步骤会把你刚创建的 Action 添加到仓库中已有的工作流文件 [`my-workflow.yml`](/.github/workflows/my-workflow.yml) 中。

### :keyboard: 实操环节: 在 workflow 文件中引用自定义 Action

在 `my-workflow.yml` 文件中添加如下内容：

```yaml
- name: ha-ha
  uses: ./.github/actions/joke-action
```

完整的 workflow 文件示例如下：

```yaml
name: JS Actions

on:
  issues:
    types: [labeled]

jobs:
  action:
    if: ${{ !github.event.repository.is_template }}
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4
      - name: ha-ha
        uses: ./.github/actions/joke-action
```

说明：

* 我们这里使用 `issues` 事件触发，而不是 `pull_request`。
* 移除了之前示例中的 `hello-world` Action。
* `uses: ./.github/actions/joke-action` 指向本地的自定义 Action 目录。

你可以在浏览器中打开 [`my-workflow.yml`](/.github/workflows/my-workflow.yml) 并直接[编辑文件](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)。
记得选择 **Commit directly to the main branch** 以直接提交更改。

等待大约 20 秒后刷新本页面，[GitHub Actions](https://docs.github.com/en/actions) 会自动检测更新，并进入下一步。

<footer>

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/write-javascript-actions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
