<div align="center">

# ComfyUI
**最强大且模块化的可视化AI引擎和应用程序。**


[![Website][website-shield]][website-url]
[![Dynamic JSON Badge][discord-shield]][discord-url]
[![Twitter][twitter-shield]][twitter-url]
[![Matrix][matrix-shield]][matrix-url]
<br>
[![][github-release-shield]][github-release-link]
[![][github-release-date-shield]][github-release-link]
[![][github-downloads-shield]][github-downloads-link]
[![][github-downloads-latest-shield]][github-downloads-link]

[matrix-shield]: https://img.shields.io/badge/Matrix-000000?style=flat&logo=matrix&logoColor=white
[matrix-url]: https://app.element.io/#/room/%23comfyui_space%3Amatrix.org
[website-shield]: https://img.shields.io/badge/ComfyOrg-4285F4?style=flat
[website-url]: https://www.comfy.org/
<!-- Workaround to display total user from https://github.com/badges/shields/issues/4500#issuecomment-2060079995 -->
[discord-shield]: https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2Fcomfyorg%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&logo=discord&logoColor=white&label=Discord&color=green&suffix=%20total
[discord-url]: https://www.comfy.org/discord
[twitter-shield]: https://img.shields.io/twitter/follow/ComfyUI
[twitter-url]: https://x.com/ComfyUI

[github-release-shield]: https://img.shields.io/github/v/release/comfyanonymous/ComfyUI?style=flat&sort=semver
[github-release-link]: https://github.com/comfyanonymous/ComfyUI/releases
[github-release-date-shield]: https://img.shields.io/github/release-date/comfyanonymous/ComfyUI?style=flat
[github-downloads-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/total?style=flat
[github-downloads-latest-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/latest/total?style=flat&label=downloads%40latest
[github-downloads-link]: https://github.com/comfyanonymous/ComfyUI/releases

![ComfyUI Screenshot](https://github.com/user-attachments/assets/7ccaf2c1-9b72-41ae-9a89-5688c94b7abe)
</div>

ComfyUI让您可以使用基于图形/节点/流程图的界面设计和执行高级稳定扩散管道。支持Windows、Linux和macOS。

## 开始使用

#### [桌面应用程序](https://www.comfy.org/download)
- 最简单的入门方式。
- 支持Windows和macOS。

#### [Windows便携包](#installing)
- 获取最新提交且完全便携。
- 支持Windows。

#### [手动安装](#manual-install-windows-linux)
支持所有操作系统和GPU类型（NVIDIA、AMD、Intel、Apple Silicon、昇腾）。

## [示例](https://comfyanonymous.github.io/ComfyUI_examples/)
查看[示例工作流](https://comfyanonymous.github.io/ComfyUI_examples/)了解ComfyUI的功能。

## 功能特性
- 节点/图形/流程图界面，无需编码即可实验和创建复杂的稳定扩散工作流。
- 图像模型
   - SD1.x, SD2.x ([unCLIP](https://comfyanonymous.github.io/ComfyUI_examples/unclip/))
   - [SDXL](https://comfyanonymous.github.io/ComfyUI_examples/sdxl/), [SDXL Turbo](https://comfyanonymous.github.io/ComfyUI_examples/sdturbo/)
   - [Stable Cascade](https://comfyanonymous.github.io/ComfyUI_examples/stable_cascade/)
   - [SD3 和 SD3.5](https://comfyanonymous.github.io/ComfyUI_examples/sd3/)
   - Pixart Alpha 和 Sigma
   - [AuraFlow](https://comfyanonymous.github.io/ComfyUI_examples/aura_flow/)
   - [HunyuanDiT](https://comfyanonymous.github.io/ComfyUI_examples/hunyuan_dit/)
   - [Flux](https://comfyanonymous.github.io/ComfyUI_examples/flux/)
   - [Lumina Image 2.0](https://comfyanonymous.github.io/ComfyUI_examples/lumina2/)
   - [HiDream](https://comfyanonymous.github.io/ComfyUI_examples/hidream/)
   - [Qwen Image](https://comfyanonymous.github.io/ComfyUI_examples/qwen_image/)
- 图像编辑模型
   - [Omnigen 2](https://comfyanonymous.github.io/ComfyUI_examples/omnigen/)
   - [Flux Kontext](https://comfyanonymous.github.io/ComfyUI_examples/flux/#flux-kontext-image-editing-model)
   - [HiDream E1.1](https://comfyanonymous.github.io/ComfyUI_examples/hidream/#hidream-e11)
   - [Qwen Image Edit](https://comfyanonymous.github.io/ComfyUI_examples/qwen_image/#edit-model)
- 视频模型
   - [Stable Video Diffusion](https://comfyanonymous.github.io/ComfyUI_examples/video/)
   - [Mochi](https://comfyanonymous.github.io/ComfyUI_examples/mochi/)
   - [LTX-Video](https://comfyanonymous.github.io/ComfyUI_examples/ltxv/)
   - [Hunyuan Video](https://comfyanonymous.github.io/ComfyUI_examples/hunyuan_video/)
   - [Wan 2.1](https://comfyanonymous.github.io/ComfyUI_examples/wan/)
   - [Wan 2.2](https://comfyanonymous.github.io/ComfyUI_examples/wan22/)
- 音频模型
   - [Stable Audio](https://comfyanonymous.github.io/ComfyUI_examples/audio/)
   - [ACE Step](https://comfyanonymous.github.io/ComfyUI_examples/audio/)
- 3D模型
   - [Hunyuan3D 2.0](https://docs.comfy.org/tutorials/3d/hunyuan3D-2)
- 异步队列系统
- 多项优化：仅重新执行执行间发生变化的工作流部分。
- 智能内存管理：可以通过智能卸载在低至1GB显存的GPU上自动运行大型模型。
- 即使没有GPU也能工作：使用 ```--cpu```（较慢）
- 可以加载ckpt和safetensors：一体化检查点或独立的扩散模型、VAE和CLIP模型。
- 安全加载ckpt、pt、pth等文件。
- 嵌入/文本反转
- [Loras（常规、locon和loha）](https://comfyanonymous.github.io/ComfyUI_examples/lora/)
- [超网络](https://comfyanonymous.github.io/ComfyUI_examples/hypernetworks/)
- 从生成的PNG、WebP和FLAC文件加载完整工作流（包含种子）。
- 将工作流保存/加载为Json文件。
- 节点界面可用于创建复杂工作流，如[高分辨率修复](https://comfyanonymous.github.io/ComfyUI_examples/2_pass_txt2img/)或更高级的工作流。
- [区域合成](https://comfyanonymous.github.io/ComfyUI_examples/area_composition/)
- 使用常规和修复模型进行[修复](https://comfyanonymous.github.io/ComfyUI_examples/inpaint/)。
- [ControlNet和T2I-Adapter](https://comfyanonymous.github.io/ComfyUI_examples/controlnet/)
- [放大模型（ESRGAN、ESRGAN变体、SwinIR、Swin2SR等）](https://comfyanonymous.github.io/ComfyUI_examples/upscale_models/)
- [GLIGEN](https://comfyanonymous.github.io/ComfyUI_examples/gligen/)
- [模型合并](https://comfyanonymous.github.io/ComfyUI_examples/model_merging/)
- [LCM模型和Loras](https://comfyanonymous.github.io/ComfyUI_examples/lcm/)
- 使用[TAESD](#how-to-show-high-quality-previews)进行潜在预览
- 完全离线工作：核心永远不会下载任何内容，除非您需要。
- 可选的API节点，通过在线[Comfy API](https://docs.comfy.org/tutorials/api-nodes/overview)使用外部提供商的付费模型。
- [配置文件](extra_model_paths.yaml.example)设置模型搜索路径。

工作流示例可在[示例页面](https://comfyanonymous.github.io/ComfyUI_examples/)找到

## 发布流程

ComfyUI遵循每周发布周期，目标是周五发布，但由于模型发布或代码库的重大更改，这个时间经常变化。有三个相互关联的仓库：

1. **[ComfyUI Core](https://github.com/comfyanonymous/ComfyUI)**
   - 发布新的稳定版本（例如v0.7.0）
   - 作为桌面版本的基础

2. **[ComfyUI Desktop](https://github.com/Comfy-Org/desktop)**
   - 使用最新稳定核心版本构建新版本

3. **[ComfyUI Frontend](https://github.com/Comfy-Org/ComfyUI_frontend)**
   - 每周前端更新合并到核心仓库
   - 为即将发布的核心版本冻结功能
   - 为下一个发布周期继续开发

## 快捷键

| 快捷键                            | 说明                                                                                                        |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `Ctrl` + `Enter`                      | 将当前图形加入生成队列                                                                              |
| `Ctrl` + `Shift` + `Enter`              | 将当前图形作为第一个加入生成队列                                                                     |
| `Ctrl` + `Alt` + `Enter`                | 取消当前生成                                                                                          |
| `Ctrl` + `Z`/`Ctrl` + `Y`                 | 撤销/重做                                                                                                          |
| `Ctrl` + `S`                          | 保存工作流                                                                                                      |
| `Ctrl` + `O`                          | 加载工作流                                                                                                      |
| `Ctrl` + `A`                          | 选择所有节点                                                                                                   |
| `Alt `+ `C`                           | 折叠/展开选中的节点                                                                                 |
| `Ctrl` + `M`                          | 静音/取消静音选中的节点                                                                                         |
| `Ctrl` + `B`                           | 绕过选中的节点（就像节点从图中移除并重新连接线路）            |
| `Delete`/`Backspace`                   | 删除选中的节点                                                                                              |
| `Ctrl` + `Backspace`                   | 删除当前图形                                                                                           |
| `Space`                              | 按住并移动光标时移动画布                                                             |
| `Ctrl`/`Shift` + `Click`                 | 将点击的节点添加到选择中                                                                                      |
| `Ctrl` + `C`/`Ctrl` + `V`                  | 复制和粘贴选中的节点（不保持与未选中节点输出的连接）                     |
| `Ctrl` + `C`/`Ctrl` + `Shift` + `V`          | 复制和粘贴选中的节点（保持从未选中节点输出到粘贴节点输入的连接） |
| `Shift` + `Drag`                       | 同时移动多个选中的节点                                                                      |
| `Ctrl` + `D`                           | 加载默认图形                                                                                                 |
| `Alt` + `+`                          | 画布放大                                                                                                     |
| `Alt` + `-`                          | 画布缩小                                                                                                    |
| `Ctrl` + `Shift` + LMB + Vertical drag | 画布放大/缩小                                                                                                 |
| `P`                                  | 固定/取消固定选中的节点                                                                                           |
| `Ctrl` + `G`                           | 组合选中的节点                                                                                               |
| `Q`                                 | 切换队列的可见性                                                                                     |
| `H`                                  | 切换历史记录的可见性                                                                                       |
| `R`                                  | 刷新图形                                                                                                      |
| `F`                                  | 显示/隐藏菜单                                                                                                      |
| `.`                                  | 适应选择的视图（未选择任何内容时为整个图形）                                                        |
| Double-Click LMB                   | 打开节点快速搜索面板                                                                                     |
| `Shift` + Drag                       | 同时移动多条线                                                                                        |
| `Ctrl` + `Alt` + LMB                   | 断开点击插槽的所有连线                                                                             |

对于macOS用户，`Ctrl`也可以替换为`Cmd`

# 安装

## Windows便携版

在[发布页面](https://github.com/comfyanonymous/ComfyUI/releases)有一个Windows便携独立构建版本，应该可以在Nvidia GPU上运行或仅在CPU上运行。

### [直接下载链接](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia.7z)

只需下载，用[7-Zip](https://7-zip.org)解压并运行。确保将您的稳定扩散检查点/模型（巨大的ckpt/safetensors文件）放在：ComfyUI\models\checkpoints

如果解压有问题，右键文件 -> 属性 -> 解除阻止

#### 如何在另一个UI和ComfyUI之间共享模型？

查看[配置文件](extra_model_paths.yaml.example)设置模型搜索路径。在Windows独立构建中，您可以在ComfyUI目录中找到此文件。将此文件重命名为extra_model_paths.yaml并用您喜欢的文本编辑器编辑它。


## [comfy-cli](https://docs.comfy.org/comfy-cli/getting-started)

您可以使用comfy-cli安装和启动ComfyUI：
```bash
pip install comfy-cli
comfy install
```

## 手动安装（Windows、Linux）

Python 3.13得到很好的支持。如果您在某些自定义节点依赖项方面遇到问题，可以尝试3.12

Git克隆此仓库。

将您的SD检查点（巨大的ckpt/safetensors文件）放在：models/checkpoints

将您的VAE放在：models/vae


### AMD GPU（仅Linux）
AMD用户可以使用pip安装rocm和pytorch（如果尚未安装），这是安装稳定版本的命令：

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm6.4```

这是安装ROCm 6.4夜间版本的命令，可能有一些性能改进：

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/rocm6.4```

### Intel GPU（Windows和Linux）

（选项1）Intel Arc GPU用户可以使用pip安装支持torch.xpu的原生PyTorch。更多信息可以在[这里](https://pytorch.org/docs/main/notes/get_start_xpu.html)找到

1. 要安装PyTorch xpu，使用以下命令：

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/xpu```

这是安装可能有一些性能改进的Pytorch xpu夜间版本的命令：

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/xpu```

（选项2）或者，Intel Extension for PyTorch (IPEX)支持的Intel GPU可以利用IPEX来提高性能。

1. 访问[安装](https://intel.github.io/intel-extension-for-pytorch/index.html#installation?platform=gpu)获取更多信息。

### NVIDIA

Nvidia用户应该使用此命令安装稳定的pytorch：

```pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu129```

这是安装可能有性能改进的pytorch夜间版本的命令。

```pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu129```

#### 故障排除

如果您遇到"Torch not compiled with CUDA enabled"错误，请卸载torch：

```pip uninstall torch```

然后使用上面的命令重新安装。

### 依赖项

通过在ComfyUI文件夹内打开终端并运行以下命令来安装依赖项：

```pip install -r requirements.txt```

之后您应该已经安装了所有内容，可以继续运行ComfyUI。

### 其他：

#### Apple Mac silicon

您可以在任何最新macOS版本的Apple Mac silicon（M1或M2）上安装ComfyUI。

1. 安装pytorch夜间版本。有关说明，请阅读[Mac上的加速PyTorch训练](https://developer.apple.com/metal/pytorch/) Apple开发者指南（确保安装最新的pytorch夜间版本）。
1. 按照Windows和Linux的[ComfyUI手动安装](#manual-install-windows-linux)说明进行操作。
1. 安装ComfyUI[依赖项](#dependencies)。如果您有另一个稳定扩散UI，[您可能能够重用依赖项](#i-already-have-another-ui-for-stable-diffusion-installed-do-i-really-have-to-install-all-of-these-dependencies)。
1. 通过运行`python main.py`启动ComfyUI

> **注意**：记住将您的模型、VAE、LoRA等添加到相应的Comfy文件夹中，如[ComfyUI手动安装](#manual-install-windows-linux)中所讨论的。

#### DirectML（Windows上的AMD卡）

这个支持很差，不推荐使用。存在一些非官方的windows pytorch ROCm构建，会给您比这更好的体验。一旦官方的windows pytorch ROCm构建发布，此readme将被更新。

```pip install torch-directml``` 然后您可以使用以下命令启动ComfyUI：```python main.py --directml```

#### 昇腾NPU

对于与Ascend Extension for PyTorch (torch_npu)兼容的模型。要开始使用，请确保您的环境满足[安装](https://ascend.github.io/docs/sources/ascend/quick_install.html)页面上概述的先决条件。以下是针对您的平台和安装方法的分步指南：

1. 如有必要，首先安装torch-npu安装页面中为Linux指定的推荐或更新的内核版本。
2. 按照为您的特定平台提供的说明，继续安装Ascend Basekit，其中包括驱动程序、固件和CANN。
3. 接下来，通过遵循[安装](https://ascend.github.io/docs/sources/pytorch/install.html#pytorch)页面上的平台特定说明来安装torch-npu的必要包。
4. 最后，遵循Linux的[ComfyUI手动安装](#manual-install-windows-linux)指南。安装所有组件后，您可以按前面描述的方式运行ComfyUI。

#### 寒武纪MLU

对于与Cambricon Extension for PyTorch (torch_mlu)兼容的模型。以下是针对您的平台和安装方法的分步指南：

1. 按照[安装](https://www.cambricon.com/docs/sdk_1.15.0/cntoolkit_3.7.2/cntoolkit_install_3.7.2/index.html)上的平台特定说明安装Cambricon CNToolkit
2. 接下来，按照[安装](https://www.cambricon.com/docs/sdk_1.15.0/cambricon_pytorch_1.17.0/user_guide_1.9/index.html)上的说明安装PyTorch(torch_mlu)
3. 通过运行`python main.py`启动ComfyUI

#### Iluvatar Corex

对于与Iluvatar Extension for PyTorch兼容的模型。以下是针对您的平台和安装方法的分步指南：

1. 按照[安装](https://support.iluvatar.com/#/DocumentCentre?id=1&nameCenter=2&productId=520117912052801536)上的平台特定说明安装Iluvatar Corex Toolkit
2. 通过运行`python main.py`启动ComfyUI

# 运行

```python main.py```

### 对于ROCm官方不支持的AMD卡

如果遇到问题，请尝试使用此命令运行：

对于6700、6600和可能的其他RDNA2或更旧版本：```HSA_OVERRIDE_GFX_VERSION=10.3.0 python main.py```

对于AMD 7600和可能的其他RDNA3卡：```HSA_OVERRIDE_GFX_VERSION=11.0.0 python main.py```

### AMD ROCm提示

您可以在一些AMD GPU上使用此命令在ComfyUI中启用最新pytorch上的实验性内存高效注意力，它应该在RDNA3上默认启用。如果这在您的GPU上的最新pytorch上提高了速度，请报告，以便我可以默认启用它。

```TORCH_ROCM_AOTRITON_ENABLE_EXPERIMENTAL=1 python main.py --use-pytorch-cross-attention```

您也可以尝试设置此环境变量`PYTORCH_TUNABLEOP_ENABLED=1`，这可能会加快速度，但代价是初始运行非常慢。

# 注意事项

只有具有所有正确输入的输出的图形部分才会被执行。

只有从一次执行到下一次执行发生变化的图形部分才会被执行，如果您提交相同的图形两次，只有第一次会被执行。如果您只更改图形的最后部分，只有您更改的部分和依赖于它的部分会被执行。

将生成的png拖到网页上或加载一个将为您提供完整的工作流，包括用于创建它的种子。

您可以使用()来改变单词或短语的强调，如：(good code:1.2)或(bad code:0.8)。()的默认强调为1.1。要在实际提示中使用()字符，请像\\(或\\)这样转义它们。

您可以使用{day|night}进行通配符/动态提示。使用此语法"{wild|card|test}"将在每次排队提示时被前端随机替换为"wild"、"card"或"test"中的一个。要在实际提示中使用{}字符，请像\\{或\\}这样转义它们。

动态提示还支持C风格注释，如`// comment`或`/* comment */`。

要在文本提示中使用文本反转概念/嵌入，请将它们放在models/embeddings目录中，并在CLIPTextEncode节点中像这样使用它们（您可以省略.pt扩展名）：

```embedding:embedding_filename.pt```


## 如何显示高质量预览？

使用```--preview-method auto```启用预览。

默认安装包括一个快速的低分辨率潜在预览方法。要使用[TAESD](https://github.com/madebyollin/taesd)启用更高质量的预览，请下载[taesd_decoder.pth、taesdxl_decoder.pth、taesd3_decoder.pth和taef1_decoder.pth](https://github.com/madebyollin/taesd/)并将它们放在`models/vae_approx`文件夹中。安装后，重启ComfyUI并使用`--preview-method taesd`启动以启用高质量预览。

## 如何使用TLS/SSL？
通过运行命令生成自签名证书（不适用于共享/生产使用）和密钥：`openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 3650 -nodes -subj "/C=XX/ST=StateName/L=CityName/O=CompanyName/OU=CompanySectionName/CN=CommonNameOrHostname"`

使用`--tls-keyfile key.pem --tls-certfile cert.pem`启用TLS/SSL，应用程序现在将可以通过`https://...`而不是`http://...`访问。

> 注意：Windows用户可以使用[alexisrolland/docker-openssl](https://github.com/alexisrolland/docker-openssl)或[第三方二进制分发](https://wiki.openssl.org/index.php/Binaries)之一来运行上面的示例命令。
<br/><br/>如果您使用容器，请注意卷挂载`-v`可以是相对路径，所以`... -v ".\:/openssl-certs" ...`将在您的命令提示符或powershell终端的当前目录中创建密钥和证书文件。

## 支持和开发频道

[Discord](https://comfy.org/discord)：尝试#help或#feedback频道。

[Matrix空间：#comfyui_space:matrix.org](https://app.element.io/#/room/%23comfyui_space%3Amatrix.org)（它像discord但是开源的）。

另请参阅：[https://www.comfy.org/](https://www.comfy.org/)

## 前端开发

自2024年8月15日起，我们已过渡到新的前端，现在托管在单独的仓库中：[ComfyUI Frontend](https://github.com/Comfy-Org/ComfyUI_frontend)。此仓库现在在`web/`目录下托管编译的JS（来自TS/Vue）。

### 报告问题和请求功能

对于任何与前端相关的错误、问题或功能请求，请使用[ComfyUI Frontend仓库](https://github.com/Comfy-Org/ComfyUI_frontend)。这将帮助我们更有效地管理和解决前端特定的问题。

### 使用最新前端

新前端现在是ComfyUI的默认选择。但是，请注意：

1. 主ComfyUI仓库中的前端每两周更新一次。
2. 每日发布在单独的前端仓库中可用。

要使用最新的前端版本：

1. 对于最新的每日发布，使用此命令行参数启动ComfyUI：

   ```
   --front-end-version Comfy-Org/ComfyUI_frontend@latest
   ```

2. 对于特定版本，将`latest`替换为所需的版本号：

   ```
   --front-end-version Comfy-Org/ComfyUI_frontend@1.2.2
   ```

这种方法允许您轻松在稳定的两周发布和前沿的每日更新之间切换，甚至为测试目的使用特定版本。

### 访问传统前端

如果您出于任何原因需要使用传统前端，可以使用以下命令行参数访问它：

```
--front-end-version Comfy-Org/ComfyUI_legacy_frontend@latest
```

这将使用保存在[ComfyUI Legacy Frontend仓库](https://github.com/Comfy-Org/ComfyUI_legacy_frontend)中的传统前端快照。

# 问答

### 我应该为此购买哪个GPU？

[查看此页面获取一些建议](https://github.com/comfyanonymous/ComfyUI/wiki/Which-GPU-should-I-buy-for-ComfyUI)
