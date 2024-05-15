<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><p dir="auto"><a href="https://github.com/OpenNMT/CTranslate2/actions?query=workflow%3ACI"><img src="https://github.com/OpenNMT/CTranslate2/workflows/CI/badge.svg" alt="CI" style="max-width: 100%;"></a> <a href="https://badge.fury.io/py/ctranslate2" rel="nofollow"><img src="https://camo.githubusercontent.com/3e8576586d303dcc6bce45751fb38102e37f94f3566f899b005e9deef52eb625/68747470733a2f2f62616467652e667572792e696f2f70792f637472616e736c617465322e737667" alt="PyPI版本" data-canonical-src="https://badge.fury.io/py/ctranslate2.svg" style="max-width: 100%;"></a> <a href="https://opennmt.net/CTranslate2/" rel="nofollow"><img src="https://camo.githubusercontent.com/bffc6e1208bae5741460f92c0c744b1831e930cf143e6f65f55b3a5e44d27688/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646f63732d6c61746573742d626c75652e737667" alt="文档" data-canonical-src="https://img.shields.io/badge/docs-latest-blue.svg" style="max-width: 100%;"></a> <a href="https://gitter.im/OpenNMT/CTranslate2?utm_source=badge&amp;utm_medium=badge&amp;utm_campaign=pr-badge" rel="nofollow"><img src="https://camo.githubusercontent.com/7219e74080dae46ef39b4204fc22a5f28827308627de3c91fcf6b3eea6487893/68747470733a2f2f6261646765732e6769747465722e696d2f4f70656e4e4d542f435472616e736c617465322e737667" alt="吉特" data-canonical-src="https://badges.gitter.im/OpenNMT/CTranslate2.svg" style="max-width: 100%;"></a> <a href="https://forum.opennmt.net/" rel="nofollow"><img src="https://camo.githubusercontent.com/da04d20382245c08386a1da6fd2d52c0e136cab8711a1ff3a28af66d0333e46c/68747470733a2f2f696d672e736869656c64732e696f2f646973636f757273652f7374617475733f7365727665723d6874747073253341253246253246666f72756d2e6f70656e6e6d742e6e6574253246" alt="论坛" data-canonical-src="https://img.shields.io/discourse/status?server=https%3A%2F%2Fforum.opennmt.net%2F" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">C翻译2</font></font></h1><a id="user-content-ctranslate2" class="anchor" aria-label="永久链接：CTranslate2" href="#ctranslate2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CTranslate2 是一个 C++ 和 Python 库，用于使用 Transformer 模型进行高效推理。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该项目实现了一个自定义运行时，应用了许多性能优化技术，如权重量化、层融合、批量重新排序等，以加速和减少</font><font style="vertical-align: inherit;">Transformer 模型在 CPU 和 GPU 上的</font></font><a href="#benchmarks"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存使用。</font></font></a><font style="vertical-align: inherit;"></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目前支持以下模型类型：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">编码器-解码器型号：Transformer base/big、M2M-100、NLLB、BART、mBART、Pegasus、T5、Whisper</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">仅解码器型号：GPT-2、GPT-J、GPT-NeoX、OPT、BLOOM、MPT、Llama、Mistral、Gemma、CodeGen、GPTBigCode、Falcon</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">仅编码器模型：BERT、DistilBERT、XLM-RoBERTa</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">兼容的模型应首先转换为优化的模型格式。该库包含多个框架的转换器：</font></font></p>
<ul dir="auto">
<li><a href="https://opennmt.net/CTranslate2/guides/opennmt_py.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py</font></font></a></li>
<li><a href="https://opennmt.net/CTranslate2/guides/opennmt_tf.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf</font></font></a></li>
<li><a href="https://opennmt.net/CTranslate2/guides/fairseq.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">费尔序列</font></font></a></li>
<li><a href="https://opennmt.net/CTranslate2/guides/marian.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">玛丽安</font></font></a></li>
<li><a href="https://opennmt.net/CTranslate2/guides/opus_mt.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OPUS-MT</font></font></a></li>
<li><a href="https://opennmt.net/CTranslate2/guides/transformers.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">变形金刚</font></font></a></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该项目面向生产，具有</font></font><a href="https://opennmt.net/CTranslate2/versioning.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">向后兼容性保证</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，但它还包括与模型压缩和推理加速相关的实验功能。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">主要特征</font></font></h2><a id="user-content-key-features" class="anchor" aria-label="永久链接：主要功能" href="#key-features"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 CPU 和 GPU 上快速高效地执行</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">得益于许多高级优化：层融合、填充去除、批量重新排序、就地操作、缓存，在受支持的模型和任务上，执行</font></font><a href="#benchmarks"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">速度明显快于通用深度学习框架，并且需要</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的资源更少机制等</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化和降低精度</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模型序列化和计算支持</font></font><a href="https://opennmt.net/CTranslate2/quantization.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">降低精度</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的权重：16 位浮点（FP16）、16 位脑浮点（BF16）、16 位整数（INT16）和 8 位整数（INT8） 。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多种CPU架构支持</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该项目支持x86-64和AArch64/ARM64处理器，并集成了针对这些平台优化的多个后端：</font></font><a href="https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/onemkl.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Intel MKL</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><a href="https://github.com/oneapi-src/oneDNN"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">oneDNN</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><a href="https://www.openblas.net/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenBLAS</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><a href="https://github.com/google/ruy"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Ruy</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://developer.apple.com/documentation/accelerate" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Apple Accelerate</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自动CPU 检测和代码调度</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">一个二进制文件可以包含多个后端（例如Intel MKL 和oneDNN）和指令集架构（例如AVX、AVX2），这些架构是在运行时根据CPU 信息自动选择的。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并行和异步执行</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可以使用多个 GPU 或 CPU 核心并行和异步处理多个批次。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动态内存使用</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存使用量根据请求大小动态变化，同时由于 CPU 和 GPU 上的缓存分配器仍然满足性能要求。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">磁盘上的轻量级</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">量化可以使磁盘上的模型缩小 4 倍，同时将精度损失降至最低。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">简单集成</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该项目几乎没有依赖项，并公开了</font></font><a href="https://opennmt.net/CTranslate2/python/overview.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和 C++ 中的简单 API 来满足大多数集成需求。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可配置的交互式解码</font></font></strong><br><a href="https://opennmt.net/CTranslate2/decoding.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">高级解码功能</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">允许自动完成部分序列并返回序列中特定位置的替代项。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持张量并行进行分布式推理</font></font></strong><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">非常大的模型可以拆分为多个GPU。按照此</font></font><a href="/OpenNMT/CTranslate2/blob/master/docs/parallel.md#model-and-tensor-parallelism"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文档</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置所需的环境。</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">其中一些功能很难使用标准深度学习框架来实现，这也是该项目的动机。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装与使用</font></font></h2><a id="user-content-installation-and-usage" class="anchor" aria-label="永久链接：安装和使用" href="#installation-and-usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CTranslate2 可以使用 pip 安装：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install ctranslate2</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install ctranslate2" tabindex="0" role="button">
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python模块用于转换模型，只需几行代码即可翻译或生成文本：</font></font></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-s1">translator</span> <span class="pl-c1">=</span> <span class="pl-s1">ctranslate2</span>.<span class="pl-v">Translator</span>(<span class="pl-s1">translation_model_path</span>)
<span class="pl-s1">translator</span>.<span class="pl-en">translate_batch</span>(<span class="pl-s1">tokens</span>)

<span class="pl-s1">generator</span> <span class="pl-c1">=</span> <span class="pl-s1">ctranslate2</span>.<span class="pl-v">Generator</span>(<span class="pl-s1">generation_model_path</span>)
<span class="pl-s1">generator</span>.<span class="pl-en">generate_batch</span>(<span class="pl-s1">start_tokens</span>)</pre><div class="zeroclipboard-container">
   
    
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请参阅</font></font><a href="https://opennmt.net/CTranslate2" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文档</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以获取更多信息和示例。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基准测试</font></font></h2><a id="user-content-benchmarks" class="anchor" aria-label="永久链接：基准" href="#benchmarks"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们用多个模型</font><font style="vertical-align: inherit;">翻译 En-&gt;De 测试集</font></font><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">newstest2014 ：</font></font></em><font style="vertical-align: inherit;"></font></p>
<ul dir="auto">
<li><a href="https://opennmt.net/Models-tf/#translation" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf WMT14</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：在 WMT14 数据集（450 万行）上使用 OpenNMT-tf 训练的基础 Transformer</font></font></li>
<li><a href="https://opennmt.net/Models-py/#translation" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py WMT14</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：在 WMT14 数据集（450 万行）上使用 OpenNMT-py 训练的基础 Transformer</font></font></li>
<li><a href="https://github.com/Helsinki-NLP/OPUS-MT-train/tree/master/models/en-de#opus-2020-02-26zip"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OPUS-MT</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：一个基础 Transformer，由 Marian 根据 2020 年 2 月 26 日提供的所有 OPUS 数据进行训练（8190 万行）</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基准测试报告每秒生成的目标令牌数量（越高越好）。结果通过多次运行进行汇总。有关更多详细信息</font><font style="vertical-align: inherit;">，请参阅</font></font><a href="/OpenNMT/CTranslate2/blob/master/tools/benchmark"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基准测试脚本</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并重现这些数字。</font></font></p>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请注意，下面提供的结果仅对该基准测试期间使用的配置有效：绝对和相对性能可能会随着不同的设置而变化。</font></font></strong></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中央处理器</font></font></h4><a id="user-content-cpu" class="anchor" aria-label="永久链接：CPU" href="#cpu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<table>
<thead>
<tr>
<th></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">每秒令牌数</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最大限度。记忆</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">蓝线</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf WMT14 模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf 2.31.0（使用 TensorFlow 2.11.0）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">209.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2653MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.93</font></font></td>
</tr>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py WMT14 模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py 3.0.4（使用 PyTorch 1.13.1）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">275.8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2012MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">323.3</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1359MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.72</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">翻译2 3.6.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">658.8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">849MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">733.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">672MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.82</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">860.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">529MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.78</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8 + vmap</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1126.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">598MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.64</font></font></td>
</tr>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OPUS-MT模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">变形金刚 4.26.1（使用 PyTorch 1.13.1）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">147.3</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2332MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.90</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">玛丽安1.11.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">344.5</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">7605MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.93</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">330.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">5901MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.65</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">355.8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4763MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.27</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">翻译2 3.6.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">525.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">721MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.92</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">596.1</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">660MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.53</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">696.1</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">516MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.65</font></font></td>
</tr>
</tbody>
</table>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在配备 Intel(R) Xeon(R) Platinum 8275CL CPU 的</font></font><a href="https://aws.amazon.com/ec2/instance-types/c5/" rel="nofollow"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">c5.2xlarge</font></font></em></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> Amazon EC2 实例上使用 4 个线程执行。</font></font></p>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">图形处理器</font></font></h4><a id="user-content-gpu" class="anchor" aria-label="永久链接：GPU" href="#gpu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<table>
<thead>
<tr>
<th></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">每秒令牌数</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最大限度。 GPU显存</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最大限度。中央处理器内存</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">蓝线</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf WMT14 模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-tf 2.31.0（使用 TensorFlow 2.11.0）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1483.5</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3031MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3122MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.94</font></font></td>
</tr>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py WMT14 模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenNMT-py 3.0.4（使用 PyTorch 1.13.1）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1795.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2973MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3099MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">更快的变压器 5.3</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">6979.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2402MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1131MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- 浮动16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8592.5</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1360MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1135MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.80</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">翻译2 3.6.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">6634.7</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1261MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">953MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8567.2</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1005MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">807MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.85</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- 浮动16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">10990.7</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">941MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">807MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.77</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8 + float16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8725.4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">813MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">800MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">26.83</font></font></td>
</tr>
<tr>
<td><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OPUS-MT模型</font></font></strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">变形金刚 4.26.1（使用 PyTorch 1.13.1）</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1022.9</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4097MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2109MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.90</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">玛丽安1.11.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3241.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3381MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2156MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.92</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- 浮动16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3962.4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3239MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1976MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.94</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">翻译2 3.6.0</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">5876.4</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1197MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">754MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.92</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">7521.9</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1005MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">792MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.79</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- 浮动16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">9296.7</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">909MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">814MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.90</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">- int8 + float16</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">8362.7</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">813MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">766MB</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">27.90</font></font></td>
</tr>
</tbody>
</table>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在配备 NVIDIA A10G GPU 的</font></font><a href="https://aws.amazon.com/ec2/instance-types/g5/" rel="nofollow"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">g5.xlarge</font></font></em></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;"> Amazon EC2 实例上使用 CUDA 11 执行（驱动程序版本：510.47.03）。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">其他资源</font></font></h2><a id="user-content-additional-resources" class="anchor" aria-label="固定链接：其他资源" href="#additional-resources"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://opennmt.net/CTranslate2" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文档</font></font></a></li>
<li><a href="https://forum.opennmt.net" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">论坛</font></font></a></li>
<li><a href="https://gitter.im/OpenNMT/CTranslate2" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">吉特</font></font></a></li>
</ul>
</article></div>
