* VGG16 Batch = 10

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 
| 1	 | data | data |	3	  | 224x224 | 	3	 | 224x224	| | activation	1.51M |
| 2	| conv1_1 | conv 3x3	| 	3	 | 224x224	| 64	| 224x224	| macc	867.04M | activation	32.11M <br> param	1.79k |
| 3	| relu1_1	| relu | 64	 | 224x224 |	64	| 224x224	| comp	32.11M | activation	32.11M |
| 4	| conv1_2	| conv 3x3 | 64 | 224x224 | 	64	| 224x224	| macc	18.5G |activation	32.11M <br> param	36.93k |
| 5	| relu1_2	| relu | 		64| 	224x224| 	64| 	224x224| 	comp	32.11M | activation	32.11M | 
| 6	| pool1 | pooling 2x2 | 		64| 	224x224| 	64| 	112x112| 	comp	32.11M | activation	8.03M |
| 7	| conv2_1 | conv 3x3 | 64 | 	112x112 | 	128 | 	112x112	| macc	9.25G |activation	16.06M <br> param	73.86k |
| 8	| relu2_1	| relu | 128 | 112x112 |128 |	112x112	|comp	16.06M | activation	16.06M |
| 9	| conv2_2 | conv 3x3 | 128 | 112x112 | 128 | 112x112 | macc	18.5G | activation	16.06M <br> param	147.58k |
| 10 | relu2_2 | relu |	128 |	112x112 |	128 |	112x112 |	comp	16.06M | activation	16.06M |
| 11 | pool2 |	pooling 2x2 |	128 |	112x112 |	128 |	56x56 |	comp	16.06M  | activation	4.01M  |
| 12 |	conv3_1 |	conv 3x3 |	128 |	56x56 |	256 |	56x56 |	macc	9.25G  | activation	8.03M<br> param	295.17k |
| 13 |	relu3_1 |	relu |		256 |	56x56 |	256 |	56x56 |	comp	8.03M  | activation	8.03M |
| 14 |	conv3_2 |	conv |		256 |	56x56 |	256 |	56x56 |	macc	18.5G |activation	8.03M <br> param	590.08k  |
| 15 |	relu3_2 |	relu |	256 |	56x56 |	256 |	56x56 |	comp	8.03M | activation	8.03M
| 16 |	conv3_3 |	conv |	256	 |56x56	 |256	 |56x56	 |macc	18.5G | activation	8.03M <br> param	590.08k  |
| 17 |	relu3_3 |	relu |		256 |	56x56 |	256 |	56x56 | comp	8.03M | activation	8.03M |
| 18 |	pool3 |	pooling 2x2 |	256 |	56x56 |	256 |	28x28 |	comp	8.03M | activation	2.01M  |
| 19 |	conv4_1 |	conv 3x3 |		256 |	28x28 |	512 |	28x28 |	macc	9.25G | activation	4.01M <br> param	1.18M  |
| 20 |	relu4_1 |	relu |		512 |	28x28 |	512 |	28x28 |	comp 4.01M | activation	4.01M  |
| 21 |	conv4_2 |	conv |		512 |	28x28 |	512 |	28x28 |	macc	18.5G  | activation	4.01M <br> param	2.36M  |
| 22 |	relu4_2  | relu |		512 |	28x28 |	512 |	28x28 |	comp	4.01M | activation	4.01M |
| 23 |	conv4_3	| conv	3x3 |	512	|28x28	|512	|28x28 |	macc	18.5G |activation	4.01M <br> param	2.36M |
| 24 |	relu4_3 |	relu |		512	| 28x28	| 512 |	28x28	| comp	4.01M | activation	4.01M |
| 25 |	pool4 |	pooling 2x2 |		512	| 28x28 |	512	| 14x14 |	comp	4.01M | activation	1M |
| 26 |	conv5_1	| conv 3x3 |		512 |	14x14 |	512 |	14x14 |	macc	4.62G | activation	1M <br> param	2.36M |
| 27 |	relu5_1	| relu | 512 | 14x14 |	512 |	14x14 |	comp	1M | activation	1M |
| 28 |	conv5_2	| conv 3x3 |	512 |	14x14 |	512 |	14x14	| macc	4.62G | activation	1M <br> param	2.36M |
| 29 |	relu5_2	| relu | 512 | 14x14 | 512 | 14x14 | comp	1M | activation	1M |
| 30 |	conv5_3	| conv 3x3 | 512 |	14x14 |	512 |	14x14 |	macc	4.62G | activation	1M <br> param	2.36M |
| 31 |	relu5_3	| relu | 512 | 14x14 |	512	| 14x14	| comp	1M | activation	1M |
| 32 |	pool5	| pooling 2x2 |	512 |	14x14 |	512	 | 7x7 |	comp	1M | activation	250.88k |
| 33 |	fc6	| inner product	|	512	| 7x7 |	4096 | 1x1 | 	macc	1.03G | activation	40.96k <br> param	102.76M |
| 34 |	relu6	| relu | 4096 |	1x1	| 4096 | 1x1 |	comp	40.96k | activation	40.96k |
| 35 |	drop6	| dropout |	4096 | 1x1 | 4096 |	1x1	| comp	40.96k | activation	40.96k |
| 36 |	fc7	| inner product	| 4096 | 1x1 | 4096 |	1x1	| macc	167.77M | activation	40.96k <br> param	16.78M |
| 37 |	relu7	| relu | 4096 |	1x1 |	4096 |	1x1	| comp	40.96k | activation	40.96k |
| 38 |	drop7	| dropout |	4096 |	1x1	| 4096 |	1x1	| comp	40.96k | activation	40.96k |
| 39 |	fc8	| inner product |	4096 | 1x1 | 1000 |	1x1	| macc	40.96M | activation	10k <br> param	4.1M |
| 40 |	prob	| softmax |	1000 |	1x1 |	1000 |	1x1	| add	10k <br> div	10k <br> exp	10k  <br>  activation	10k |
| TOTAL |	| | | | | | macc	154.7G  <br> comp	196.85M  <br> add	10k  <br>  div	10k  <br> exp	10k | activation	288.03M <br> param	138.36M |
