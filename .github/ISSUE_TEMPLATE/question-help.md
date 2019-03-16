My English is not very good. Thank you in advance for reading my questions and helping me.
This problem has been bothering me for a week.
When I enter instructions"pip install --upgrade torch-scatter",it will generate the following error results:

 user@ubuntu:~$ pip install --upgrade torch-scatter
Collecting torch-scatter
  Using cached https://files.pythonhosted.org/packages/d4/83/67eeea00c2db1959e2ff95d8680dbd756977bfab254bda8658f09dc3bc11/torch_scatter-1.1.2.tar.gz
Building wheels for collected packages: torch-scatter
  Building wheel for torch-scatter (setup.py) ... error
  Complete output from command /home/user/anaconda/envs/wangqi/bin/python -u -c "import setuptools, tokenize;__file__='/tmp/pip-install-hfb08iri/torch-scatter/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" bdist_wheel -d /tmp/pip-wheel-gfntnfww --python-tag cp35:
  running bdist_wheel
  running build
  running build_py
  creating build
  creating build/lib.linux-x86_64-3.5
  creating build/lib.linux-x86_64-3.5/test
  copying test/test_forward.py -> build/lib.linux-x86_64-3.5/test
  copying test/test_std.py -> build/lib.linux-x86_64-3.5/test
  copying test/utils.py -> build/lib.linux-x86_64-3.5/test
  copying test/test_multi_gpu.py -> build/lib.linux-x86_64-3.5/test
  copying test/test_backward.py -> build/lib.linux-x86_64-3.5/test
  copying test/__init__.py -> build/lib.linux-x86_64-3.5/test
  creating build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/add.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/mean.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/std.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/min.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/mul.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/max.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/sub.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/__init__.py -> build/lib.linux-x86_64-3.5/torch_scatter
  copying torch_scatter/div.py -> build/lib.linux-x86_64-3.5/torch_scatter
  creating build/lib.linux-x86_64-3.5/torch_scatter/utils
  copying torch_scatter/utils/gen.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
  copying torch_scatter/utils/ext.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
  copying torch_scatter/utils/__init__.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
  running build_ext
  building 'torch_scatter.scatter_cpu' extension
  creating build/temp.linux-x86_64-3.5
  creating build/temp.linux-x86_64-3.5/cpu
  gcc -pthread -Wsign-compare -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes -fPIC -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cpu/scatter.cpp -o build/temp.linux-x86_64-3.5/cpu/scatter.o -Wno-unused-variable -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cpu -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
  cc1plus: warning: command line option ‘-Wstrict-prototypes’ is valid for C/ObjC but not for C++
  g++ -pthread -shared -L/home/user/anaconda/envs/wangqi/lib -Wl,-rpath=/home/user/anaconda/envs/wangqi/lib,--no-as-needed build/temp.linux-x86_64-3.5/cpu/scatter.o -L/home/user/anaconda/envs/wangqi/lib -lpython3.5m -o build/lib.linux-x86_64-3.5/torch_scatter/scatter_cpu.cpython-35m-x86_64-linux-gnu.so
  building 'torch_scatter.scatter_cuda' extension
  creating build/temp.linux-x86_64-3.5/cuda
  gcc -pthread -Wsign-compare -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes -fPIC -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/usr/local/cuda:/usr/local/cuda-8.0/include -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cuda/scatter.cpp -o build/temp.linux-x86_64-3.5/cuda/scatter.o -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
  cc1plus: warning: command line option ‘-Wstrict-prototypes’ is valid for C/ObjC but not for C++
  /usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/usr/local/cuda:/usr/local/cuda-8.0/include -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cuda/scatter_kernel.cu -o build/temp.linux-x86_64-3.5/cuda/scatter_kernel.o -D__CUDA_NO_HALF_OPERATORS__ -D__CUDA_NO_HALF_CONVERSIONS__ -D__CUDA_NO_HALF2_OPERATORS__ --compiler-options '-fPIC' -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
  unable to execute '/usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc': No such file or directory
  error: command '/usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc' failed with exit status 1

  ----------------------------------------
  Failed building wheel for torch-scatter
  Running setup.py clean for torch-scatter
Failed to build torch-scatter
Installing collected packages: torch-scatter
  Running setup.py install for torch-scatter ... error
    Complete output from command /home/user/anaconda/envs/wangqi/bin/python -u -c "import setuptools, tokenize;__file__='/tmp/pip-install-hfb08iri/torch-scatter/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" install --record /tmp/pip-record-5rq4itoo/install-record.txt --single-version-externally-managed --compile:
    running install
    running build
    running build_py
    creating build
    creating build/lib.linux-x86_64-3.5
    creating build/lib.linux-x86_64-3.5/test
    copying test/test_forward.py -> build/lib.linux-x86_64-3.5/test
    copying test/test_std.py -> build/lib.linux-x86_64-3.5/test
    copying test/utils.py -> build/lib.linux-x86_64-3.5/test
    copying test/test_multi_gpu.py -> build/lib.linux-x86_64-3.5/test
    copying test/test_backward.py -> build/lib.linux-x86_64-3.5/test
    copying test/__init__.py -> build/lib.linux-x86_64-3.5/test
    creating build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/add.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/mean.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/std.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/min.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/mul.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/max.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/sub.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/__init__.py -> build/lib.linux-x86_64-3.5/torch_scatter
    copying torch_scatter/div.py -> build/lib.linux-x86_64-3.5/torch_scatter
    creating build/lib.linux-x86_64-3.5/torch_scatter/utils
    copying torch_scatter/utils/gen.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
    copying torch_scatter/utils/ext.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
    copying torch_scatter/utils/__init__.py -> build/lib.linux-x86_64-3.5/torch_scatter/utils
    running build_ext
    building 'torch_scatter.scatter_cpu' extension
    creating build/temp.linux-x86_64-3.5
    creating build/temp.linux-x86_64-3.5/cpu
    gcc -pthread -Wsign-compare -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes -fPIC -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cpu/scatter.cpp -o build/temp.linux-x86_64-3.5/cpu/scatter.o -Wno-unused-variable -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cpu -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
    cc1plus: warning: command line option ‘-Wstrict-prototypes’ is valid for C/ObjC but not for C++
    g++ -pthread -shared -L/home/user/anaconda/envs/wangqi/lib -Wl,-rpath=/home/user/anaconda/envs/wangqi/lib,--no-as-needed build/temp.linux-x86_64-3.5/cpu/scatter.o -L/home/user/anaconda/envs/wangqi/lib -lpython3.5m -o build/lib.linux-x86_64-3.5/torch_scatter/scatter_cpu.cpython-35m-x86_64-linux-gnu.so
    building 'torch_scatter.scatter_cuda' extension
    creating build/temp.linux-x86_64-3.5/cuda
    gcc -pthread -Wsign-compare -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes -fPIC -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/usr/local/cuda:/usr/local/cuda-8.0/include -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cuda/scatter.cpp -o build/temp.linux-x86_64-3.5/cuda/scatter.o -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
    cc1plus: warning: command line option ‘-Wstrict-prototypes’ is valid for C/ObjC but not for C++
    /usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/torch/csrc/api/include -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/TH -I/home/user/.local/lib/python3.5/site-packages/torch/lib/include/THC -I/usr/local/cuda:/usr/local/cuda-8.0/include -I/home/user/anaconda/envs/wangqi/include/python3.5m -c cuda/scatter_kernel.cu -o build/temp.linux-x86_64-3.5/cuda/scatter_kernel.o -D__CUDA_NO_HALF_OPERATORS__ -D__CUDA_NO_HALF_CONVERSIONS__ -D__CUDA_NO_HALF2_OPERATORS__ --compiler-options '-fPIC' -DTORCH_API_INCLUDE_EXTENSION_H -DTORCH_EXTENSION_NAME=scatter_cuda -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11
    unable to execute '/usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc': No such file or directory
    error: command '/usr/local/cuda:/usr/local/cuda-8.0/bin/nvcc' failed with exit status 1

    ----------------------------------------
Command "/home/user/anaconda/envs/wangqi/bin/python -u -c "import setuptools, tokenize;__file__='/tmp/pip-install-hfb08iri/torch-scatter/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" install --record /tmp/pip-record-5rq4itoo/install-record.txt --single-version-externally-managed --compile" failed with error code 1 in /tmp/pip-install-hfb08iri/torch-scatter/

The previous CUDA and nvcc versions never match. Whether I install cuda8.0 or 9.0 or 10.0, and enter the corresponding instructions for installing pytorch, "import torch; print(torch.version.cuda)" will show 9.0.176.I don't know if it has anything to do with the above errors that caused nvcc to fail to find.
