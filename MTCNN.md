* Proposal Net (P-Net)

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |

| 1	| data	| data		| 3	| 12x12	| 3	| 12x12		| activation	432 | 
2	conv1	Convolution		3	12x12	10	10x10	
macc	27k
activation	1000
param	280
3	PReLU1	PReLU		10	10x10	10	10x10	
comp	1000
activation	1000
4	pool1	Pooling		10	10x10	10	5x5	
comp	1000
activation	250
5	conv2	Convolution		10	5x5	16	3x3	
macc	12.96k
activation	144
param	1.46k
6	PReLU2	PReLU		16	3x3	16	3x3	
comp	144
activation	144
7	conv3	Convolution		16	3x3	32	1x1	
macc	4.61k
activation	32
param	4.64k
8	PReLU3	PReLU		32	1x1	32	1x1	
comp	32
activation	32
9	conv4-2	Convolution		32	1x1	4	1x1	
macc	128
activation	4
param	132
10	conv4-1	Convolution		32	1x1	2	1x1	
macc	64
activation	2
param	66
11	prob1	Softmax		2	1x1	2	1x1	
add	2
div	2
exp	2
activation	2
TOTAL							
macc	44.76k
comp	2.18k
add	2
div	2
exp	2
activation	3.04k
param	6.57k
