* VGG16 Batch = 1

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 
| 1	| data	| data		| 3	| 224x224	| 3	| 224x224		| | activation 	150.53k | 
| 2	| conv1_1	| conv | 		3	| 224x224	| 64	| 224x224	| macc	86.7M | activation	3.21M<br>param	1.79k | 
| 3	| relu1_1	| relu		| 64	| 224x224	| 64	| 224x224	| comp	| 3.21M | activation	3.21M | 
| 4	| conv1_2	| convolution	| 	64	| 224x224	| 64	| 224x224	| macc	| 1.85G | activation	3.21M<br>param	36.93k | 
| 5	| relu1_2	| relu | 64	| 224x224	| 64	| 224x224	| comp	3.21M | 	activation	3.21M | 
| 6	| pool1	| pooling	| 	64	| 224x224	| 64	| 112x112	| comp	| 3.21M | activation	802.82k | 
| 7	| conv2_1	| convolution	| 	64	| 112x112	| 128	| 112x112 | macc	| 924.84M | activation	1.61M<br>param	73.86k | 
| 8	| relu2_1	| relu		| 128	| 112x112	| 128	| 112x112	| comp	1.61M | 	activation	1.61M | 
| 9	| conv2_2	| convolution	| 	128	| 112x112	| 128	| 112x112	| macc	| 1.85G | activation	1.61M<br>param	147.58k | 
| 10| relu2_2	| relu	| 	128	| 112x112	| 128	| 112x112	| comp	| 1.61M	| activation	1.61M | 
| 11| 	pool2	| pooling	| 	128	| 112x112	| 128	| 56x56	| comp	1.61M | activation	401.41k | 
| 12	| conv3_1	| convolution	| 128	| 56x56	| 256	| 56x56	| macc	924.84M | activation	802.82k<br>param	295.17k | 
| 13	| relu3_1	relu	| 	256	| 56x56	| 256	| 56x56	| comp	802.82k | activation	802.82k | 
| 14	| conv3_2	| convolution	| 256	| 56x56	| 256	| 56x56	| macc	1.85G | activation	802.82k<br>param	590.08k | 
| 15	| relu3_2	| relu | 256	| 56x56	| 256	| 56x56	| comp	802.82k | activation	802.82k | 
| 16	| conv3_3	| convolution		| 256	| 56x56	| 256	| 56x56	| macc	1.85G | activation	802.82k<br>param	590.08k | 
| 17	| relu3_3	| relu		| 256	| 56x56	| 256	| 56x56	| comp	802.82k | activation	802.82k | 
| 18	| pool3	| pooling		| 256	| 56x56	| 256	| 28x28	| comp	802.82k | activation	200.7k | 
| 19	| conv4_1	| convolution		| 256	| 28x28	| 512	| 28x28	| macc	924.84M | activation	401.41k<br>param	1.18M | 
| 20	| relu4_1	| relu		| 512	| 28x28	| 512	| 28x28	| comp	401.41k | activation	401.41k | 
| 21	| conv4_2	| convolution	| 	512	| 28x28	| 512	| 28x28	| macc	1.85G | activation	401.41k<br>param	2.36M | 
| 22	| relu4_2	| relu	| 	512	| 28x28	| 512	| 28x28	| comp	401.41k | activation	401.41k | 
| 23	| conv4_3	| convolution	| 	512	| 28x28	| 512	| 28x28	| macc	1.85G | activation 401.41k<br>param	2.36M | 
| 24	| relu4_3 | relu	| 512	| 28x28	| 512	| 28x28	| comp	401.41k | activation	401.41k | 
| 25	| pool4	| pooling	| 512	| 28x28	| 512	| 14x14	| comp	401.41k | activation	100.35k | 
| 26	| conv5_1 | convolution | 512	| 14x14	| 512	| 14x14	| macc	462.42M | activation	100.35k<br>param 2.36M | 


27	relu5_1	relu		512	14x14	512	14x14	comp	100.35k
	activation	100.35k
28	conv5_2	convolution		512	14x14	512	14x14	macc	462.42M
	activation	100.35k
param	2.36M
29	relu5_2	relu		512	14x14	512	14x14	comp	100.35k
	activation	100.35k
30	conv5_3	convolution		512	14x14	512	14x14	macc	462.42M
	activation	100.35k
param	2.36M
31	relu5_3	relu		512	14x14	512	14x14	comp	100.35k
	activation	100.35k
32	pool5	pooling		512	14x14	512	7x7	comp	100.35k
	activation	25.09k
33	fc6	inner_product		512	7x7	4096	1x1	macc	102.76M
	activation	4.1k
param	102.76M
34	relu6	relu		4096	1x1	4096	1x1	comp	4.1k
	activation	4.1k
35	drop6	dropout		4096	1x1	4096	1x1	comp	4.1k
	activation	4.1k
36	fc7	inner_product		4096	1x1	4096	1x1	macc	16.78M
	activation	4.1k
param	16.78M
37	relu7	relu		4096	1x1	4096	1x1	comp	4.1k
	activation	4.1k
38	drop7	dropout		4096	1x1	4096	1x1	comp	4.1k
	activation	4.1k
39	fc8	inner_product		4096	1x1	1000	1x1	macc	4.1M
	activation	1000
param	4.1M
40	prob	softmax		1000	1x1	1000	1x1	add	1000
div	1000
exp	1000
	activation	1000
	TOTAL							macc	15.47G
comp	19.69M
add	1000
div	1000
exp	1000
	activation	28.8M
param	138.36M
