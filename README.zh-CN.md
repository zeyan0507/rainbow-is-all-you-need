<div align="center">

<img src="assets/banner.svg" alt="Rainbow is All You Need" width="800"/>

[![所有贡献者](https://img.shields.io/badge/all_contributors-6-orange.svg?style=flat-square)](#contributors)

</div>

# Rainbow is All You Need 中文说明

这是一个从 DQN 逐步讲解到 Rainbow 的强化学习教程。
每一章都包含理论背景和面向对象的代码实现，你可以选择自己感兴趣的主题开始学习！通过 [molab](https://molab.marimo.io/)，你可以直接在云端运行这些教程，无需在本地配置环境。

本项目基于 [marimo](https://marimo.io/) 构建。marimo 是一种响应式 Python 笔记本，以纯 `.py` 文件保存和运行，便于复现实验、查看 Git 差异，并提供交互式界面。

如果你有改进项目的想法，欢迎提交 Issue 或 Pull Request。:)

> 如果你想学习策略梯度方法，请参阅 [PG is All You Need](https://github.com/MrSyee/pg-is-all-you-need)。

## 目录

01. 深度 Q 网络（DQN）[[源码](01_dqn.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/01_dqn.py)]
02. 双重深度 Q 网络（Double DQN）[[源码](02_double_q.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/02_double_q.py)]
03. 优先经验回放（Prioritized Experience Replay，PER）[[源码](03_per.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/03_per.py)]
04. 对偶网络（Dueling Network）[[源码](04_dueling.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/04_dueling.py)]
05. 噪声网络（NoisyNet）[[源码](05_noisy_net.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/05_noisy_net.py)]
06. 类别分布式 DQN（Categorical DQN）[[源码](06_categorical_dqn.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/06_categorical_dqn.py)]
07. N 步学习（N-step Learning）[[源码](07_n_step_learning.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/07_n_step_learning.py)]
08. Rainbow [[源码](08_rainbow.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/08_rainbow.py)]
09. Rainbow IQN（结合隐式分位数网络）[[源码](09_rainbow_iqn.py)] [[在线预览](https://molab.marimo.io/github/Curt-Park/rainbow-is-all-you-need/blob/master/09_rainbow_iqn.py)]

> 在预览页面点击 **“Run in molab”**，即可打开交互式会话，编辑并运行笔记本。

## 环境准备

以下命令与英文原文一致，使用 Bash 风格的 Shell：

```bash
# 安装 mise
curl https://mise.run | sh

# 克隆项目
git clone https://github.com/Curt-Park/rainbow-is-all-you-need.git
cd rainbow-is-all-you-need

# 安装 Python、创建虚拟环境并安装 Python 依赖
make init
make setup
```

## 运行方法

运行任意一个笔记本并进行实验，例如：

```bash
make run notebook=01_dqn.py
```

将 `01_dqn.py` 替换为目录中其他章节的文件名，即可运行对应的教程。

## 开发

```bash
make format    # 格式化代码
make lint      # 检查代码规范
```

## 相关论文

以下保留论文的英文题名，便于检索，并附上中文译名：

01. [V. Mnih 等，"Human-level control through deep reinforcement learning." Nature, 518(7540):529–533, 2015.](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)（通过深度强化学习实现人类水平的控制）
02. [van Hasselt 等，"Deep Reinforcement Learning with Double Q-learning." arXiv 预印本 arXiv:1509.06461, 2015.](https://arxiv.org/pdf/1509.06461.pdf)（结合双重 Q 学习的深度强化学习）
03. [T. Schaul 等，"Prioritized Experience Replay." arXiv 预印本 arXiv:1511.05952, 2015.](https://arxiv.org/pdf/1511.05952.pdf)（优先经验回放）
04. [Z. Wang 等，"Dueling Network Architectures for Deep Reinforcement Learning." arXiv 预印本 arXiv:1511.06581, 2015.](https://arxiv.org/pdf/1511.06581.pdf)（用于深度强化学习的对偶网络架构）
05. [M. Fortunato 等，"Noisy Networks for Exploration." arXiv 预印本 arXiv:1706.10295, 2017.](https://arxiv.org/pdf/1706.10295.pdf)（用于探索的噪声网络）
06. [M. G. Bellemare 等，"A Distributional Perspective on Reinforcement Learning." arXiv 预印本 arXiv:1707.06887, 2017.](https://arxiv.org/pdf/1707.06887.pdf)（从分布视角看强化学习）
07. [R. S. Sutton，"Learning to predict by the methods of temporal differences." Machine Learning, 3(1):9–44, 1988.](http://incompleteideas.net/papers/sutton-88-with-erratum.pdf)（通过时序差分方法学习预测）
08. [M. Hessel 等，"Rainbow: Combining Improvements in Deep Reinforcement Learning." arXiv 预印本 arXiv:1710.02298, 2017.](https://arxiv.org/pdf/1710.02298.pdf)（Rainbow：融合深度强化学习的多项改进）
09. [W. Dabney 等，"Implicit Quantile Networks for Distributional Reinforcement Learning." arXiv 预印本 arXiv:1806.06923, 2018.](https://arxiv.org/pdf/1806.06923.pdf)（用于分布式强化学习的隐式分位数网络）

<a id="contributors"></a>

## 贡献者

感谢以下贡献者（[表情符号含义](https://allcontributors.org/docs/en/emoji-key)）：

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://www.linkedin.com/in/curt-park/"><img src="https://avatars3.githubusercontent.com/u/14961526?v=4?s=100" width="100px;" alt="Jinwoo Park (Curt)"/><br /><sub><b>Jinwoo Park (Curt)</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=Curt-Park" title="Code">💻</a> <a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=Curt-Park" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.linkedin.com/in/kyunghwan-kim-0739a314a/"><img src="https://avatars3.githubusercontent.com/u/17582508?v=4?s=100" width="100px;" alt="Kyunghwan Kim"/><br /><sub><b>Kyunghwan Kim</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=MrSyee" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/Wei-1"><img src="https://avatars0.githubusercontent.com/u/10698262?v=4?s=100" width="100px;" alt="Wei Chen"/><br /><sub><b>Wei Chen</b></sub></a><br /><a href="#maintenance-Wei-1" title="Maintenance">🚧</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/wlbksy"><img src="https://avatars1.githubusercontent.com/u/2433806?v=4?s=100" width="100px;" alt="WANG Lei"/><br /><sub><b>WANG Lei</b></sub></a><br /><a href="#maintenance-wlbksy" title="Maintenance">🚧</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://www.tun6.com/"><img src="https://avatars.githubusercontent.com/u/10635308?v=4?s=100" width="100px;" alt="leeyaf"/><br /><sub><b>leeyaf</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=leeyaf" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/AFanaei"><img src="https://avatars.githubusercontent.com/u/5231504?v=4?s=100" width="100px;" alt="ahmadF"/><br /><sub><b>ahmadF</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=AFanaei" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/robertoschiavone"><img src="https://avatars.githubusercontent.com/u/5054879?v=4?s=100" width="100px;" alt="Roberto Schiavone"/><br /><sub><b>Roberto Schiavone</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=robertoschiavone" title="Code">💻</a></td>
    </tr>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/DaivdYuan"><img src="https://avatars.githubusercontent.com/u/47169162?v=4?s=100" width="100px;" alt="David Yuan"/><br /><sub><b>David Yuan</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=DaivdYuan" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/dhanushka2001"><img src="https://avatars.githubusercontent.com/u/79731347?v=4?s=100" width="100px;" alt="dhanushka2001"/><br /><sub><b>dhanushka2001</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=dhanushka2001" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://pierre-couy.dev"><img src="https://avatars.githubusercontent.com/u/11176108?v=4?s=100" width="100px;" alt="Pierre Couy"/><br /><sub><b>Pierre Couy</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=pcouy" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://anthropic.com/claude-code"><img src="https://avatars.githubusercontent.com/u/81847?v=4?s=100" width="100px;" alt="Claude"/><br /><sub><b>Claude</b></sub></a><br /><a href="https://github.com/Curt-Park/rainbow-is-all-you-need/commits?author=claude" title="Code">💻</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

本项目遵循 [all-contributors](https://github.com/all-contributors/all-contributors) 规范，欢迎任何形式的贡献！
