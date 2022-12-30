# Collision Avoidance
in this example we'll collect an image classification dataset that will be used to help keep JetBot safe! We'll teach JetBot to detect two scenarios free and blocked. We'll use this AI classifier to prevent JetBot from entering dangerous territory.
https://linksharing.samsungcloud.com/yCzbPDlMI6sr
https://linksharing.samsungcloud.com/545Bm73w1nnL




#### Step 1 - Collect data on JetBot


Connect to your robot by navigating to http://<jetbot_ip_address>:8888
Sign in with the default password jetbot
Shutdown all other running notebooks by selecting Kernel -> Shutdown All Kernels...
Navigate to ~/Notebooks/collision_avoidance/
Open and follow the data_collection.ipynb notebook
???+ tip We provide a pre-trained model so you can skip to step 3 if desired. This model was trained on a limited dataset using the Raspberry Pi V2 Camera with wide angle attachment.

#### Step 2 - Train neural network


###Option 1 - Train on Jetson Nano
Connect to your robot by navigating to http://<jetbot_ip_address>:8888
Sign in with the default password jetbot
In the Jupyter Lab tab, navigate to ~/collision_avoidance
Open and follow the train_model_resnet18.ipynb notebook

###Option 2 - Train on other GPU machine
Connect to a GPU machine with PyTorch installed and a Jupyter Lab server running
Upload the collision avoidance training notebook to this machine
Open and follow the train_model_resnet18.ipynb notebook

###Step 3 - Optimize the model on Jetson Nano
Connect to your robot by navigating to https://<jetbot_ip_address>:8888
Sign in with the default password jetbot
Shutdown all other running notebooks by selecting Kernel -> Shutdown All Kernels...
Navigate to ~/Notebooks/road_following
Open and follow the live_demo_resnet18_build_trt.ipynb notebook to optimize the model with TensorRT
###Step 4 - Run live demo on JetBot


Connect to your robot by navigating to http://<jetbot_ip_address>:8888
Sign in with the default password jetbot
Shutdown all other running notebooks by selecting Kernel -> Shutdown All Kernels...
Navigate to ~/Notebooks/collision_avoidance
Open and follow the live_demo_resnet18_trt.ipynb notebook to run the optimized model
???+ caution
JetBot will physically move in this notebook, make sure it has enough space to move around.
