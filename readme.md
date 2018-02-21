Deep Learning Recipes for DNA reads and short variants.
=======================================================

Training models from example tensors
------------------------------------

Train a model that predicts variant quality from read tensors and variant annotations:

    python recipes.py train_ref_read_anno \
      --data_dir ./data/g94982_tensors_chr1_channels_last/ \
      --tensor_map read_tensor \
      --id ref_read_anno_model

Train a model that predicts variant quality from read tensors and variant annotations:

    python recipes.py train_ref_read \
      --data_dir ./data/g94982_tensors_chr1_channels_last/ \
      --tensor_map read_tensor \
      --id ref_read_model

Train a model that predicts variant quality from reference sequence and annotations:

    python recipes.py train_reference_annotation \
      --data_dir ./data/example_reference_tensors_chr1/ \
      --tensor_map reference \
      --id ref_anno_model

Train a model that predicts variant quality from reference sequence only:

    python recipes.py train_reference_annotation \
      --data_dir ./data/example_reference_tensors_chr1/ \
      --tensor_map reference \
      --id ref_model

Setting up your environment
---------------------------

We recommend using [anaconda](https://conda.io/docs/user-guide/install/index.html) to handle your python environments. For CPU only libraries:

    conda env create -n gatk -f ./gatkcondaenv_cpu.yml

To use GPU:

    conda env create -n gatk -f ./gatkcondaenv_gpu.yml