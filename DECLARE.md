# AI 与第三方声明

## AI 辅助范围

开发过程中使用 OpenAI ChatGPT 与 Codex 协助整理需求和资料，编写或修改网页界面、部分计算参数校验和任务桥接代码，接入后处理脚本，并起草测试与本次提交说明。网页展示的分析数值由计算代码读取轨迹后生成。

验证覆盖现有站点测试、浏览器输入与下载、服务端任务状态和实际产物。RESP 导出使用已完成的五份 PVDF 拟合结果验证，生成的拓扑通过 GROMACS `grompp` 检查。后处理以 320 帧合成轨迹验证上传、计算、图表和 CSV/ZIP 下载。验证针对所列功能与算例范围。

## 第三方组件和资料

| 工具或资料 | 在 AtomLoom 中的用途 |
| --- | --- |
| [RDKit](https://www.rdkit.org/) 与 [OpenChemLib](https://github.com/Actelion/openchemlib) | 化学结构解析与编辑 |
| [Packmol](https://m3g.github.io/packmol/) 与 [Three.js](https://threejs.org/) | 分子装盒与浏览器三维交互 |
| [GROMACS](https://www.gromacs.org/)、[LAMMPS](https://www.lammps.org/) 与 [EMC](https://montecarlo.sourceforge.net/emc/) | 分子动力学运行输入及力场分配 |
| [MDAnalysis](https://www.mdanalysis.org/)、[NumPy](https://numpy.org/)、[SciPy](https://scipy.org/)、[Matplotlib](https://matplotlib.org/) | 轨迹读取、数值分析与绘图 |
| [Gaussian](https://gaussian.com/)、[ORCA](https://www.faccts.de/orca/)、[VASP](https://www.vasp.at/)、[Multiwfn](http://sobereva.com/multiwfn/) 等 | 有相应环境与软件授权时执行量化计算、RESP 与分析 |
| [Cloudflare Workers / D1](https://developers.cloudflare.com/workers/) | 正式网站和任务接口运行环境 |

表中工具由 AtomLoom 正式网站与计算环境使用，按各自许可运行。轨迹后处理参考提交方提供的电解质分析算法。

## 演示数据来源

- `demo/example-input.zip` 中的合成拓扑与轨迹由固定随机种子生成。对应输出来自同一轨迹的实际分析程序运行。
- 正式网站的首页也包含说明性结构、轨迹与参考图。正式站点引用的文献案例包括 Wang 等人的图 4，来源与许可见[原文](https://doi.org/10.1038/s41467-025-67982-0)。文献结果和随包合成算例各自独立。
