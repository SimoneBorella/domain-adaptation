# domain-adaptation
Domain adaptation on classification task with AlexNet and PACS dataset

## Results

Model: `AlexNet (Baseline)`

Optimizer: `SGD(lr, momentum=0.9, weight_decay=0.0005)`

Scheduler: `StepLR(lr, step_size)`

Train dataset: `Cartoon`

Test dataset: `Sketch`

| MODEL VERSION | LR     | NUM_EPOCHS | STEP_SIZE  | TRAIN ACCURACY | TEST ACCURACY |
|---------------|--------|------------|------------|----------------|---------------|
| 0             | 0.1    | 100        | 60         | 1.000          | 0.510         |
| **1**             | **0.01**   | **80**         | **35**         | **1.000**          | **0.567**         |
| 2             | 0.005  | 60         | 35         | 1.000          | 0.496         |



Model: `AlexNet (DANN)`

Optimizer: `SGD(lr, momentum=0.9, weight_decay=0.0005)`

Scheduler: `StepLR(lr, step_size)`

Train dataset: `Cartoon`

Test dataset: `Sketch`

| MODEL VERSION | LR     | LAMBDA | NUM_EPOCHS | STEP_SIZE  | TRAIN ACCURACY | TEST ACCURACY |
|---------------|--------|--------|------------|------------|----------------|---------------|
| 0             | 0.1    | 0.5    | 80         | 35         | 0.196          | 0.188         |
| 1             | 0.1    | 1/1e17 | 80         | 35         | 1.000          | 0.567         |
| 2             | 0.01   | 1/1e17 | 80         | 35         | 1.000          | 0.515         |
| 3             | 0.1    | 1/1e7  | 80         | 35         | 1.000          | 0.520         |
| 4             | 0.1    | 1/1e5  | 80         | 35         | 1.000          | 0.555         |
| 5             | 0.1    | 1/1e4  | 80         | 45         | 1.000          | 0.443         |
| 6             | 0.05   | 1/1e4  | 80         | 45         | 1.000          | 0.466         |
| 7             | 0.05   | 1/1e6  | 80         | 45         | 1.000          | 0.549         |
| 8             | 0.05   | 1/1e5  | 80         | 45         | 1.000          | 0.550         |




Model: `AlexNet (DANN Rev)`

Optimizer: `SGD(lr, momentum=0.9, weight_decay=0.0005)`

Scheduler: `StepLR(lr, step_size)`

Train dataset: `Cartoon`

Test dataset: `Sketch`

| MODEL VERSION | LR     | ALPHA  | NUM_EPOCHS | STEP_SIZE  | TRAIN ACCURACY | TEST ACCURACY |
|---------------|--------|--------|------------|------------|----------------|---------------|
| 0             | 0.005  | 0.25   | 30         | 20         | 0.999          | 0.596         |
| 0             | 0.005  | 0.1    | 30         | 20         |           |          |
| 0             | 0.01   | 0.1    | 30         | 20         |           |          |
| 0             | 0.1    | 0.1    | 30         | 20         |           |          |




lr         alpha epoch/size     batch size
5,00E-03	0.1	30/20	        256	        0,5449	        0,5444	0,5464		            0,5452	
5,00E-03	0.1	30/20	        128	        0,4873	        0,5503	0,5400	0,5210	        0,5246
5,00E-03	0.1	30/20	        64	        0,5444	        0,5200	0,5239		            0,5294	
1,00E-03	0.1	30/20	        256	        0,5156	        0,5014	0,5161		            0,5110
1,00E-03	0.1	30/20	        128	        0,5161	        0,4978	0,5342		            0,5160	
1,00E-03	0.1	30/20	        64	        0,5127	        0,5415			                0,5271
1,00E-02	0.1	30/20	        256	        0,5254	        0,5156	0,465		            0,5020	
1,00E-02	0.1	30/20	        128	        0,5537	        0,5444	0,5053	0,5400	        0,5359	
1,00E-02	0.1	30/20	        64	        0,4707	        0,185	0,185		            0,2802