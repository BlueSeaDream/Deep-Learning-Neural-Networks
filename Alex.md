* Alex

Batch = 10


| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 

| 1	| data | Input | 3	| 227x227	| 3	| 227x227		|  | activation	1.55M |
| 2	| conv1 | Convolution | 3	 |  227x227	| 96	|  55x55	| macc	1.05G | activation	2.9M <br> param	34.94k | 
| 3	| relu1	| ReLU | 96	| 55x55 | 96 | 55x55	| comp	2.9M | activation	2.9M |
| 4	| norm1	| LRN | 96	| 55x55	| 96 | 55x55	| macc	14.52M <br> add	2.9M <br> div	5.81M <br> exp	2.9M |
activation	2.9M <br> param	2 |
| 5	| pool1 | Pooling | 96 | 55x55 |	96| 	27x27| 	comp	6.3M | activation	699.84k |


6	conv2	Convolution		96	27x27	256	27x27	
macc	2.24G
activation	1.87M
param	307.46k
7	relu2	ReLU		256	27x27	256	27x27	
comp	1.87M
activation	1.87M
8	norm2	LRN		256	27x27	256	27x27	
macc	9.33M
add	1.87M
div	3.73M
exp	1.87M
activation	1.87M
param	2
9	pool2	Pooling		256	27x27	256	13x13	
comp	3.89M
activation	432.64k
10	conv3	Convolution		256	13x13	384	13x13	
macc	1.5G
activation	648.96k
param	885.12k
11	relu3	ReLU		384	13x13	384	13x13	
comp	648.96k
activation	648.96k
12	conv4	Convolution		384	13x13	384	13x13	
macc	1.12G
activation	648.96k
param	663.94k
13	relu4	ReLU		384	13x13	384	13x13	
comp	648.96k
activation	648.96k
14	conv5	Convolution		384	13x13	256	13x13	
macc	747.6M
activation	432.64k
param	442.62k
15	relu5	ReLU		256	13x13	256	13x13	
comp	432.64k
activation	432.64k
16	pool5	Pooling		256	13x13	256	6x6	
comp	829.44k
activation	92.16k
17	fc6	InnerProduct		256	6x6	4096	1x1	
macc	377.49M
activation	40.96k
param	37.75M
18	relu6	ReLU		4096	1x1	4096	1x1	
comp	40.96k
activation	40.96k
19	drop6	Dropout		4096	1x1	4096	1x1	
comp	40.96k
activation	40.96k
20	fc7	InnerProduct		4096	1x1	4096	1x1	
macc	167.77M
activation	40.96k
param	16.78M
21	relu7	ReLU		4096	1x1	4096	1x1	
comp	40.96k
activation	40.96k
22	drop7	Dropout		4096	1x1	4096	1x1	
comp	40.96k
activation	40.96k
23	fc8	InnerProduct		4096	1x1	1000	1x1	
macc	40.96M
activation	10k
param	4.1M
24	prob	Softmax		1000	1x1	1000	1x1	
add	10k
div	10k
exp	10k
activation	10k
TOTAL							
macc	7.27G
comp	17.69M
add	4.78M
div	9.55M
exp	4.78M
activation	20.81M
param	60.97M
