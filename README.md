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

 - Clone the Vitis-AI repository to obtain the examples, reference code, and scripts.
    ```bash
    git clone --recurse-submodules https://github.com/yu3peng/Vitis-AI  

    chown -R 1000:1000 Vitis-AI

    cd Vitis-AI
    ```

#### Using Pre-built Docker

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
Vitis-AI /workspace > conda activate vitis-ai-caffe
(vitis-ai-caffe) Vitis-AI /workspace > source /vitis_ai_home/setup/alveo/u200_u250/overlaybins/setup.sh
------------------
Using VAI_HOME
------------------
/vitis_ai_home

---------------------
Verifying XILINX_XRM
---------------------
---------------------
Using LD_LIBRARY_PATH
---------------------
/opt/xilinx/xrt/lib:/usr/lib:/usr/lib/x86_64-linux-gnu:/usr/local/lib:/opt/vitis_ai/conda/envs/vitis-ai-tensorflow/lib
--------------------
Vitis-AI Flow
---------------------
-------------------
Using LIBXDNN_PATH
-------------------
/opt/vitis_ai/conda/envs/vitis-ai-caffe/lib/libxfdnn.so

-------------------
PYTHONPATH
-------------------


---------------------
Verifying XILINX_XRT
---------------------
XILINX_XRT        : /opt/xilinx/xrt
PATH              : /opt/xilinx/xrt/bin:/opt/vitis_ai/conda/envs/vitis-ai-caffe/bin:/opt/vitis_ai/conda/bin:/opt/vitis_ai/conda/condabin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
LD_LIBRARY_PATH   : /opt/xilinx/xrt/lib:/opt/vitis_ai/conda/envs/vitis-ai-caffe/lib:/opt/xilinx/xrt/lib:/usr/lib:/usr/lib/x86_64-linux-gnu:/usr/local/lib:/opt/vitis_ai/conda/envs/vitis-ai-tensorflow/lib
PYTHONPATH        : /opt/xilinx/xrt/python:
(vitis-ai-caffe) Vitis-AI /workspace > cd $VAI_HOME/examples/DPUCADX8G/face_detect/FDDB
(vitis-ai-caffe) Vitis-AI /vitis_ai_home/examples/DPUCADX8G/face_detect/FDDB > wget http://vis-www.cs.umass.edu/fddb/originalPics.tar.gz
--2021-05-24 21:37:51--  http://vis-www.cs.umass.edu/fddb/originalPics.tar.gz
Resolving vis-www.cs.umass.edu (vis-www.cs.umass.edu)... 128.119.244.95
Connecting to vis-www.cs.umass.edu (vis-www.cs.umass.edu)|128.119.244.95|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 579061091 (552M) [application/x-gzip]
Saving to: ‘originalPics.tar.gz’

originalPics.tar.gz      100%[===============================>] 552.24M  27.8MB/s    in 20s     

2021-05-24 21:38:11 (27.1 MB/s) - ‘originalPics.tar.gz’ saved [579061091/579061091]

(vitis-ai-caffe) Vitis-AI /vitis_ai_home/examples/DPUCADX8G/face_detect/FDDB > tar -xvf originalPics.tar.gz
(vitis-ai-caffe) Vitis-AI /vitis_ai_home/examples/DPUCADX8G/face_detect/FDDB > cd $VAI_HOME/examples/DPUCADX8G/face_detect/
(vitis-ai-caffe) Vitis-AI /vitis_ai_home/examples/DPUCADX8G/face_detect/FDDB > ./test_visual.sh face_detection_360_640

/python/ face_detection_360_640/face_detection_360_640.prototxt ./work/face_detection_360_640_dec
ent.prototxt FDDB/FDDB_list_dummy.txt FDDB/
360 640
<class 'caffe.net_spec.NetSpec'>
layer {
  name: "data"
  type: "ImageData"
  top: "data"
  top: "label"
  include {
    phase: TRAIN
  }
  transform_param {
    mirror: false
    mean_value: 128.0
  }
  image_data_param {
    source: "FDDB/FDDB_list_dummy.txt"
    batch_size: 50
    shuffle: false
    new_height: 360
    new_width: 640
    root_folder: "FDDB/"
  }
}

before
 layer {
  name: "data"
  type: "Input"
  top: "data"
  input_param {
    shape {
      dim: 1
      dim: 3
      dim: 360
      dim: 640
    }
  }
}
layer {
  name: "L0"
  type: "Convolution"
  bottom: "data"
  top: "L0"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 8
    pad: 2
    kernel_size: 5
    stride: 2
      weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L0_bn"
  type: "BatchNorm"
  bottom: "L0"
  top: "L0_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
   decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu1"
  type: "ReLU"
  bottom: "L0_bn"
  top: "L0_bn"
}
layer {
  name: "L0_1"
  type: "Convolution"
  bottom: "L0_bn"
  top: "L0_1"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 32
    pad: 2
    kernel_size: 5
    stride: 2
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L0_1_bn"
  type: "BatchNorm"
  bottom: "L0_1"
  top: "L0_1_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
   lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu1_1"
  type: "ReLU"
  bottom: "L0_1_bn"
  top: "L0_1_bn"
}
layer {
  name: "cp1"
  type: "Convolution"
  bottom: "L0_1_bn"
  top: "cp1"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 32
    pad: 1
    kernel_size: 3
    stride: 2
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
 name: "cp1_bn"
  type: "BatchNorm"
  bottom: "cp1"
  top: "cp1_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
     }
  }
}
layer {
  name: "relu_cp1"
  type: "ReLU"
  bottom: "cp1_bn"
  top: "cp1_bn"
}
layer {
  name: "L1"
  type: "Convolution"
  bottom: "cp1_bn"
  top: "L1"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 2
    kernel_size: 5
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
   }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L1_bn"
  type: "BatchNorm"
  bottom: "L1"
  top: "L1_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu2"
  type: "ReLU"
  bottom: "L1_bn"
  top: "L1_bn"
}
layer {
  name: "cp2"
  type: "Convolution"
  bottom: "L1_bn"
  top: "cp2"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 1
    kernel_size: 3
    stride: 2
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "cp2_bn"
  type: "BatchNorm"
  bottom: "cp2"
  top: "cp2_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu_cp2"
  type: "ReLU"
  bottom: "cp2_bn"
  top: "cp2_bn"
}
layer {
  name: "L2"
  type: "Convolution"
 bottom: "cp2_bn"
  top: "L2"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 1
    kernel_size: 3
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L2_bn"
  type: "BatchNorm"
  bottom: "L2"
  top: "L2_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu3"
  type: "ReLU"
  bottom: "L2_bn"
  top: "L2_bn"
}
layer {
  name: "L3"
  type: "Convolution"
  bottom: "L2_bn"
  top: "L3"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 1
    kernel_size: 3
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
      }
  }
}
layer {
  name: "L3_bn"
  type: "BatchNorm"
  bottom: "L3"
  top: "L3_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
      }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu4"
  type: "ReLU"
  bottom: "L3_bn"
  top: "L3_bn"
}
layer {
  name: "L4"
  type: "Convolution"
  bottom: "L3_bn"
  top: "L4"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 1
   kernel_size: 3
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L4_bn"
  type: "BatchNorm"
  bottom: "L4"
  top: "L4_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu5"
  type: "ReLU"
  bottom: "L4_bn"
  top: "L4_bn"
}
layer {
  name: "cp5"
  type: "Convolution"
  bottom: "L4_bn"
  top: "cp5"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 64
    pad: 1
    kernel_size: 3
    stride: 2
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "cp5_bn"
  type: "BatchNorm"
  bottom: "cp5"
  top: "cp5_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
 param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu_cp5"
  type: "ReLU"
  bottom: "cp5_bn"
  top: "cp5_bn"
}
layer {
  name: "L5"
  type: "Convolution"
  bottom: "cp5_bn"
  top: "L5"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    pad: 2
    kernel_size: 5
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
 type: "BatchNorm"
  bottom: "L5"
  top: "L5_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu6"
  type: "ReLU"
  bottom: "L5_bn"
  top: "L5_bn"
}
layer {
  name: "L6"
  type: "Convolution"
  bottom: "L5_bn"
  top: "L6"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
     type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L6_bn"
  type: "BatchNorm"
  bottom: "L6"
  top: "L6_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu7"
  type: "ReLU"
  bottom: "L6_bn"
  top: "L6_bn"
}
layer {
  name: "bb-output"
  type: "Convolution"
  bottom: "L6_bn"
  top: "bb-output"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 256
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "pixel-conv"
  type: "Convolution"
  bottom: "L6_bn"
  top: "pixel-conv"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    kernel_size: 1
    weight_filler {  
     num_output: 256
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "pixel-conv"
  type: "Convolution"
  bottom: "L6_bn"
  top: "pixel-conv"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    kernel_size: 1
    weight_filler {
    
    
    
    
layer {
  name: "cp5_bn"
  type: "BatchNorm"
  bottom: "cp5"
  top: "cp5_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu_cp5"
  type: "ReLU"
  bottom: "cp5_bn"
  top: "cp5_bn"
}
layer {
  name: "L5"
  type: "Convolution"
  bottom: "cp5_bn"
  top: "L5"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    pad: 2
    kernel_size: 5
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L5_bn"
  type: "BatchNorm"
  bottom: "L5"
  top: "L5_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu6"
  type: "ReLU"
  bottom: "L5_bn"
  top: "L5_bn"
}
layer {
  name: "L6"
  type: "Convolution"
  bottom: "L5_bn"
  top: "L6"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 1.0
    }
  }
}
layer {
  name: "L6_bn"
  type: "BatchNorm"
  bottom: "L6"
  top: "L6_bn"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  param {
    lr_mult: 0.0
    decay_mult: 0.0
  }
  batch_norm_param {
    moving_average_fraction: 0.8999999761581421
    scale_filler {
      type: "constant"
      value: 1.0
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "relu7"
  type: "ReLU"
  bottom: "L6_bn"
  top: "L6_bn"
}
layer {
  name: "bb-output"
  type: "Convolution"
  bottom: "L6_bn"
  top: "bb-output"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 256
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "pixel-conv"
  type: "Convolution"
  bottom: "L6_bn"
  top: "pixel-conv"
  param {
    lr_mult: 1.0
    decay_mult: 1.0
  }
  param {
    lr_mult: 2.0
    decay_mult: 0.0
  }
  convolution_param {
    num_output: 128
    kernel_size: 1
    weight_filler {
      type: "gaussian"
      std: 0.009999999776482582
    }
    bias_filler {
      type: "constant"
      value: 0.0
    }
  }
}
layer {
  name: "pixel-tile"
  type: "GSTiling"
  bottom: "pixel-conv"
  top: "pixel-conv-tiled"
  gs_tiling_param {
    stride: 8
    reverse: true
  }
}
layer {
  name: "bb-tile"
  type: "GSTiling"
  bottom: "bb-output"
  top: "bb-output-tiled"
  gs_tiling_param {
    stride: 8
    reverse: true
  }
}
layer {
  name: "pixel-loss"
  type: "Softmax"
  bottom: "pixel-conv-tiled"
  top: "pixel-loss"
}

--------------------------------------------------
Output Quantized Train&Test Model:   "./work/quantize_train_test.prototxt"
Output Quantized Train&Test Weights: "./work/quantize_train_test.caffemodel"
Output Deploy Weights: "./work/deploy.caffemodel"
Output Deploy Model:   "./work/deploy.prototxt"
Output Quantize Info for debugging: "./work/quantize_info.txt"
--- Using Local XCLBIN ---
**************************************************
* VITIS_AI Compilation - Xilinx Inc.
**************************************************
GenerateCode: ./work/face_detect
Weights: ./work/deploy.caffemodel
PngFile: None
ConcatStrategy: None
Strategy: all
ScheduleFile: None
DDR: 1024
DSP: 96
Verbose: False
FromTF: True
Memory: 9
Byte per Pixel: 1
Phase: TEST
RankDir: BT
Start compiling ./work/deploy.prototxt

**************************************************
* BUILDING DATA FLOW GRAPH
**************************************************
Writing processed protoxt to /tmp/tmp2w6nqof1:deploy.prototxt
 ... Loading Network Net /tmp/tmp2w6nqof1:deploy.prototxt ./work/deploy.caffemodel 1 <class 'str'> <class 'str'> <class 'int'>
  ... loading static Net
 Combining Nodes 
  _____ 

**************************************************
* BUILDING NETWORK SCHEDULE
**************************************************
**************************************************
* General Graph Manipulations
**************************************************
**************************************************
* Fully connected layers as Convolutions
**************************************************
{'version': 3, 'name': 'rule3', 'images': {'width': range(1, 4095), 'height': range(1, 4095), 'channels': range(3, 4097)}, 'kernels': {'frames': [[1, 1], [1, 2], [1, 3], [1, 4], [1, 5], [1, 6], [1, 7], [1, 8], [1, 9], [1, 10], [1, 11], [1, 12], [1, 13], [1, 14], [1, 15], [2, 1], [2, 2], [2, 3], [2, 4], [2, 5], [2, 6], [2, 7], [2, 8], [2, 9], [2, 10], [2, 11], [2, 12], [2, 13], [2, 14], [2, 15], [3, 1], [3, 2], [3, 3], [3, 4], [3, 5], [3, 6], [3, 7], [3, 8], [3, 9], [3, 10], [3, 11], [3, 12], [3, 13], [3, 14], [3, 15], [4, 1], [4, 2], [4, 3], [4, 4], [4, 5], [4, 6], [4, 7], [4, 8], [4, 9], [4, 10], [4, 11], [4, 12], [4, 13], [4, 14], [4, 15], [5, 1], [5, 2], [5, 3], [5, 4], [5, 5], [5, 6], [5, 7], [5, 8], [5, 9], [5, 10], [5, 11], [5, 12], [5, 13], [5, 14], [5, 15], [6, 1], [6, 2], [6, 3], [6, 4], [6, 5], [6, 6], [6, 7], [6, 8], [6, 9], [6, 10], [6, 11], [6, 12], [6, 13], [6, 14], [6, 15], [7, 1], [7, 2], [7, 3], [7, 4], [7, 5], [7, 6], [7, 7], [7, 8], [7, 9], [7, 10], [7, 11], [7, 12], [7, 13], [7, 14], [7, 15], [8, 1], [8, 2], [8, 3], [8, 4], [8, 5], [8, 6], [8, 7], [8, 8], [8, 9], [8, 10], [8, 11], [8, 12], [8, 13], [8, 14], [8, 15], [9, 1], [9, 2], [9, 3], [9, 4], [9, 5], [9, 6], [9, 7], [9, 8], [9, 9], [9, 10], [9, 11], [9, 12], [9, 13], [9, 14], [9, 15], [10, 1], [10, 2], [10, 3], [10, 4], [10, 5], [10, 6], [10, 7], [10, 8], [10, 9], [10, 10], [10, 11], [10, 12], [10, 13], [10, 14], [10, 15], [11, 1], [11, 2], [11, 3], [11, 4], [11, 5], [11, 6], [11, 7], [11, 8], [11, 9], [11, 10], [11, 11], [11, 12], [11, 13], [11, 14], [11, 15], [12, 1], [12, 2], [12, 3], [12, 4], [12, 5], [12, 6], [12, 7], [12, 8], [12, 9], [12, 10], [12, 11], [12, 12], [12, 13], [12, 14], [12, 15], [13, 1], [13, 2], [13, 3], [13, 4], [13, 5], [13, 6], [13, 7], [13, 8], [13, 9], [13, 10], [13, 11], [13, 12], [13, 13], [13, 14], [13, 15], [14, 1], [14, 2], [14, 3], [14, 4], [14, 5], [14, 6], [14, 7], [14, 8], [14, 9], [14, 10], [14, 11], [14, 12], [14, 13], [14, 14], [14, 15], [15, 1], [15, 2], [15, 3], [15, 4], [15, 5], [15, 6], [15, 7], [15, 8], [15, 9], [15, 10], [15, 11], [15, 12], [15, 13], [15, 14], [15, 15]], 'strides': [[1, 1], [1, 2], [1, 3], [1, 4], [1, 5], [1, 6], [1, 7], [1, 8], [1, 9], [1, 10], [1, 11], [1, 12], [1, 13], [1, 14], [1, 15], [2, 1], [2, 2], [2, 3], [2, 4], [2, 5], [2, 6], [2, 7], [2, 8], [2, 9], [2, 10], [2, 11], [2, 12], [2, 13], [2, 14], [2, 15], [3, 1], [3, 2], [3, 3], [3, 4], [3, 5], [3, 6], [3, 7], [3, 8], [3, 9], [3, 10], [3, 11], [3, 12], [3, 13], [3, 14], [3, 15], [4, 1], [4, 2], [4, 3], [4, 4], [4, 5], [4, 6], [4, 7], [4, 8], [4, 9], [4, 10], [4, 11], [4, 12], [4, 13], [4, 14], [4, 15], [5, 1], [5, 2], [5, 3], [5, 4], [5, 5], [5, 6], [5, 7], [5, 8], [5, 9], [5, 10], [5, 11], [5, 12], [5, 13], [5, 14], [5, 15], [6, 1], [6, 2], [6, 3], [6, 4], [6, 5], [6, 6], [6, 7], [6, 8], [6, 9], [6, 10], [6, 11], [6, 12], [6, 13], [6, 14], [6, 15], [7, 1], [7, 2], [7, 3], [7, 4], [7, 5], [7, 6], [7, 7], [7, 8], [7, 9], [7, 10], [7, 11], [7, 12], [7, 13], [7, 14], [7, 15], [8, 1], [8, 2], [8, 3], [8, 4], [8, 5], [8, 6], [8, 7], [8, 8], [8, 9], [8, 10], [8, 11], [8, 12], [8, 13], [8, 14], [8, 15], [9, 1], [9, 2], [9, 3], [9, 4], [9, 5], [9, 6], [9, 7], [9, 8], [9, 9], [9, 10], [9, 11], [9, 12], [9, 13], [9, 14], [9, 15], [10, 1], [10, 2], [10, 3], [10, 4], [10, 5], [10, 6], [10, 7], [10, 8], [10, 9], [10, 10], [10, 11], [10, 12], [10, 13], [10, 14], [10, 15], [11, 1], [11, 2], [11, 3], [11, 4], [11, 5], [11, 6], [11, 7], [11, 8], [11, 9], [11, 10], [11, 11], [11, 12], [11, 13], [11, 14], [11, 15], [12, 1], [12, 2], [12, 3], [12, 4], [12, 5], [12, 6], [12, 7], [12, 8], [12, 9], [12, 10], [12, 11], [12, 12], [12, 13], [12, 14], [12, 15], [13, 1], [13, 2], [13, 3], [13, 4], [13, 5], [13, 6], [13, 7], [13, 8], [13, 9], [13, 10], [13, 11], [13, 12], [13, 13], [13, 14], [13, 15], [14, 1], [14, 2], [14, 3], [14, 4], [14, 5], [14, 6], [14, 7], [14, 8], [14, 9], [14, 10], [14, 11], [14, 12], [14, 13], [14, 14], [14, 15], [15, 1], [15, 2], [15, 3], [15, 4], [15, 5], [15, 6], [15, 7], [15, 8], [15, 9], [15, 10], [15, 11], [15, 12], [15, 13], [15, 14], [15, 15]], 'padding': [[1, 1], [1, 2], [1, 3], [1, 4], [1, 5], [1, 6], [1, 7], [1, 8], [1, 9], [1, 10], [1, 11], [1, 12], [1, 13], [1, 14], [1, 15], [2, 1], [2, 2], [2, 3], [2, 4], [2, 5], [2, 6], [2, 7], [2, 8], [2, 9], [2, 10], [2, 11], [2, 12], [2, 13], [2, 14], [2, 15], [3, 1], [3, 2], [3, 3], [3, 4], [3, 5], [3, 6], [3, 7], [3, 8], [3, 9], [3, 10], [3, 11], [3, 12], [3, 13], [3, 14], [3, 15], [4, 1], [4, 2], [4, 3], [4, 4], [4, 5], [4, 6], [4, 7], [4, 8], [4, 9], [4, 10], [4, 11], [4, 12], [4, 13], [4, 14], [4, 15], [5, 1], [5, 2], [5, 3], [5, 4], [5, 5], [5, 6], [5, 7], [5, 8], [5, 9], [5, 10], [5, 11], [5, 12], [5, 13], [5, 14], [5, 15], [6, 1], [6, 2], [6, 3], [6, 4], [6, 5], [6, 6], [6, 7], [6, 8], [6, 9], [6, 10], [6, 11], [6, 12], [6, 13], [6, 14], [6, 15], [7, 1], [7, 2], [7, 3], [7, 4], [7, 5], [7, 6], [7, 7], [7, 8], [7, 9], [7, 10], [7, 11], [7, 12], [7, 13], [7, 14], [7, 15], [8, 1], [8, 2], [8, 3], [8, 4], [8, 5], [8, 6], [8, 7], [8, 8], [8, 9], [8, 10], [8, 11], [8, 12], [8, 13], [8, 14], [8, 15], [9, 1], [9, 2], [9, 3], [9, 4], [9, 5], [9, 6], [9, 7], [9, 8], [9, 9], [9, 10], [9, 11], [9, 12], [9, 13], [9, 14], [9, 15], [10, 1], [10, 2], [10, 3], [10, 4], [10, 5], [10, 6], [10, 7], [10, 8], [10, 9], [10, 10], [10, 11], [10, 12], [10, 13], [10, 14], [10, 15], [11, 1], [11, 2], [11, 3], [11, 4], [11, 5], [11, 6], [11, 7], [11, 8], [11, 9], [11, 10], [11, 11], [11, 12], [11, 13], [11, 14], [11, 15], [12, 1], [12, 2], [12, 3], [12, 4], [12, 5], [12, 6], [12, 7], [12, 8], [12, 9], [12, 10], [12, 11], [12, 12], [12, 13], [12, 14], [12, 15], [13, 1], [13, 2], [13, 3], [13, 4], [13, 5], [13, 6], [13, 7], [13, 8], [13, 9], [13, 10], [13, 11], [13, 12], [13, 13], [13, 14], [13, 15], [14, 1], [14, 2], [14, 3], [14, 4], [14, 5], [14, 6], [14, 7], [14, 8], [14, 9], [14, 10], [14, 11], [14, 12], [14, 13], [14, 14], [14, 15], [15, 1], [15, 2], [15, 3], [15, 4], [15, 5], [15, 6], [15, 7], [15, 8], [15, 9], [15, 10], [15, 11], [15, 12], [15, 13], [15, 14], [15, 15]], 'dilation': [[1, 1], [1, 2], [1, 4], [1, 8], [1, 16], [2, 1], [2, 2], [2, 4], [2, 8], [2, 16], [4, 1], [4, 2], [4, 4], [4, 8], [4, 16], [8, 1], [8, 2], [8, 4], [8, 8], [8, 16], [16, 1], [16, 2], [16, 4], [16, 8], [16, 16]]}, 'max_filter': 9792, 'dsp': [[96, 32]], 'operations': ['Convolution', 'MaxPool', 'AvgPool', 'EltwiseAdd', 'UpSample', 'Download', 'Upload'], 'upsample': [[1, 1], [1, 2], [1, 4], [1, 8], [2, 1], [2, 2], [2, 4], [2, 8], [4, 1], [4, 2], [4, 4], [4, 8], [8, 1], [8, 2], [8, 4], [8, 8]]}
Inner Product Found 0
Schedule Name: 
{1} -|-0 name data type Input fpga False bottoms [] [Extras None]-  Past [] -> Future []
{1} -|-1 name L0_bn type Convolution fpga True bottoms ['data'] [Extras None]-  Past [] -> Future []
{1} -|-2 name relu1 type ReLU fpga True bottoms ['L0_bn'] [Extras None]-  Past [] -> Future []
{1} -|-3 name L0_1_bn type Convolution fpga True bottoms ['relu1'] [Extras None]-  Past [] -> Future []
{1} -|-4 name relu1_1 type ReLU fpga True bottoms ['L0_1_bn'] [Extras None]-  Past [] -> Future []
{1} -|-5 name cp1_bn type Convolution fpga True bottoms ['relu1_1'] [Extras None]-  Past [] -> Future []
{1} -|-6 name relu_cp1 type ReLU fpga True bottoms ['cp1_bn'] [Extras None]-  Past [] -> Future []
{1} -|-7 name L1_bn type Convolution fpga True bottoms ['relu_cp1'] [Extras None]-  Past [] -> Future []
{1} -|-8 name relu2 type ReLU fpga True bottoms ['L1_bn'] [Extras None]-  Past [] -> Future []
{1} -|-9 name cp2_bn type Convolution fpga True bottoms ['relu2'] [Extras None]-  Past [] -> Future []
{1} -|-10 name relu_cp2 type ReLU fpga True bottoms ['cp2_bn'] [Extras None]-  Past [] -> Future []
{1} -|-11 name L2_bn type Convolution fpga True bottoms ['relu_cp2'] [Extras None]-  Past [] -> Future []
{1} -|-12 name relu3 type ReLU fpga True bottoms ['L2_bn'] [Extras None]-  Past [] -> Future []
{1} -|-13 name L3_bn type Convolution fpga True bottoms ['relu3'] [Extras None]-  Past [] -> Future []
{1} -|-14 name relu4 type ReLU fpga True bottoms ['L3_bn'] [Extras None]-  Past [] -> Future []
{1} -|-15 name L4_bn type Convolution fpga True bottoms ['relu4'] [Extras None]-  Past [] -> Future []
{1} -|-16 name relu5 type ReLU fpga True bottoms ['L4_bn'] [Extras None]-  Past [] -> Future []
{1} -|-17 name cp5_bn type Convolution fpga True bottoms ['relu5'] [Extras None]-  Past [] -> Future []
{1} -|-18 name relu_cp5 type ReLU fpga True bottoms ['cp5_bn'] [Extras None]-  Past [] -> Future []
{1} -|-19 name L5_bn type Convolution fpga True bottoms ['relu_cp5'] [Extras None]-  Past [] -> Future []
{1} -|-20 name relu6 type ReLU fpga True bottoms ['L5_bn'] [Extras None]-  Past [] -> Future []
{1} -|-21 name L6_bn type Convolution fpga True bottoms ['relu6'] [Extras None]-  Past [] -> Future []
{1} -|-22 name relu7 type ReLU fpga True bottoms ['L6_bn'] [Extras None]-  Past [] -> Future []
{1} -|-23 name bb-output type Convolution fpga True bottoms ['relu7'] [Extras None]-  Past [] -> Future []
{1} -|-24 name pixel-conv type Convolution fpga True bottoms ['relu7'] [Extras None]-  Past [] -> Future []
{1} -|-25 name pixel-conv-tiled type GSTiling fpga False bottoms ['pixel-conv'] [Extras None]-  Past [] -> Future []
{1} -|-26 name bb-output-tiled type GSTiling fpga False bottoms ['bb-output'] [Extras None]-  Past [] -> Future []
{1} -|-27 name pixel-loss type Softmax fpga False bottoms ['pixel-conv-tiled'] [Extras None]-  Past [] -> Future []
####################################
**************************************************
* BASE Introduction DeepPhi (aka deeppy) factors
**************************************************
**************************************************
* Deconv to (Upsample)? + Conv
**************************************************
Added Updamples 0 []
**************************************************
*  Maximus AuReLiUs: MAX(x*K,X) = RELU(x, K) 
**************************************************
Removed batch norm - scale 0 []
Removal Dropout
Removed Dropout ? 0 []
Bathnorm-Scale telescoping
Removed SC 0 []
Pre-Bathnorm or Pre-Scale
Removed Pre 0 []
Pre-Bathnorm or Pre-Scale Inner-product
Removed Pre 0 []
Post-Bathnorm or Post-Scale
Removed Post 0 []
Removed ReLU? 11 ['relu1', 'relu1_1', 'relu_cp1', 'relu2', 'relu_cp2', 'relu3', 'relu4', 'relu5', 'relu_cp5', 'relu6', 'relu7']
Removed PreReLU? 0 []
**************************************************
*  Ping Pong Failure preventions 
**************************************************
         Fatty convolutions:  0 []
**************************************************
* ReLU can move before concat if there are Convolutions, Eltwise, or Scale 
**************************************************

**************************************************
* Concat Alignment verification to mod 8             
**************************************************
**************************************************
* Pools can move before concat if there are convs 
**************************************************
**************************************************
* Pipelining Convolution and Pooling
**************************************************

**************************************************
* Concat Alignment verification              
**************************************************

**************************************************
* Concat Alignment verification READ        
**************************************************
**************************************************
* ReLU can move before concat if there are convs, eltwise, Scale 
**************************************************
**************************************************
* CPU Layer will be REMOVED
**************************************************
Enforce Convexity of the FPGA Computation
Schedule Name: 
{1} -|-0 name data type Input fpga False bottoms [] [Extras None]-  Past [] -> Future []
{1} -|-1 name L0_bn type Convolution fpga True bottoms ['data'] [Extras ['relu1']]-  Past [] -> Future ['relu1']
{1} -|-2 name L0_1_bn type Convolution fpga True bottoms ['L0_bn'] [Extras ['relu1_1']]-  Past [] -> Future ['relu1_1']
{1} -|-3 name cp1_bn type Convolution fpga True bottoms ['L0_1_bn'] [Extras ['relu_cp1']]-  Past [] -> Future ['relu_cp1']
{1} -|-4 name L1_bn type Convolution fpga True bottoms ['cp1_bn'] [Extras ['relu2']]-  Past [] -> Future ['relu2']
{1} -|-5 name cp2_bn type Convolution fpga True bottoms ['L1_bn'] [Extras ['relu_cp2']]-  Past [] -> Future ['relu_cp2']
{1} -|-6 name L2_bn type Convolution fpga True bottoms ['cp2_bn'] [Extras ['relu3']]-  Past [] -> Future ['relu3']
{1} -|-7 name L3_bn type Convolution fpga True bottoms ['L2_bn'] [Extras ['relu4']]-  Past [] -> Future ['relu4']
{1} -|-8 name L4_bn type Convolution fpga True bottoms ['L3_bn'] [Extras ['relu5']]-  Past [] -> Future ['relu5']
{1} -|-9 name cp5_bn type Convolution fpga True bottoms ['L4_bn'] [Extras ['relu_cp5']]-  Past [] -> Future ['relu_cp5']
{1} -|-10 name L5_bn type Convolution fpga True bottoms ['cp5_bn'] [Extras ['relu6']]-  Past [] -> Future ['relu6']
{1} -|-11 name L6_bn type Convolution fpga True bottoms ['L5_bn'] [Extras ['relu7']]-  Past [] -> Future ['relu7']
{1} -|-12 name bb-output type Convolution fpga True bottoms ['L6_bn'] [Extras None]-  Past [] -> Future []
{1} -|-13 name pixel-conv type Convolution fpga True bottoms ['L6_bn'] [Extras None]-  Past [] -> Future []
{1} -|-14 name pixel-conv-tiled type GSTiling fpga False bottoms ['pixel-conv'] [Extras None]-  Past [] -> Future []
{1} -|-15 name bb-output-tiled type GSTiling fpga False bottoms ['bb-output'] [Extras None]-  Past [] -> Future []
{1} -|-16 name pixel-loss type Softmax fpga False bottoms ['pixel-conv-tiled'] [Extras None]-  Past [] -> Future []
####################################

 convex_fpga 

CPUS 3
NO FPGA pixel-conv-tiled Layers 19 Time 19
NO FPGA bb-output-tiled Layers 18 Time 19
NO FPGA pixel-loss Layers 17 Time 19
Schedule Name: 
{1} -|-0 name data type Input fpga True bottoms [] [Extras None]-  Past [] -> Future []
{1} -|-1 name L0_bn type Convolution fpga True bottoms ['data'] [Extras ['relu1']]-  Past [] -> Future ['relu1']
{1} -|-2 name L0_1_bn type Convolution fpga True bottoms ['L0_bn'] [Extras ['relu1_1']]-  Past [] -> Future ['relu1_1']
{1} -|-3 name cp1_bn type Convolution fpga True bottoms ['L0_1_bn'] [Extras ['relu_cp1']]-  Past [] -> Future ['relu_cp1']
{1} -|-4 name L1_bn type Convolution fpga True bottoms ['cp1_bn'] [Extras ['relu2']]-  Past [] -> Future ['relu2']
{1} -|-5 name cp2_bn type Convolution fpga True bottoms ['L1_bn'] [Extras ['relu_cp2']]-  Past [] -> Future ['relu_cp2']
{1} -|-6 name L2_bn type Convolution fpga True bottoms ['cp2_bn'] [Extras ['relu3']]-  Past [] -> Future ['relu3']
{1} -|-7 name L3_bn type Convolution fpga True bottoms ['L2_bn'] [Extras ['relu4']]-  Past [] -> Future ['relu4']
{1} -|-8 name L4_bn type Convolution fpga True bottoms ['L3_bn'] [Extras ['relu5']]-  Past [] -> Future ['relu5']
{1} -|-9 name cp5_bn type Convolution fpga True bottoms ['L4_bn'] [Extras ['relu_cp5']]-  Past [] -> Future ['relu_cp5']
{1} -|-10 name L5_bn type Convolution fpga True bottoms ['cp5_bn'] [Extras ['relu6']]-  Past [] -> Future ['relu6']
{1} -|-11 name L6_bn type Convolution fpga True bottoms ['L5_bn'] [Extras ['relu7']]-  Past [] -> Future ['relu7']
{1} -|-12 name bb-output type Convolution fpga True bottoms ['L6_bn'] [Extras None]-  Past [] -> Future []
{1} -|-12 name bb-output_output type Output fpga True bottoms ['bb-output'] [Extras None]-  Past [] -> Future []
{1} -|-13 name pixel-conv type Convolution fpga True bottoms ['L6_bn'] [Extras None]-  Past [] -> Future []
{1} -|-13 name pixel-conv_output type Output fpga True bottoms ['pixel-conv'] [Extras None]-  Past [] -> Future []
{0} 
{0} 
####################################
**************************************************
* * AVG + Scale -> AVG with different scaling  
**************************************************
**************************************************
* * Enrich the graph with quantization information  
**************************************************
Optimizing 1 schedules
**************************************************
* COMPUTING MEMORY REQUIREMENTS
**************************************************
IO @@@ bb-output_output_blob MemoryAllocation(start=0, end=69120, size=69120, extra=[], strategy=[], layout=-1, timestamp=-1, slice=1, shapes=SizeType(batches=1, channels=256, height=12, width=20), replication=Replication(full_sect_num=0, repl_sect_num=0, repl_unit_num=0, repl_unit_width=0, channels_division=0), written=False, specifier='', IO=True)
IO @@@ pixel-conv_output_blob MemoryAllocation(start=0, end=46080, size=46080, extra=[], strategy=[], layout=-1, timestamp=-1, slice=1, shapes=SizeType(batches=1, channels=128, height=12, width=20), replication=Replication(full_sect_num=0, repl_sect_num=0, repl_unit_num=0, repl_unit_width=0, channels_division=0), written=False, specifier='', IO=True)
IO @@@ data_blob MemoryAllocation(start=0, end=22118400, size=22118400, extra=[], strategy=[], layout=-1, timestamp=-1, slice=1, shapes=SizeType(batches=1, channels=3, height=360, width=640), replication=Replication(full_sect_num=0, repl_sect_num=0, repl_unit_num=0, repl_unit_width=0, channels_division=0), written=False, specifier='', IO=True)
Minimum Memory __________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
MAX  1
TOP 5
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
__________
0 ['data'] size:22118400 remap:[] data movement:[]
0       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
__________
2 ['L0_1_bn'] size:6912000 remap:[] data movement:[]
2       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
2       L0_1_bn_blob M[0,1382400] Z=1382400 F=[3] B=[2] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=32, height=90, width=160)
__________
3 ['cp1_bn'] size:1728000 remap:[] data movement:[]
3       L0_1_bn_blob M[0,1382400] Z=1382400 F=[3] B=[2] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=32, height=90, width=160)
3       cp1_bn_blob M[0,345600] Z=345600 F=[4] B=[3] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=32, height=45, width=80)
__________
4 ['L1_bn'] size:691200 remap:[] data movement:[]
4       cp1_bn_blob M[0,345600] Z=345600 F=[4] B=[3] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=32, height=45, width=80)
4       L1_bn_blob M[0,345600] Z=345600 F=[5] B=[4] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=64, height=45, width=80)
Using Hardware Version [3, 3]
**************************************************
* REPLICATION 
**************************************************
Simple Replication
optimized replication: 32 L0_bn
optimized replication: 32 L0_1_bn
optimized replication: 32 cp1_bn
optimized replication: 32 L1_bn
optimized replication: 32 cp2_bn
optimized replication: 32 L2_bn
optimized replication: 32 L3_bn
optimized replication: 32 L4_bn
optimized replication: 32 cp5_bn
optimized replication: 32 L5_bn
replicaiton done
replicaiton done 2
**************************************************
* ALLOCATING DYNAMIC MEMORY SCHEDULE
**************************************************
Allocating Memory all
Trying no-DDR strategies...
You tell me there must be DDR, Skip the AM only
Trying DDR strategies with 0 MB ...
Reset Memory
Trying strategy bottom (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy bottles (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy xXx (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy flip (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy top (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy tops (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy shuffle (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy bottle (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Reset Memory
Trying strategy bysize (DDR: 0 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
No Memory: it is based on the maximum available
__________
1 ['L0_bn'] size:27648000 remap:[] data movement:[]
1       data_blob M[0,22118400] Z=22118400 F=[1] B=[0] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=3, height=360, width=640)
1       L0_bn_blob M[0,5529600] Z=5529600 F=[2] B=[1] E=[] S=['layer'] [] L=-1 T=SizeType(batches=1, channels=8, height=180, width=320)
Initial memory map sizes [0, 9437184, 9437184]
Trying DDR strategies with 1024 MB ...
Reset Memory
Trying strategy bottom (DDR: 1024 MB)
Performing two level schedule strategy all
Reference {'Convolution': ['ddr_to_am', 'ddr_to_ddr', 'am_to_am']}
outs 2
inss 1
 ?????  <dpuv1.codegeneration.hardware.DDR object at 0x7f1c3769cf28> <dpuv1.codegeneration.hardware.DDR object at 0x7f1c375acd68>
Done I instruction:inputs  [] outputs [0] call data
None
BlobInformation(size=22118400, name='data_blob', memory=MemoryAllocation(start=0, end=7372800, size=7372800, extra=[1], strategy=[], layout=1, timestamp=1, slice=1, shapes=SizeType(batches=1, channels=3, height=360, width=640), replication=Replication(full_sect_num=0, repl_sect_num=1, repl_unit_num=3, repl_unit_width=32, channels_division=[3]), written=False, specifier='Input', IO=True), dag=ColorForDAG(active=[3], schedule=-1, forward=[1], backward=[0], extra=None, hook=[]), layer_type=['layer'], data_movement_operations=[], data_movement_operation_costs=[])
Successful Strategy bottom (DDR: 1024 MB)
Done schedule 16 STEPS
**************************************************
* ADDED weight information weights_bit 
**************************************************
**************************************************
* GENERATING OUTPUT REPORTS
**************************************************
schedule_and_parallelism
Minimum Memory 2 ['L0_1_bn'] 9437184
L0_bn_blob M[3907584,9437184] Z=5529600 F=[2] B=[1] E=[1] S=['layer'] ['tops'] L=0 T=SizeType(batches=1, channels=8, height=180, width=320)
L0_1_bn_blob M[0,1382400] Z=1382400 F=[3] B=[2] E=[1] S=['layer'] [] L=0 T=SizeType(batches=1, channels=32, height=90, width=160)
**************************************************
* GENERATING OUTPUT FILES
**************************************************
XDNN Command file: ./work/face_detect
XDNN JSON Report file: ./work/face_detect.json
./work
Path to generatefile exists...
***** Inst JSON
[1] <class 'dpuv1.utils.xdnn_util.dict2attr'>
REP V   BestReplication(FSN=0, RSN=1, RUN=12, RUW=8, FSC=0, RSC=3) SpaceAndTime(space=22118400, time=89, replication=Replication(full_sect_num=0, repl_sect_num=1, repl_unit_num=12, repl_unit_width=8, channels_division=[3]))
V3 Tile L0_bn (23.48936170212766, -360960)
output ddr {(368640, 268435456): MemoryAllocation(start=368640, end=268435456, size=268066816, extra=[], strategy=[], layout=-1, timestamp=-1, slice=-1, shapes=None, replication=Replication(full_sect_num=0, repl_sect_num=0, repl_unit_num=0, repl_unit_width=0, channels_division=0), written=False, specifier='', IO=False)}
input ddr {(7372800, 268435456): MemoryAllocation(start=7372800, end=268435456, size=261062656, extra=[], strategy=[], layout=-1, timestamp=-1, slice=-1, shapes=None, replication=Replication(full_sect_num=0, repl_sect_num=0, repl_unit_num=0, repl_unit_width=0, channels_division=0), written=False, specifier='', IO=False)}
OUTPUT REPORT:
Unsupported Layers: 0
***** Inst JSON Done
* XDNN QUANT JSON  ./work/face_detect_quant.json
***** Inst FILE
REP V   BestReplication(FSN=0, RSN=1, RUN=12, RUW=8, FSC=0, RSC=3) SpaceAndTime(space=22118400, time=14332, replication=Replication(full_sect_num=0, repl_sect_num=1, repl_unit_num=12, repl_unit_width=8, channels_division=[3]))
V3 Tile L0_bn (23.48936170212766, -360960)
***** Inst FILE OUT
***** Inst COLLECT
***** COLLECT CODES 31
# template XNConv id XNOp name kernel_w kernel_h strides_w strides_h padding_w padding_h dilation_w dilation_h preshift scale postshift relu prelu bias inaddr insize_w insize_h inchan outaddr outsize_w outsize_h  outchan weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset 
# template XNDeconv id XNOp name kernel_w kernel_h strides_w strides_h padding_w padding_h dilation_w dilation_h preshift scale postshift relu prelu bias inaddr insize_w insize_h inchan outaddr outsize_w outsize_h  outchan weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset 
# template XNConvP id XNOp name kernel_w kernel_h strides_w strides_h padding_w padding_h dilation_w dilation_h preshift scale postshift relu bias inaddr insize_w insize_h inchan outaddr outsize_w outsize_h  outchan Bypass_Perf_Opt  pool_kernel_w pool_kernel_h pool_strides_w pool_strides_h pool_paddings_w pool_paddings_h pool_fcmode
# template XNUpload id XNOp inaddr insize inchan
# template XNConcat pound id XNOp name start end size dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width MUTE
# template XNInner id XNOp name relu prelu preshift scale postshift matrixheight matrixwidthh inaddr inheight inwidth outaddr outheight outwidth
# template XNGather id XNOp uram_dest ddr_src insize_w insize_h inchan a0 b1 c1 start_row end_row slice full_sect_num repl_sect_num repl_unit_num repl_unit_width srcAddrReadFromImgQ sep comment
# template XNScatter id XNOp uram_src ddr_dest outsize_w outsize_h outchan a0 b1 c1 start_row end_row slice full_sect_num repl_sect_num repl_unit_num repl_unit_width destAddrReadFromImgQ
# template XNEltwise id XNOp name add bn relu prelu inaddrA inaddrB insize_w insize_h inchan outaddr weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset EWA_2nd-Src_AM 
# template XNAvgPool id XNOp name kernel_w kernel_h  strides_w strides_h paddings_w paddings_h inaddr insize_w insize_h inchan outaddr outsize_w outsize_h weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset 
# template XNMaxPool id XNOp name kernel_w kernel_h  strides_w strides_h paddings_w paddings_h inaddr insize_w insize_h inchan outaddr outsize_w outsize_h weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset 
# template XNUpsample id XNOp name kernel_h kernel_w   inaddr insize_h  insize_w  inchan outaddr outsize_w outsize_h method weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset 
# template XNAvgPoolPipelined id XNOp name kernel_w kernel_h  strides_w strides_h paddings_w paddings_h inaddr insize_w insize_h inchan outaddr outsize_w outsize_h weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset conv_name conv_kernel_w conv_kernel_h conv_strides_w conv_strides_h conv_padding_w conv_padding_h conv_dilation_w conv_dilation_h conv_relu conv_prelu conv_bias pool_insize_w pool_insize_h pool_inchan conv_outsize_w
# template XNMaxPoolPipelined id XNOp name kernel_w kernel_h  strides_w strides_h paddings_w paddings_h inaddr insize_w insize_h inchan outaddr outsize_w outsize_h weights_bit slice src_full_sect_num src_repl_sect_num src_repl_unit_num src_repl_unit_width dst_full_sect_num dst_repl_sect_num dst_repl_unit_num dst_repl_unit_width concat_i_am_your_father concat_full_sect_num concat_repl_sect_num concat_repl_unit_num concat_repl_unit_width concat_starting_ch concat_channels wait_download wait_upload wait_conv wait_pool wait_ew wait_upsmpl parallel_read prerelu en_pingpong_weight en_halfrate_mode en_inlinemaxpool srcAddrReadFromImgQ destAddrReadFromImgQ srcAddDDR dstAddDDR tile_width tile_height HAT SRCAM-Buffer_0 SRCAM-Buffer_1 DEST_AM-Buffer_Offset conv_name conv_kernel_w conv_kernel_h conv_strides_w conv_strides_h conv_padding_w conv_padding_h conv_dilation_w conv_dilation_h conv_relu conv_prelu conv_bias pool_insize_w pool_insize_h pool_inchan conv_outsize_w
# 1 XNGather 0x0 0x0 640 360 3 0 1 1 0 359 1 0 1 3 32 1 # Input data data: type=Input, sizes=None, shapes=None, sched 0 Kernel None Strides None Padding None MUTE CODE
# spLiT L0_bn 9437184 ;
2 XNConv L0 5 5 2 2 2 2 1 1 0 32768 25 1 0 1 0x0 640 360 3 0x9f00 320 180 8 1 1 0 1 12 8 0 1 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 1 0 1 0 80 47 1 0 16384 40704 # V3 SPLIT Code :)ddr_to_am
5 XNConv L0_1 5 5 2 2 2 2 1 1 0 32768 22 1 0 1 0x9f00 320 180 8 0x0 160 90 32 1 1 0 1 3 32 0 1 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
7 XNConv cp1 3 3 2 2 1 1 1 1 0 32768 23 1 0 1 0x0 160 90 32 0x3840 80 45 32 1 1 0 1 3 32 0 1 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
9 XNConv L1 5 5 1 1 2 2 1 1 0 32768 21 1 0 1 0x3840 80 45 32 0x0 80 45 64 1 1 0 1 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
11 XNConv cp2 3 3 2 2 1 1 1 1 0 32768 24 1 0 1 0x0 80 45 64 0x1c20 40 23 64 1 1 0 2 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
13 XNConv L2 3 3 1 1 1 1 1 1 0 32768 23 1 0 1 0x1c20 40 23 64 0x0 40 23 64 1 1 0 2 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
15 XNConv L3 3 3 1 1 1 1 1 1 0 32768 23 1 0 1 0x0 40 23 64 0x730 40 23 64 1 1 0 2 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
17 XNConv L4 3 3 1 1 1 1 1 1 0 32768 23 1 0 1 0x730 40 23 64 0x0 40 23 64 1 1 0 2 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
19 XNConv cp5 3 3 2 2 1 1 1 1 0 32768 23 1 0 1 0x0 40 23 64 0x730 20 12 64 1 1 0 2 3 32 0 2 3 32 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
21 XNConv L5 5 5 1 1 2 2 1 1 0 32768 21 1 0 1 0x730 20 12 64 0x0 20 12 128 1 1 0 2 3 32 2 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
23 XNConv L6 1 1 1 1 0 0 1 1 0 32768 23 1 0 1 0x0 20 12 128 0x1e0 20 12 128 1 1 2 0 0 0 2 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
25 XNConv bb-output 1 1 1 1 0 0 1 1 0 32768 24 0 0 1 0x1e0 20 12 128 0x3c0 20 12 256 1 1 2 0 0 0 3 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
27 XNScatter 0x3c0 0x0 20 12 256 0 1 1 0 11 1 3 0 0 0 1 # Output bb-output_output
29 XNConv pixel-conv 1 1 1 1 0 0 1 1 0 32768 22 0 0 1 0x1e0 20 12 128 0x0 20 12 128 1 1 2 0 0 0 2 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 # am_to_am
31 XNScatter 0x0 0x3c000 20 12 128 0 1 1 0 11 1 2 0 0 0 1 # Output pixel-conv_output
**************************************************
* CLEANING PREVIOUS WEIGHTS
**************************************************
**************************************************
* WRITING WEIGHTS
**************************************************
Weight HDF5: ./work/deploy.caffemodel_data.h5
Processing weights for 16 schedule steps: 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16
Done writing weights.
**************************************************
* EUREKA Schedule  PASSED
**************************************************
SUCCESS True
Inputs ['data']
Outputs ['bb-output-tiled', 'pixel-loss']
-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

-------------------
Speaking to Butler 
Response from Butler is: 
errCode: errCode: 2
errCode String: NO_XCLBIN_FOUND
myHandle: 0
valid: 1

(vitis-ai-caffe) Vitis-AI /vitis_ai_home/examples/DPUCADX8G/face_detect >     
  
  
  
      

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
