.. _vasp:

VASP
====

简介
----

VASP全称Vienna Ab-initio Simulation Package，是维也纳大学Hafner小组开发的进行电子结构计算和量子力学-分子动力学模拟软件包。它是目前材料模拟和计算物质科学研究中最流行的商用软件之一。

VASP使用需要得到VASP官方授权。请自行购买VASP license许可，下载和安装。如需协助安装或使用，请发邮件联系我们，附上课题组拥有VASP license的证明。

ARM版VASP
---------

以下版本的使用，需要先邮件联系我们，提供课题组拥有 VASP license 的证明。

ARM平台上运行脚本如下(vasp.slurm):    

.. code:: bash

   #!/bin/bash

   #SBATCH --job-name=test       
   #SBATCH --partition=arm128c256g       
   #SBATCH -N 2            
   #SBATCH --ntasks-per-node=128
   #SBATCH --output=%j.out
   #SBATCH --error=%j.err

   source /lustre/share/singularity/commercial-app/vasp/activate arm

   mpirun -n $SLURM_NTASKS vasp_std

使用如下指令提交：

.. code:: bash

   $ sbatch vasp.slurm
