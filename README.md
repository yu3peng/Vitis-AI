<div align="center">
  <img width="100%" height="100%" src="docs/images/Vitis-AI.png">
</div>

https://china.xilinx.com/support/documentation/sw_manuals/vitis_ai/1_3/c_ug1414-vitis-ai.pdf

<br />
Xilinx&reg; Vitis&trade; AI is a development stack for AI inference on Xilinx hardware platforms, including both edge devices and Alveo cards.

It consists of optimized IP, tools, libraries, models, and example designs. It is designed with high efficiency and ease of use in mind, unleashing the full potential of AI acceleration on Xilinx FPGA and ACAP.  
<br />
<br />

<div align="center">
  <img width="45%" height="45%" src="docs/images/Vitis-AI-arch.png">
</div>

<br />
Vitis AI is composed of the following key components:

* **AI Model Zoo**  - A comprehensive set of pre-optimized models that are ready to deploy on Xilinx devices.
* **AI Optimizer** - An optional model optimizer that can prune a model by up to 90%. It is separately available with commercial licenses.
* **AI Quantizer** - A powerful quantizer that supports model quantization, calibration, and fine tuning.
* **AI Compiler** - Compiles the quantized model to a high-efficient instruction set and data flow.
* **AI Profiler** - Perform an in-depth analysis of the efficiency and utilization of AI inference implementation.
* **AI Library** - Offers high-level yet optimized C++ APIs for AI applications from edge to cloud.
* **DPU** - Efficient and scalable IP cores can be customized to meet the needs for many different applications.
  * For more details on the different DPUs available, refer to [DPU Naming](docs/learn/dpu_naming.md).


**Learn More:** [Vitis AI Overview](https://www.xilinx.com/products/design-tools/vitis/vitis-ai.html)  


## [See What's New](docs//learn/release_notes.md)
- [Release Notes](docs//learn/release_notes.md)
- Added support for Pytorch and Tensorflow 2.3 frameworks
- Added more ready-to-use AI models for a wider range of applications, including 3D point cloud detection and segmentation, COVID-19 chest image segmentation and other reference models
- Unified XIR-based compilation flow from edge to cloud
- Vitis AI Runtime (VART) fully open source
- New RNN overlay for NLP applications
- New CNN DPUs for the low-latency and higher throughput applications on Alveo cards
- EoU enhancement with Beta version model partitioning and custom layer/operators plug-in

## Getting Started

Two options are available for installing the containers with the Vitis AI tools and resources.

 - Pre-built containers on Docker Hub: [xilinx/vitis-ai](https://hub.docker.com/r/xilinx/vitis-ai/tags)
 - Build containers locally with Docker recipes: [Docker Recipes](setup/docker)


### Installation

 - [Ubuntu playground](https://www.katacoda.com/courses/ubuntu/playground) - Use free resource

 - [Install Docker](docs/install_docker/README.md) - if Docker not installed on your machine yet

 - [Ensure your linux user is in the group docker](https://docs.docker.com/install/linux/linux-postinstall/)

 - Clone the Vitis-AI repository to obtain the examples, reference code, and scripts.
    ```bash
    git clone --recurse-submodules https://github.com/yu3peng/Vitis-AI  

    cd Vitis-AI
    ```

#### Using Pre-built Docker

Download the latest Vitis AI Docker with the following command. This container runs on CPU.  
```
docker pull xilinx/vitis-ai-cpu:latest  
```

To run the docker, use command:
```
./docker_run.sh xilinx/vitis-ai-cpu:latest
```

```
NOTICE:  BY INVOKING THIS SCRIPT AND USING THE SOFTWARE INSTALLED BY THE
SCRIPT, YOU AGREE ON BEHALF OF YOURSELF AND YOUR EMPLOYER (IF APPLICABLE)
TO BE BOUND TO THE LICENSE AGREEMENTS APPLICABLE TO THE SOFTWARE THAT YOU
INSTALL BY RUNNING THE SCRIPT.

Press any key to continue...
BY ELECTING TO CONTINUE, YOU WILL CAUSE THIS SCRIPT FILE TO AUTOMATICALLY
INSTALL A VARIETY OF SOFTWARE COPYRIGHTED
BY XILINX AND THIRD PARTIES THAT IS SUBJECT TO VARIOUS LICENSE AGREEMENTS 
THAT APPEAR UPON INSTALLATION, ACCEPTANCE AND/OR ACTIVATION OF THE
SOFTWARE AND/OR ARE CONTAINED OR DESCRIBED IN THE CORRESPONDING RELEASE
NOTES OR OTHER DOCUMENTATION OR HEADER OR SOURCE FILES. XILINX DOES NOT
GRANT TO LICENSEE ANY RIGHTS OR LICENSES TO SUCH THIRD-PARTY SOFTWARE.
LICENSEE AGREES TO CAREFULLY REVIEW AND ABIDE BY THE TERMS AND CONDITIONS
OF SUCH LICENSE AGREEMENTS TO THE EXTENT THAT THEY GOVERN SUCH SOFTWARE.

Press any key to continue...
BY ELECTING TO CONTINUE, YOU WILL CAUSE THE FOLLOWING SOFTWARE TO BE DOWNLOADED
AND INSTALLED ON YOUR SYSTEM. BY ELECTING TO CONTINUE, YOU UNDERSTAND THAT THE
INSTALLATION OF THE SOFTWARE LISTED BELOW MAY ALSO RESULT IN THE INSTALLATION
ON YOUR SYSTEM OF ADDITIONAL SOFTWARE NOT LISTED BELOW IN ORDER TO OPERATE
(SUCH SOFTWARE IS HEREAFTER REFERRED TO AS ‘DEPENDENCIES’)
XILINX DOES NOT GRANT TO LICENSEE ANY RIGHTS OR LICENSES TO SUCH DEPENDENCIES
LICENSEE AGREES TO CAREFULLY REVIEW AND ABIDE BY THE TERMS AND CONDITIONS
OF ANY LICENSE AGREEMENTS TO THE EXTENT THAT THEY GOVERN SUCH DEPENDENCIES

BY ELECTING TO CONTINUE, YOU WILL CAUSE THE FOLLOWING SOFTWARE PACKAGES
(AND THEIR RESPECTIVE DEPENDENCIES, IF APPLICABLE) TO BE DOWNLOADED FROM
UBUNTU'S MAIN REPO AND INSTALLED ON YOUR SYSTEM:
http://us.archive.ubuntu.com/ubuntu/dists/bionic/
Press any key to continue...http://us.archive.ubuntu.com/ubuntu/dists/bionic/
1.  sudo  
2.  git  
3.  zstd  
4.  tree  
5.  vim  
6.  wget  
7.  bzip2  
8.  ca-certificates  
9.  curl  
10. unzip  
11. python3-minimal  
12. python3-opencv  
13. python3-venv  
14. python3-pip  
15. python3-setuptools  
16. g++  
17. make  
18. cmake  
19. build-essential  
20. autoconf  
21. libgoogle-glog-dev  
22. libgflags-dev  
23. libunwind-dev  
24. libtool  
25. libgtk2.0-dev
26. libavcodec-dev
27. libavformat-dev
28. libavdevice-dev

BY ELECTING TO CONTINUE, YOU WILL CAUSE THE FOLLOWING SOFTWARE PACKAGES
(AND THEIR RESPECTIVE DEPENDENCIES, IF APPLICABLE) TO BE DOWNLOADED FROM
ANACONDA REPO AND INSTALLED ON YOUR SYSTEM:
https://anaconda.org”
Press any key to continue...1.  absl-py
2.  astor
3.  attrs
4.  backcall
5.  backports
6.  backports.weakref
7.  blas
8.  bleach
9.  boost
10.  bzip2
11.  ca-certificates
12.  cairo
13.  c-ares
14.  certifi
15.  cffi
16.  chardet
17.  cloudpickle
18.  conda
19.  conda-package-handling
20.  cryptography
21.  cycler
22.  cytoolz
23.  dask-core
24.  dbus
25.  decorator
26.  defusedxml
27.  dill
28.  dpuv1_compiler
29.  dpuv1-rt
30.  dpuv1-rt-ext
31.  dpuv1-rt-neptune
32.  entrypoints
33.  expat
34.  ffmpeg
35.  fontconfig
36.  freeglut
37.  freetype
38.  fribidi
39.  gast
40.  gettext
41.  gflags
42.  giflib
43.  glib
44.  glog
45.  gmp
46.  gnutls
47.  google-pasta
48.  graphite2
49.  graphviz
50.  grpcio
51.  gst-plugins-base
52.  gstreamer
53.  h5py
54.  harfbuzz
55.  hdf5
56.  icu
57.  idna
58.  imageio
59.  importlib_metadata
60.  importlib-metadata
61.  intel-openmp
62.  ipykernel
63.  ipython
64.  ipython_genutils
65.  ipywidgets
66.  jasper
67.  jedi
68.  jinja2
69.  joblib
70.  jpeg
71.  json-c
72.  jsoncpp
73.  jsonschema
74.  jupyter
75.  jupyter_client
76.  jupyter_console
77.  jupyter_core
78.  keras
79.  keras-applications
80.  keras-base
81.  keras-preprocessing
82.  kiwisolver
83.  krb5
84.  lame
85.  ld_impl_linux-64
86.  leveldb
87.  libblas
88.  libboost
89.  libcblas
90.  libedit
91.  libffi
92.  _libgcc_mutex
93.  libgcc-ng
94.  libgfortran-ng
95.  libglu
96.  libiconv
97.  liblapack
98.  liblapacke
99.  libopenblas
100.  libopencv
101.  libopus
102.  libpng
103.  libprotobuf
104.  libsodium
105.  libssh2
106.  libstdcxx-ng
107.  libtiff
108.  libtool
109.  libuuid
110.  libvpx
111.  libwebp
112.  libxcb
113.  libxml2
114.  lmdb
115.  lz4-c
116.  markdown
117.  markupsafe
118.  marshmallow
119.  matplotlib
120.  matplotlib-base
121.  mistune
122.  mkl
123.  mkl_fft
124.  mkl_random
125.  mkl-service
126.  mock
127.  more-itertools
128.  nbconvert
129.  nbformat
130.  ncurses
131.  nettle
132.  networkx
133.  notebook
134.  numpy
135.  numpy-base
136.  olefile
137.  openblas
138.  opencv
139.  openh264
140.  openssl
141.  opt_einsum
142.  packaging
143.  pandas
144.  pandoc
145.  pandocfilters
146.  pango
147.  parso
148.  pexpect
149.  pickleshare
150.  pillow
151.  pip
152.  pixman
153.  pluggy
154.  progressbar2
155.  prometheus_client
156.  prompt_toolkit
157.  prompt-toolkit
158.  protobuf
159.  ptyprocess
160.  py
161.  pybind11
162.  py-boost
163.  pycosat
Press any key to continue...163.  pycosat
164.  pycparser
165.  pydot
166.  pygments
167.  py-opencv
168.  pyopenssl
169.  pyparsing
170.  pyqt
171.  pyrsistent
172.  pysocks
173.  pytest
174.  pytest-runner
175.  python
176.  python-dateutil
177.  python-gflags
178.  python-graphviz
179.  python-leveldb
180.  python-utils
181.  pytz
182.  pywavelets
183.  pyyaml
184.  pyzmq
185.  qt
186.  qtconsole
187.  qtpy
188.  readline
189.  requests
190.  ruamel_yaml
191.  scikit-image
192.  scikit-learn
193.  scipy
194.  send2trash
195.  setuptools
196.  sip
197.  six
198.  snappy
199.  sqlite
200.  tensorboard
201.  tensorflow
202.  tensorflow-base
203.  tensorflow-estimator
204.  termcolor
205.  terminado
206.  testpath
207.  _tflow_select
208.  threadpoolctl
209.  tk
210.  toolz
211.  tornado
212.  tqdm
213.  traitlets
214.  urllib3
215.  wcwidth
216.  webencodings
217.  werkzeug
218.  wheel
219.  widgetsnbextension
220.  wrapt
221.  x264
222.  xcompiler
223.  xorg-libice
224.  xorg-libsm
225.  xorg-libx11
226.  xorg-libxext
227.  xorg-libxpm
228.  xorg-libxrender
229.  xorg-libxt
230.  xorg-renderproto
231.  xorg-xextproto
232.  xorg-xproto
233.  xz
234.  yaml
235.  yaml-cpp
236.  zeromq
237.  zipp
238.  zlib
239.  zstd

BY ELECTING TO CONTINUE, YOU ACKNOWLEDGE AND AGREE, FOR YOURSELF AND ON BEHALF
OF YOUR EMPLOYER (IF APPLICABLE), THAT XILINX IS NOT DISTRIBUTING TO YOU IN
THIS FILE ANY OF THE AFORMENTIONED SOFTWARE OR DEPENDENCIES, AND THAT YOU ARE
SOLELY RESPONSIBLE FOR THE INSTALLATION OF SUCH SOFTWARE AND DEPENDENCIES ON
YOUR SYSTEM AND FOR CAREFULLY REVIEWING AND ABIDING BY THE TERMS AND CONDITIONS
OF ANY LICENSE AGREEMENTS TO THE EXTENT THAT THEY GOVERN SUCH SOFTWARE AND DEPENDENCIES

Press any key to continue...

Do you agree to the terms and wish to proceed [y/n]? y
find: ‘/dev/dri’: No such file or directory
Setting up root 's environment in the Docker container...
 WARNING: You are running Vitis AI Docker container as root. 
For security reasons, consider running as a regular user:
    $ sh docker_run.sh 

OR

    $ docker run -e UID=$(id -u) -e GID=$(id -g) args...

You will be running as vitis-ai-user with non-root UID/GID in Vitis AI Docker container. 


==========================================
 
__      ___ _   _                   _____
\ \    / (_) | (_)            /\   |_   _|
 \ \  / / _| |_ _ ___ ______ /  \    | |
  \ \/ / | | __| / __|______/ /\ \   | |
   \  /  | | |_| \__ \     / ____ \ _| |_
    \/   |_|\__|_|___/    /_/    \_\_____|
 
==========================================

Docker Image Version:  1.3.598 
Build Date: 2021-02-18
VAI_ROOT: /opt/vitis_ai

For TensorFlow 1.15 Workflows do:
     conda activate vitis-ai-tensorflow 
For Caffe Workflows do:
     conda activate vitis-ai-caffe 
For Neptune Workflows do:
     conda activate vitis-ai-neptune 
For PyTorch Workflows do:
     conda activate vitis-ai-pytorch 
For TensorFlow 2.3 Workflows do:
     conda activate vitis-ai-tensorflow2 
Vitis-AI /workspace > 
Vitis-AI /workspace > 
Vitis-AI /workspace > conda activate vitis-ai-tensorflow2
(vitis-ai-tensorflow2) Vitis-AI /workspace > 
(vitis-ai-tensorflow2) Vitis-AI /workspace > 
(vitis-ai-tensorflow2) Vitis-AI /workspace > 

```

#### Building Docker from Recipe

There are two types of docker recipes provided - CPU recipe and GPU recipe. If you have a compatible nVidia graphics card with CUDA support, you could use GPU recipe; otherwise you could use CPU recipe.

**CPU Docker**

Use below commands to build the CPU docker:
```
cd setup/docker
./docker_build_cpu.sh
```
To run the CPU docker, use command:
```
./docker_run.sh xilinx/vitis-ai-cpu:latest
```
**GPU Docker**

Use below commands to build the GPU docker:
```
cd setup/docker
./docker_build_gpu.sh
```
To run the GPU docker, use command:
```
./docker_run.sh xilinx/vitis-ai-gpu:latest
```
Please use the file **./docker_run.sh** as a reference for the docker launching scripts, you could make necessary modification to it according to your needs.
More Detail can be found here: [Run Docker Container](docs/install_docker/load_run_docker.md)

**X11 Support for Running Vitis AI Docker with Alveo**

If you are running Vitis AI docker with Alveo card and want to use X11 support for graphics (for example, some demo applications in VART and Vitis-AI-Library for Alveo need to display images or video), please add following line into the *docker_run_params* variable definition in *docker_run.sh* script:

~~~
-e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/tmp/.Xauthority \
~~~

And after the docker starts up, run following command lines:

~~~
cp /tmp/.Xauthority ~/
sudo chown vitis-ai-user:vitis-ai-group ~/.Xauthority
~~~

Please note before running this script, please make sure either you have local X11 server running if you are using Windows based ssh terminal to connect to remote server, or you have run **xhost +** command at a command terminal if you are using Linux with Desktop. Also if you are using ssh to connect to the remote server, remember to enable *X11 Forwarding* option either with Windows ssh tools setting or with *-X* options in ssh command line.



 ### Get Started with Examples
  - [VART](demo/VART/README.md)
  - [Vitis AI Library](demo/Vitis-AI-Library/README.md)
  - [Examples](examples/README.md)
  - [Vitis AI DNNDK samples](demo/DNNDK)


## Programming with Vitis AI

Vitis AI offers a unified set of high-level C++/Python programming APIs to run AI applications across edge-to-cloud platforms, including DPU for Alveo, and DPU for Zynq Ultrascale+ MPSoC and Zynq-7000. It brings the benefits to easily port AI applications from cloud to edge and vice versa. 8 samples in [VART Samples](demo/VART) are available to help you get familiar with the unfied programming APIs.


| ID | Example Name          | Models              | Framework  | Notes                                                                     |
|----|-----------------------|---------------------|------------|---------------------------------------------------------------------------|
| 1  | resnet50              | ResNet50            | Caffe      | Image classification with VART C\+\+ APIs\.                   |
| 2  | resnet50\_mt\_py      | ResNet50            | TensorFlow | Multi\-threading image classification with VART Python APIs\. |
| 3  | inception\_v1\_mt\_py | Inception\-v1       | TensorFlow | Multi\-threading image classification with VART Python APIs\. |
| 4  | pose\_detection       | SSD, Pose detection | Caffe      | Pose detection with VART C\+\+ APIs\.                         |
| 5  | video\_analysis       | SSD                 | Caffe      | Traffic detection with VART C\+\+ APIs\.                      |
| 6  | adas\_detection       | YOLO\-v3            | Caffe      | ADAS detection with VART C\+\+ APIs\.                         |
| 7  | segmentation          | FPN                 | Caffe      | Semantic segmentation with VART C\+\+ APIs\.                  |
| 8  | squeezenet\_pytorch   | Squeezenet          | Pytorch    | Image classification with VART C\+\+ APIs\.                   |

For more information, please refer to [Vitis AI User Guide](https://www.xilinx.com/html_docs/vitis_ai/1_3/zmw1606771874842.html)


## References
- [Vitis AI Overview](https://www.xilinx.com/products/design-tools/vitis/vitis-ai.html)
- [Vitis AI User Guide](https://www.xilinx.com/html_docs/vitis_ai/1_3/zmw1606771874842.html)
- [Vitis AI Model Zoo with Performance & Accuracy Data](models/AI-Model-Zoo)
- [Vitis AI Tutorials](https://github.com/Xilinx/Vitis-In-Depth-Tutorial/tree/master/Machine_Learning)
- [Developer Articles](https://developer.xilinx.com/en/get-started/ai.html)

## [System Requirements](docs/system_requirements.md)

## Questions and Support
- [FAQ](docs/faq.md)
- [Vitis AI Forum](https://forums.xilinx.com/t5/AI-and-Vitis-AI/bd-p/AI)
- [Third Party Source](docs/Thirdpartysource.md)

[models]: docs/models.md
[Amazon AWS EC2 F1]: https://aws.amazon.com/marketplace/pp/B077FM2JNS
[Xilinx Virtex UltraScale+ FPGA VCU1525 Acceleration Development Kit]: https://www.xilinx.com/products/boards-and-kits/vcu1525-a.html
[AWS F1 Application Execution on Xilinx Virtex UltraScale Devices]: https://github.com/aws/aws-fpga/blob/master/SDAccel/README.md
[Release Notes]: docs/release-notes/1.x.md
[UG1023]: https://www.xilinx.com/support/documentation/sw_manuals/xilinx2017_4/ug1023-sdaccel-user-guide.pdf
[FAQ]: docs/faq.md
[ML Suite Overview]: docs/ml-suite-overview.md
[Webinar on Xilinx FPGA Accelerated Inference]: https://event.on24.com/wcc/r/1625401/2D3B69878E21E0A3DA63B4CDB5531C23?partnerref=Mlsuite
[Vitis AI Forum]: https://forums.xilinx.com/t5/AI-and-Vitis-AI/bd-p/AI
[ML Suite Lounge]: https://www.xilinx.com/products/boards-and-kits/alveo/applications/xilinx-machine-learning-suite.html
[Models]: https://www.xilinx.com/products/boards-and-kits/alveo/applications/xilinx-machine-learning-suite.html#gettingStartedCloud
[whitepaper here]: https://www.xilinx.com/support/documentation/white_papers/wp504-accel-dnns.pdf

   ```
