* Proposal Net (P-Net)

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 
| 1	| data	| data		| 3	| 12x12	| 3	| 12x12		| activation	432 | 
| 2	| conv1	| Convolution	| 3	| 12x12	| 10	| 10x10 |	macc	27k | activation	1000 | param	280| 
| 3	| PReLU1| 	PReLU	| 	10	| 10x10	| 10	| 10x10	| comp	1000 | activation	1000 | 
| 4	| pool1	| Pooling	| 	10	| 10x10	| 10	| 5x5	| comp	1000 | activation	250 | 
| 5	| conv2	| Convolution	| 10	| 5x5	| 16	| 3x3	| macc	12.96k | activation	144<br>param	1.46k | 
| 6	| PReLU2| 	PReLU	| 	16	| 3x3	| 16	| 3x3	| comp	144 | activation	144
| 7	| conv3	| Convolution		| 16	| 3x3	| 32	| 1x1	| macc	4.61k | activation	32<br>param	4.64k | 
| 8	| PReLU3| 	PReLU		| 32	| 1x1	| 32	| 1x1	| comp	32 | activation	32| 
| 9	| conv4-2	| Convolution	| 	32	| 1x1	| 4	| 1x1 | 	macc	128 | activation	4<br>param	132| 
| 10	| conv4-1	| Convolution	| 	32	| 1x1	| 2	| 1x1	| macc	64 | activation	2<br>param	66 | 
| 11	| prob1	| Softmax		| 2	| 1x1	| 2	| 1x1 | add	2<br>div	2<br>exp	2 | activation	2 |
| TOTAL | | | | | | |	macc	44.76k<br>comp	2.18k | add	2<br>div	2<br>exp	2 | activation	3.04k<br>param	6.57k |


* Refine Net (R-Net)

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 
| 1	| data	| data		| 3	| 24x24	| 3	| 24x24 | activation	1.73k | 
| 2	| conv1	| Convolution	| 	3	| 24x24	| 28	| 22x22 | 	macc	365.9k | activation	13.55k<br>param	784 | 
| 3	| prelu1	| PReLU	| 	28	| 22x22	| 28	| 22x22 | comp	13.55k | activation	13.55k | 
| 4	| pool1	| Pooling	| 28	| 22x22	| 28	| 11x11	| comp	30.49k | activation	3.39k | 
| 5	| conv2	| Convolution		| 28	| 11x11	| 48	| 9x9	| macc	979.78k | activation	3.89k<br>param	12.14k | 
| 6	| prelu2	| PReLU		| 48	| 9x9	| 48	| 9x9 | comp	3.89k | activation	3.89k | 
| 7	| pool2	| Pooling	| 	48	| 9x9	| 48	| 4x4 | comp	6.91k | activation	768 | 
| 8	| conv3	| Convolution	| 	48	| 4x4	| 64	| 3x3 | macc	110.59k | activation	576<br>param	12.35k | 
| 9	| prelu3	| PReLU	| 64	| 3x3	| 64	| 3x3 | comp	576 | activation	576 | 
| 10	| conv4	| InnerProduct	| 	64	| 3x3	| 128	| 1x1 | macc	73.73k | activation	128<br>param	73.86k | 
| 11	| prelu4	| PReLU	| 	128	| 1x1	| 128	| 1x1	| comp	128 | activation	128 | 
| 12	| conv5-2	| InnerProduct	| 	128	| 1x1	| 4	| 1x1 | macc	512 | activation	4<br>param	516 | 
| 13	| conv5-1	| InnerProduct	| 	128	| 1x1	| 2	| 1x1 | macc	256 | activation	2<br>param	258 | 
| 14	| prob1 | 	Softmax	 | 	2	| 1x1	| 2	| 1x1 | 	add	2<br>div	2<br>exp	2 | activation	2 | 
| TOTAL | | | | | | | macc	1.53M<br>comp	55.55k<br>add	2<br>div	2<br>exp	2 | activation	42.18k<br>param	99.91k | 


* Output Net (O-Net)

| ID | Name | Type | Input CH | Input DIM | Output CH | Output DIM | OPS | Mem |
| -- | :--- | :--- | :--- | :--- | :--- |:--- | :--- | :--- | 
| 1	 | data	| data		| 3	| 48x48	| 3	| 48x48 | activation	6.91k | 
| 2	| conv1	| Convolution	| 3	| 48x48	| 32	| 46x46 | macc	1.83M | activation	67.71k<br>param	896 | 
| 3	| relu1	| PReLU	| 32	| 46x46	| 32	| 46x46 | comp	67.71k | activation	67.71k | 
| 4	| pool1	| Pooling	| 32 | 46x46	| 32	| 23x23 | comp	152.35k | activation	16.93k | 
| 5	| conv2	| Convolution	| 	32	| 23x23	| 64	| 21x21 | macc	8.13M | activation	28.22k<br>param	18.5k | 
| 6	| relu2	| PReLU	| 	64	| 21x21	| 64	| 21x21	| comp	28.22k | activation	28.22k | 
| 7	| pool2	| Pooling	| 64	| 21x21	| 64	| 10x10	| comp	57.6k | activation	6.4k
| 8	| conv3	| Convolution	| 64	| 10x10	| 64	| 8x8	| macc	2.36M | activation	4.1k<br>param	36.93k | 
| 9	| relu3	| PReLU	| 	64	| 8x8	| 64	| 8x8 | comp	4.1k | activation	4.1k | 
| 10	| pool3	| Pooling		| 64	| 8x8	| 64	| 4x4	| comp	4.1k | activation	1.02k | 
| 11	| conv4	| Convolution	| 	64	| 4x4	| 128	| 3x3	| macc	294.91k | activation	1.15k<br>param	32.9k | 
| 12	| relu4	| PReLU	| 128	| 3x3	| 128	| 3x3	| comp	1.15k | activation	1.15k | 
| 13	| fc5	| InnerProduct | 128	| 3x3	| 256	| 1x1	| macc	294.91k | activation	256<br>param	295.17k | 
| 14	| relu5	| PReLU	| 	256	| 1x1	| 256	| 1x1 | comp	256 | activation	256 | 
| 15	| drop5	| Dropout	| 	256	| 1x1	| 256	| 1x1	| comp	256 | activation	256 | 
| 16	| fc6-3	| InnerProduct	| 	256	| 1x1	| 10	| 1x1 | macc	2.56k | activation	10<br>param	2.57k | 
| 17	| fc6-2	| InnerProduct	| 	256	| 1x1	| 4	| 1x1 | macc	1.02k | activation	4 | param	1.03k | 
| 18	| fc6-1	| InnerProduct	| 	256	| 1x1	| 2	| 1x1 | macc	512 | activation	2 | param	514 | 
| 19	| prob1	| Softmax		| 2	| 1x1	| 2	| 1x1 | add	2<br>div	2<br>exp	2 | activation	2 | 
| TOTAL | | | | | | | macc	12.91M<br>comp	315.74k<br>add	2<br>div	2<br>exp	2 | activation	234.42k<br>param	388.5k | 
