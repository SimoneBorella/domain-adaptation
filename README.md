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
| **1**             | **0.1**    | **1/1e17** | **80**         | **35**         | **1.000**          | **0.567**         |
| 2             | 0.01   | 1/1e17 | 80         | 35         | 1.000          | 0.515         |
| 3             | 0.1    | 1/1e7  | 80         | 35         | 1.000          | 0.520         |
| 4             | 0.1    | 1/1e5  | 80         | 35         | 1.000          |          |
| 5             | 0.01   | 1/1e13 | 80         | 35         | 1.000          |          |
