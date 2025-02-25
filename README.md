# simple-onnx-processing-tools
A set of simple tools for splitting, merging, OP deletion, size compression, rewriting attributes and constants, OP generation, change opset, change to the specified input order, addition of OP, RGB to BGR conversion, change batch size, batch rename of OP, and JSON convertion for ONNX models.

[![Downloads](https://static.pepy.tech/personalized-badge/simple-onnx-processing-tools?period=total&units=none&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/simple-onnx-processing-tools) ![GitHub](https://img.shields.io/github/license/PINTO0309/simple-onnx-processing-tools?color=2BAF2B) [![PyPI](https://img.shields.io/pypi/v/simple-onnx-processing-tools?color=2BAF2B)](https://pypi.org/project/simple-onnx-processing-tools/)

<p align="center">
  <img src="https://user-images.githubusercontent.com/33194443/162783149-3b0d6e25-44da-4bc1-89fb-beae8aeae31d.png" />
</p>

## 1. Tools
### HostPC
```bash
# (1) Minimum configuration installation with no dependent packages installed
$ pip install -U simple-onnx-processing-tools \
&& pip install -U onnx \
&& python3 -m pip install -U onnx_graphsurgeon --index-url https://pypi.ngc.nvidia.com

or

# (2) When installing all dependent packages such as onnx-simplifier, onnxruntime, numpy, etc...
$ pip install -U simple-onnx-processing-tools[full] \
&& pip install -U onnx \
&& python3 -m pip install -U onnx_graphsurgeon --index-url https://pypi.ngc.nvidia.com
```
### Docker
```bash
$ docker run --rm -it \
-v `pwd`:/workdir \
-w /workdir \
pinto0309/simple-onnx-processing-tools:1.0.31
```

|No.|Tool Name|Tags|Summary|
|:-:|:-:|:-:|:-|
|1|**[snc4onnx](https://github.com/PINTO0309/snc4onnx)**<br>![snc](https://user-images.githubusercontent.com/33194443/170050379-72e2819a-8cc4-40c2-9cc9-d4ca50b83866.png)|[![PyPI](https://img.shields.io/pypi/v/snc4onnx?color=2BAF2B)](https://pypi.org/project/snc4onnx/)[![snc](https://img.shields.io/github/stars/PINTO0309/snc4onnx.svg?style=social)](https://github.com/PINTO0309/snc4onnx)|Simple tool to combine(merge) onnx models. **S**imple **N**etwork **C**ombine Tool for **ONNX**.|
|2|**[sne4onnx](https://github.com/PINTO0309/sne4onnx)**<br>![image](https://user-images.githubusercontent.com/33194443/170036340-dd098dd2-4955-48b6-a0dd-6b59c3598018.png)|[![PyPI](https://img.shields.io/pypi/v/sne4onnx?color=2BAF2B)](https://pypi.org/project/sne4onnx/)[![sne](https://img.shields.io/github/stars/PINTO0309/sne4onnx.svg?style=social)](https://github.com/PINTO0309/sne4onnx)|A very simple tool for situations where optimization with onnx-simplifier would exceed the Protocol Buffers upper file size limit of 2GB, or simply to separate onnx files to any size you want. **S**imple **N**etwork **E**xtraction for **ONNX**.|
|3|**[snd4onnx](https://github.com/PINTO0309/snd4onnx)**<br>![snd](https://user-images.githubusercontent.com/33194443/170049884-63abc243-0493-400a-9d95-612a800fbfce.png)|[![PyPI](https://img.shields.io/pypi/v/snd4onnx?color=2BAF2B)](https://pypi.org/project/snd4onnx/)[![snd](https://img.shields.io/github/stars/PINTO0309/snd4onnx.svg?style=social)](https://github.com/PINTO0309/snd4onnx)|Simple node deletion tool for onnx. **S**imple **N**ode **D**eletion for **ONNX**.|
|4|**[scs4onnx](https://github.com/PINTO0309/scs4onnx)**<br>![scs](https://user-images.githubusercontent.com/33194443/170051562-167c555d-251e-4672-b7c8-27106b08b310.png)|[![PyPI](https://img.shields.io/pypi/v/scs4onnx?color=2BAF2B)](https://pypi.org/project/scs4onnx/)[![scs](https://img.shields.io/github/stars/PINTO0309/scs4onnx.svg?style=social)](https://github.com/PINTO0309/scs4onnx)|A very simple tool that compresses the overall size of the ONNX model by aggregating duplicate constant values as much as possible. **S**imple **C**onstant value **S**hrink for **ONNX**.|
|5|**[sog4onnx](https://github.com/PINTO0309/sog4onnx)**<br>![sog](https://user-images.githubusercontent.com/33194443/170052975-a41eb326-aa96-45e5-9e82-6f15b7d3a2df.png)|[![PyPI](https://img.shields.io/pypi/v/sog4onnx?color=2BAF2B)](https://pypi.org/project/sog4onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/sog4onnx.svg?style=social)](https://github.com/PINTO0309/sog4onnx)|Simple ONNX operation generator. **S**imple **O**peration **G**enerator for **ONNX**.|
|6|**[sam4onnx](https://github.com/PINTO0309/sam4onnx)**<br>![sam](https://user-images.githubusercontent.com/33194443/170053658-a73ed77d-b7e4-475e-badf-e9ad933fccfe.png)|[![PyPI](https://img.shields.io/pypi/v/sam4onnx?color=2BAF2B)](https://pypi.org/project/sam4onnx/)[![sam](https://img.shields.io/github/stars/PINTO0309/sam4onnx.svg?style=social)](https://github.com/PINTO0309/sam4onnx)|A very simple tool to rewrite parameters such as attributes and constants for OPs in ONNX models. **S**imple **A**ttribute and Constant **M**odifier for **ONNX**.|
|7|**[soc4onnx](https://github.com/PINTO0309/soc4onnx)**<br>![soc](https://user-images.githubusercontent.com/33194443/170055270-71c108a8-53e5-4ab0-9ca7-2ca2b1627ad4.png)|[![PyPI](https://img.shields.io/pypi/v/soc4onnx?color=2BAF2B)](https://pypi.org/project/soc4onnx/)[![sam](https://img.shields.io/github/stars/PINTO0309/soc4onnx.svg?style=social)](https://github.com/PINTO0309/soc4onnx)|A very simple tool that forces a change in the opset of an ONNX graph. **S**imple **O**pset **C**hanger for **ONNX**.|
|8|**[scc4onnx](https://github.com/PINTO0309/scc4onnx)**<br>![scc](https://user-images.githubusercontent.com/33194443/170063890-a79c057e-ce61-4b21-be25-82f58d06f460.png)|[![PyPI](https://img.shields.io/pypi/v/scc4onnx?color=2BAF2B)](https://pypi.org/project/scc4onnx/)[![sam](https://img.shields.io/github/stars/PINTO0309/scc4onnx.svg?style=social)](https://github.com/PINTO0309/scc4onnx)|Very simple NCHW and NHWC conversion tool for ONNX. Change to the specified input order for each and every input OP. Also, change the channel order of RGB and BGR. **S**imple **C**hannel **C**onverter for **ONNX**.|
|9|**[sna4onnx](https://github.com/PINTO0309/sna4onnx)**<br>![sna](https://user-images.githubusercontent.com/33194443/170064699-39b1645e-d1b0-4751-8399-e47eca2b28ae.png)|[![PyPI](https://img.shields.io/pypi/v/sna4onnx?color=2BAF2B)](https://pypi.org/project/sna4onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/sna4onnx.svg?style=social)](https://github.com/PINTO0309/sna4onnx)|Simple node addition tool for onnx. **S**imple **N**ode **A**ddition for **ONNX**.|
|10|**[sbi4onnx](https://github.com/PINTO0309/sbi4onnx)**<br>![sbi](https://user-images.githubusercontent.com/33194443/170146414-5a4b0b8a-ac5e-49e7-9e17-703c04f1b746.png)|[![PyPI](https://img.shields.io/pypi/v/sbi4onnx?color=2BAF2B)](https://pypi.org/project/sbi4onnx/)[![sbi4onnx](https://img.shields.io/github/stars/PINTO0309/sbi4onnx.svg?style=social)](https://github.com/PINTO0309/sbi4onnx)|A very simple script that only initializes the batch size of ONNX. **S**imple **B**atchsize **I**nitialization for **ONNX**.|
|11|**[sor4onnx](https://github.com/PINTO0309/sor4onnx)**<br>![sor](https://user-images.githubusercontent.com/33194443/170146570-681a4e72-35e2-4625-96ae-dc84ef2ff4c9.png)|[![PyPI](https://img.shields.io/pypi/v/sor4onnx?color=2BAF2B)](https://pypi.org/project/sor4onnx/)[![sor4onnx](https://img.shields.io/github/stars/PINTO0309/sor4onnx.svg?style=social)](https://github.com/PINTO0309/sor4onnx)|**S**imple **O**P **R**enamer for **ONNX**.|
|12|**[soa4onnx](https://github.com/PINTO0309/soa4onnx)**<br>![soa](https://user-images.githubusercontent.com/33194443/170147250-d49ae8d1-0ad2-4c7c-8578-70d75c3463a7.png)|[![PyPI](https://img.shields.io/pypi/v/soa4onnx?color=2BAF2B)](https://pypi.org/project/soa4onnx/)[![soa4onnx](https://img.shields.io/github/stars/PINTO0309/soa4onnx.svg?style=social)](https://github.com/PINTO0309/soa4onnx)|**S**imple model **O**utput OP **A**dditional tools for ONNX.|
|13|**[ssi4onnx](https://github.com/PINTO0309/ssi4onnx)**<br>![ssi](https://user-images.githubusercontent.com/33194443/170065874-74cc3c91-e0d6-46fb-9084-925d3d503e05.png)|[![PyPI](https://img.shields.io/pypi/v/ssi4onnx?color=2BAF2B)](https://pypi.org/project/ssi4onnx/)[![ssi4onnx](https://img.shields.io/github/stars/PINTO0309/ssi4onnx.svg?style=social)](https://github.com/PINTO0309/ssi4onnx)|**S**imple **S**hape **I**nference tool for **ONNX**.|
|14|**[sit4onnx](https://github.com/PINTO0309/sit4onnx)**<br>![sit](https://user-images.githubusercontent.com/33194443/170147823-3f4c34c5-b8f1-4b13-9c4a-6f186b59a024.png)|[![PyPI](https://img.shields.io/pypi/v/sit4onnx?color=2BAF2B)](https://pypi.org/project/sit4onnx/)[![sit4onnx](https://img.shields.io/github/stars/PINTO0309/sit4onnx.svg?style=social)](https://github.com/PINTO0309/sit4onnx)|Tools for simple inference testing using TensorRT, CUDA and OpenVINO CPU/GPU and CPU providers. **S**imple **I**nference **T**est for **ONNX**.|
|15|**[onnx2json](https://github.com/PINTO0309/onnx2json)**<br>![onnx2json](https://user-images.githubusercontent.com/33194443/170148134-56194fe0-c871-4592-affe-76b2f45bc5c1.png)|[![PyPI](https://img.shields.io/pypi/v/onnx2json?color=2BAF2B)](https://pypi.org/project/onnx2json/)[![onnx2json](https://img.shields.io/github/stars/PINTO0309/onnx2json.svg?style=social)](https://github.com/PINTO0309/onnx2json)|Exports the ONNX file to a JSON file.|
|16|**[json2onnx](https://github.com/PINTO0309/json2onnx)**<br>![json2onnx](https://user-images.githubusercontent.com/33194443/170148289-aae9591d-c7b7-4ea9-acfd-a790a7b50243.png)|[![PyPI](https://img.shields.io/pypi/v/json2onnx?color=2BAF2B)](https://pypi.org/project/json2onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/json2onnx.svg?style=social)](https://github.com/PINTO0309/json2onnx)|Converts a JSON file to an ONNX file.|
|17|**[sed4onnx](https://github.com/PINTO0309/sed4onnx)**<br>![sed](https://user-images.githubusercontent.com/33194443/170149753-3a586319-bded-4385-996a-272a4bb1dac1.png)|[![PyPI](https://img.shields.io/pypi/v/sed4onnx?color=2BAF2B)](https://pypi.org/project/sed4onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/sed4onnx.svg?style=social)](https://github.com/PINTO0309/sed4onnx)|Simple ONNX constant encoder/decoder. Since the constant values in the JSON files generated by onnx2json are Base64-encoded values, ASCII <-> Base64 conversion is required when rewriting JSON constant values.|
|18|**[ssc4onnx](https://github.com/PINTO0309/ssc4onnx)**<br>![ssc](https://user-images.githubusercontent.com/33194443/170720385-d8fcde6b-f8c0-4a8e-94eb-230996e0f5d2.png)|[![PyPI](https://img.shields.io/pypi/v/ssc4onnx?color=2BAF2B)](https://pypi.org/project/ssc4onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/ssc4onnx.svg?style=social)](https://github.com/PINTO0309/ssc4onnx)|Checker with simple ONNX model structure. **S**imple **S**tructure **C**hecker for **ONNX**. Analyzes and displays the structure of huge size models that cannot be displayed by Netron.|
|19|**[components_of_onnx](https://github.com/PINTO0309/components_of_onnx)**<br>![components_of_onnx](https://user-images.githubusercontent.com/33194443/170149987-6184980f-e4cf-4b1b-b49f-92874c7941a5.png)|[WIP][![PyPI](https://img.shields.io/pypi/v/components_of_onnx?color=2BAF2B)](https://pypi.org/project/components_of_onnx/)[![sog](https://img.shields.io/github/stars/PINTO0309/components_of_onnx.svg?style=social)](https://github.com/PINTO0309/components_of_onnx)|ONNX parts yard. The various operations described in [Operator Schemas](https://github.com/onnx/onnx/blob/main/docs/Operators.md) are converted in advance into OP stand-alone ONNX files.|

## 2. Very useful tools

|No.|Tool Name|Author|Tags|Summary|
|:-:|:-:|:-|:-:|:-|
|1|**[OnnxGraphQt](https://github.com/fateshelled/OnnxGraphQt)**<br>![onnx_graph_qt](https://user-images.githubusercontent.com/33194443/170164510-b53b14d0-3492-4952-9ed9-1bbfb52c12e8.png)|**[fateshelled](https://github.com/fateshelled)**|[WIP]|ONNX model visualizer. Model structure can be edited on the visualization tool.![image](https://user-images.githubusercontent.com/33194443/166604378-ba33f9b3-8dc1-46b3-bece-15c2d08b678a.png)![image](https://user-images.githubusercontent.com/33194443/166604396-1fe3a015-9b3c-4a49-8bc4-7438aedbbab6.png)|
|2|**[onnx-simplifier](https://github.com/daquexian/onnx-simplifier)**|**[daquexian](https://github.com/daquexian)**|[![PyPI](https://img.shields.io/pypi/v/onnx-simplifier?color=2BAF2B)](https://pypi.org/project/onnx-simplifier/)[![onnxsim](https://img.shields.io/github/stars/daquexian/onnx-simplifier.svg?style=social)](https://github.com/daquexian/onnx-simplifier)|ONNX Simplifier is presented to simplify the ONNX model. It infers the whole computation graph and then replaces the redundant operators with their constant outputs.|

### 2-1. OnnxGraphQt - [WIP] Startup Method Sample
```bash
$ xhost +local: && \
docker run -it --rm \
-v `pwd`:/home/user/workdir \
-v /tmp/.X11-unix/:/tmp/.X11-unix:rw \
--net=host \
-e XDG_RUNTIME_DIR=$XDG_RUNTIME_DIR \
-e DISPLAY=$DISPLAY \
--privileged \
ghcr.io/pinto0309/openvino2tensorflow:latest

$ git clone https://github.com/fateshelled/OnnxGraphQt \
&& cd OnnxGraphQt \
&& sudo python3 -m pip install -r requirements.txt -U \
&& cd ..

$ python3 OnnxGraphQt/onnxgraphqt/main.py
```
### 2-2. win10 安装建议
1. pip install -U pydot PyQt5  --user
2. 设置系统环境变量


   ![image](https://user-images.githubusercontent.com/28527493/172283064-5db8bbdf-9c1a-4216-bce2-b9d65dc1dce6.png)
3. NodeGraphQt 包安装 和 OnnxGraphQt（GitHub超时）
  ```bash
  $ git clone https://github.com/jchanvfx/NodeGraphQt.git
  $ cd NodeGraphQt
  $ python setup.py install 
  $ git clone https://github.com/fateshelled/OnnxGraphQt \
  $ cd OnnxGraphQt \
  $ ## 先屏蔽 requirements.txt 中 git+https://github.com/jchanvfx/NodeGraphQt.git@v0.2.2#egg=NodeGraphQt
  $ sudo python3 -m pip install -r requirements.txt -U \
  $ cd ..
  $ python3 OnnxGraphQt/onnxgraphqt/main.py
   ```
## 3. Acknowledgments
1. https://github.com/onnx/onnx/blob/main/docs/PythonAPIOverview.md
 https://docs.nvidia.com/deeplearning/tensorrt/onnx-graphsurgeon/docs/index.html
3. https://github.com/NVIDIA/TensorRT/tree/main/tools/onnx-graphsurgeon
4. https://github.com/onnx/onnx/blob/main/docs/Operators.md

## 4. References
1. https://github.com/PINTO0309/PINTO_model_zoo
