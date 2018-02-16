

1	data	data		3	224x224	3	224x224		
activation	150.53k
2	conv1	Convolution		3	224x224	64	112x112	
macc	118.01M
activation	802.82k
param	9.47k
3	bn_conv1	BatchNorm		64	112x112	64	112x112	
add	802.82k
div	802.82k
activation	802.82k
param	128
4	scale_conv1	Scale		64	112x112	64	112x112	
macc	802.82k
activation	802.82k
5	conv1_relu	ReLU		64	112x112	64	112x112	
comp	802.82k
activation	802.82k
6	pool1	Pooling		64	112x112	64	56x56	
comp	1.81M
activation	200.7k
7	res2a_branch2a	Convolution		64	56x56	64	56x56	
macc	12.85M
activation	200.7k
param	4.1k
8	bn2a_branch2a	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
9	scale2a_branch2a	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
10	res2a_branch2a_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
11	res2a_branch2b	Convolution		64	56x56	64	56x56	
macc	115.61M
activation	200.7k
param	36.86k
12	bn2a_branch2b	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
13	scale2a_branch2b	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
14	res2a_branch2b_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
15	res2a_branch2c	Convolution		64	56x56	256	56x56	
macc	51.38M
activation	802.82k
param	16.38k
16	bn2a_branch2c	BatchNorm		256	56x56	256	56x56	
add	802.82k
div	802.82k
activation	802.82k
param	512
17	scale2a_branch2c	Scale		256	56x56	256	56x56	
macc	802.82k
activation	802.82k
18	res2a_branch1	Convolution		64	56x56	256	56x56	
macc	51.38M
activation	802.82k
param	16.38k
19	bn2a_branch1	BatchNorm		256	56x56	256	56x56	
add	802.82k
div	802.82k
activation	802.82k
param	512
20	scale2a_branch1	Scale		256	56x56	256	56x56	
macc	802.82k
activation	802.82k
21	res2a	Eltwise		256	56x56	256	56x56	
add	802.82k
activation	802.82k
22	res2a_relu	ReLU		256	56x56	256	56x56	
comp	802.82k
activation	802.82k
23	res2b_branch2a	Convolution		256	56x56	64	56x56	
macc	51.38M
activation	200.7k
param	16.38k
24	bn2b_branch2a	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
25	scale2b_branch2a	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
26	res2b_branch2a_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
27	res2b_branch2b	Convolution		64	56x56	64	56x56	
macc	115.61M
activation	200.7k
param	36.86k
28	bn2b_branch2b	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
29	scale2b_branch2b	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
30	res2b_branch2b_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
31	res2b_branch2c	Convolution		64	56x56	256	56x56	
macc	51.38M
activation	802.82k
param	16.38k
32	bn2b_branch2c	BatchNorm		256	56x56	256	56x56	
add	802.82k
div	802.82k
activation	802.82k
param	512
33	scale2b_branch2c	Scale		256	56x56	256	56x56	
macc	802.82k
activation	802.82k
34	res2b	Eltwise		256	56x56	256	56x56	
add	802.82k
activation	802.82k
35	res2b_relu	ReLU		256	56x56	256	56x56	
comp	802.82k
activation	802.82k
36	res2c_branch2a	Convolution		256	56x56	64	56x56	
macc	51.38M
activation	200.7k
param	16.38k
37	bn2c_branch2a	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
38	scale2c_branch2a	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
39	res2c_branch2a_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
40	res2c_branch2b	Convolution		64	56x56	64	56x56	
macc	115.61M
activation	200.7k
param	36.86k
41	bn2c_branch2b	BatchNorm		64	56x56	64	56x56	
add	200.7k
div	200.7k
activation	200.7k
param	128
42	scale2c_branch2b	Scale		64	56x56	64	56x56	
macc	200.7k
activation	200.7k
43	res2c_branch2b_relu	ReLU		64	56x56	64	56x56	
comp	200.7k
activation	200.7k
44	res2c_branch2c	Convolution		64	56x56	256	56x56	
macc	51.38M
activation	802.82k
param	16.38k
45	bn2c_branch2c	BatchNorm		256	56x56	256	56x56	
add	802.82k
div	802.82k
activation	802.82k
param	512
46	scale2c_branch2c	Scale		256	56x56	256	56x56	
macc	802.82k
activation	802.82k
47	res2c	Eltwise		256	56x56	256	56x56	
add	802.82k
activation	802.82k
48	res2c_relu	ReLU		256	56x56	256	56x56	
comp	802.82k
activation	802.82k
49	res3a_branch2a	Convolution		256	56x56	128	28x28	
macc	25.69M
activation	100.35k
param	32.77k
50	bn3a_branch2a	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
51	scale3a_branch2a	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
52	res3a_branch2a_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
53	res3a_branch2b	Convolution		128	28x28	128	28x28	
macc	115.61M
activation	100.35k
param	147.46k
54	bn3a_branch2b	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
55	scale3a_branch2b	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
56	res3a_branch2b_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
57	res3a_branch2c	Convolution		128	28x28	512	28x28	
macc	51.38M
activation	401.41k
param	65.54k
58	bn3a_branch2c	BatchNorm		512	28x28	512	28x28	
add	401.41k
div	401.41k
activation	401.41k
param	1.02k
59	scale3a_branch2c	Scale		512	28x28	512	28x28	
macc	401.41k
activation	401.41k
60	res3a_branch1	Convolution		256	56x56	512	28x28	
macc	102.76M
activation	401.41k
param	131.07k
61	bn3a_branch1	BatchNorm		512	28x28	512	28x28	
add	401.41k
div	401.41k
activation	401.41k
param	1.02k
62	scale3a_branch1	Scale		512	28x28	512	28x28	
macc	401.41k
activation	401.41k
63	res3a	Eltwise		512	28x28	512	28x28	
add	401.41k
activation	401.41k
64	res3a_relu	ReLU		512	28x28	512	28x28	
comp	401.41k
activation	401.41k
65	res3b_branch2a	Convolution		512	28x28	128	28x28	
macc	51.38M
activation	100.35k
param	65.54k
66	bn3b_branch2a	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
67	scale3b_branch2a	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
68	res3b_branch2a_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
69	res3b_branch2b	Convolution		128	28x28	128	28x28	
macc	115.61M
activation	100.35k
param	147.46k
70	bn3b_branch2b	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
71	scale3b_branch2b	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
72	res3b_branch2b_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
73	res3b_branch2c	Convolution		128	28x28	512	28x28	
macc	51.38M
activation	401.41k
param	65.54k
74	bn3b_branch2c	BatchNorm		512	28x28	512	28x28	
add	401.41k
div	401.41k
activation	401.41k
param	1.02k
75	scale3b_branch2c	Scale		512	28x28	512	28x28	
macc	401.41k
activation	401.41k
76	res3b	Eltwise		512	28x28	512	28x28	
add	401.41k
activation	401.41k
77	res3b_relu	ReLU		512	28x28	512	28x28	
comp	401.41k
activation	401.41k
78	res3c_branch2a	Convolution		512	28x28	128	28x28	
macc	51.38M
activation	100.35k
param	65.54k
79	bn3c_branch2a	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
80	scale3c_branch2a	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
81	res3c_branch2a_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
82	res3c_branch2b	Convolution		128	28x28	128	28x28	
macc	115.61M
activation	100.35k
param	147.46k
83	bn3c_branch2b	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
84	scale3c_branch2b	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
85	res3c_branch2b_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
86	res3c_branch2c	Convolution		128	28x28	512	28x28	
macc	51.38M
activation	401.41k
param	65.54k
87	bn3c_branch2c	BatchNorm		512	28x28	512	28x28	
add	401.41k
div	401.41k
activation	401.41k
param	1.02k
88	scale3c_branch2c	Scale		512	28x28	512	28x28	
macc	401.41k
activation	401.41k
89	res3c	Eltwise		512	28x28	512	28x28	
add	401.41k
activation	401.41k
90	res3c_relu	ReLU		512	28x28	512	28x28	
comp	401.41k
activation	401.41k
91	res3d_branch2a	Convolution		512	28x28	128	28x28	
macc	51.38M
activation	100.35k
param	65.54k
92	bn3d_branch2a	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
93	scale3d_branch2a	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
94	res3d_branch2a_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
95	res3d_branch2b	Convolution		128	28x28	128	28x28	
macc	115.61M
activation	100.35k
param	147.46k
96	bn3d_branch2b	BatchNorm		128	28x28	128	28x28	
add	100.35k
div	100.35k
activation	100.35k
param	256
97	scale3d_branch2b	Scale		128	28x28	128	28x28	
macc	100.35k
activation	100.35k
98	res3d_branch2b_relu	ReLU		128	28x28	128	28x28	
comp	100.35k
activation	100.35k
99	res3d_branch2c	Convolution		128	28x28	512	28x28	
macc	51.38M
activation	401.41k
param	65.54k
100	bn3d_branch2c	BatchNorm		512	28x28	512	28x28	
add	401.41k
div	401.41k
activation	401.41k
param	1.02k
101	scale3d_branch2c	Scale		512	28x28	512	28x28	
macc	401.41k
activation	401.41k
102	res3d	Eltwise		512	28x28	512	28x28	
add	401.41k
activation	401.41k
103	res3d_relu	ReLU		512	28x28	512	28x28	
comp	401.41k
activation	401.41k
104	res4a_branch2a	Convolution		512	28x28	256	14x14	
macc	25.69M
activation	50.18k
param	131.07k
105	bn4a_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
106	scale4a_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
107	res4a_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
108	res4a_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
109	bn4a_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
110	scale4a_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
111	res4a_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
112	res4a_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
113	bn4a_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
114	scale4a_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
115	res4a_branch1	Convolution		512	28x28	1024	14x14	
macc	102.76M
activation	200.7k
param	524.29k
116	bn4a_branch1	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
117	scale4a_branch1	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
118	res4a	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
119	res4a_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
120	res4b_branch2a	Convolution		1024	14x14	256	14x14	
macc	51.38M
activation	50.18k
param	262.14k
121	bn4b_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
122	scale4b_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
123	res4b_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
124	res4b_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
125	bn4b_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
126	scale4b_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
127	res4b_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
128	res4b_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
129	bn4b_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
130	scale4b_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
131	res4b	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
132	res4b_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
133	res4c_branch2a	Convolution		1024	14x14	256	14x14	
macc	51.38M
activation	50.18k
param	262.14k
134	bn4c_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
135	scale4c_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
136	res4c_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
137	res4c_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
138	bn4c_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
139	scale4c_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
140	res4c_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
141	res4c_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
142	bn4c_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
143	scale4c_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
144	res4c	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
145	res4c_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
146	res4d_branch2a	Convolution		1024	14x14	256	14x14	
macc	51.38M
activation	50.18k
param	262.14k
147	bn4d_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
148	scale4d_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
149	res4d_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
150	res4d_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
151	bn4d_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
152	scale4d_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
153	res4d_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
154	res4d_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
155	bn4d_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
156	scale4d_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
157	res4d	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
158	res4d_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
159	res4e_branch2a	Convolution		1024	14x14	256	14x14	
macc	51.38M
activation	50.18k
param	262.14k
160	bn4e_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
161	scale4e_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
162	res4e_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
163	res4e_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
164	bn4e_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
165	scale4e_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
166	res4e_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
167	res4e_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
168	bn4e_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
169	scale4e_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
170	res4e	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
171	res4e_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
172	res4f_branch2a	Convolution		1024	14x14	256	14x14	
macc	51.38M
activation	50.18k
param	262.14k
173	bn4f_branch2a	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
174	scale4f_branch2a	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
175	res4f_branch2a_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
176	res4f_branch2b	Convolution		256	14x14	256	14x14	
macc	115.61M
activation	50.18k
param	589.82k
177	bn4f_branch2b	BatchNorm		256	14x14	256	14x14	
add	50.18k
div	50.18k
activation	50.18k
param	512
178	scale4f_branch2b	Scale		256	14x14	256	14x14	
macc	50.18k
activation	50.18k
179	res4f_branch2b_relu	ReLU		256	14x14	256	14x14	
comp	50.18k
activation	50.18k
180	res4f_branch2c	Convolution		256	14x14	1024	14x14	
macc	51.38M
activation	200.7k
param	262.14k
181	bn4f_branch2c	BatchNorm		1024	14x14	1024	14x14	
add	200.7k
div	200.7k
activation	200.7k
param	2.05k
182	scale4f_branch2c	Scale		1024	14x14	1024	14x14	
macc	200.7k
activation	200.7k
183	res4f	Eltwise		1024	14x14	1024	14x14	
add	200.7k
activation	200.7k
184	res4f_relu	ReLU		1024	14x14	1024	14x14	
comp	200.7k
activation	200.7k
185	res5a_branch2a	Convolution		1024	14x14	512	7x7	
macc	25.69M
activation	25.09k
param	524.29k
186	bn5a_branch2a	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
187	scale5a_branch2a	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
188	res5a_branch2a_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
189	res5a_branch2b	Convolution		512	7x7	512	7x7	
macc	115.61M
activation	25.09k
param	2.36M
190	bn5a_branch2b	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
191	scale5a_branch2b	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
192	res5a_branch2b_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
193	res5a_branch2c	Convolution		512	7x7	2048	7x7	
macc	51.38M
activation	100.35k
param	1.05M
194	bn5a_branch2c	BatchNorm		2048	7x7	2048	7x7	
add	100.35k
div	100.35k
activation	100.35k
param	4.1k
195	scale5a_branch2c	Scale		2048	7x7	2048	7x7	
macc	100.35k
activation	100.35k
196	res5a_branch1	Convolution		1024	14x14	2048	7x7	
macc	102.76M
activation	100.35k
param	2.1M
197	bn5a_branch1	BatchNorm		2048	7x7	2048	7x7	
add	100.35k
div	100.35k
activation	100.35k
param	4.1k
198	scale5a_branch1	Scale		2048	7x7	2048	7x7	
macc	100.35k
activation	100.35k
199	res5a	Eltwise		2048	7x7	2048	7x7	
add	100.35k
activation	100.35k
200	res5a_relu	ReLU		2048	7x7	2048	7x7	
comp	100.35k
activation	100.35k
201	res5b_branch2a	Convolution		2048	7x7	512	7x7	
macc	51.38M
activation	25.09k
param	1.05M
202	bn5b_branch2a	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
203	scale5b_branch2a	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
204	res5b_branch2a_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
205	res5b_branch2b	Convolution		512	7x7	512	7x7	
macc	115.61M
activation	25.09k
param	2.36M
206	bn5b_branch2b	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
207	scale5b_branch2b	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
208	res5b_branch2b_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
209	res5b_branch2c	Convolution		512	7x7	2048	7x7	
macc	51.38M
activation	100.35k
param	1.05M
210	bn5b_branch2c	BatchNorm		2048	7x7	2048	7x7	
add	100.35k
div	100.35k
activation	100.35k
param	4.1k
211	scale5b_branch2c	Scale		2048	7x7	2048	7x7	
macc	100.35k
activation	100.35k
212	res5b	Eltwise		2048	7x7	2048	7x7	
add	100.35k
activation	100.35k
213	res5b_relu	ReLU		2048	7x7	2048	7x7	
comp	100.35k
activation	100.35k
214	res5c_branch2a	Convolution		2048	7x7	512	7x7	
macc	51.38M
activation	25.09k
param	1.05M
215	bn5c_branch2a	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
216	scale5c_branch2a	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
217	res5c_branch2a_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
218	res5c_branch2b	Convolution		512	7x7	512	7x7	
macc	115.61M
activation	25.09k
param	2.36M
219	bn5c_branch2b	BatchNorm		512	7x7	512	7x7	
add	25.09k
div	25.09k
activation	25.09k
param	1.02k
220	scale5c_branch2b	Scale		512	7x7	512	7x7	
macc	25.09k
activation	25.09k
221	res5c_branch2b_relu	ReLU		512	7x7	512	7x7	
comp	25.09k
activation	25.09k
222	res5c_branch2c	Convolution		512	7x7	2048	7x7	
macc	51.38M
activation	100.35k
param	1.05M
223	bn5c_branch2c	BatchNorm		2048	7x7	2048	7x7	
add	100.35k
div	100.35k
activation	100.35k
param	4.1k
224	scale5c_branch2c	Scale		2048	7x7	2048	7x7	
macc	100.35k
activation	100.35k
225	res5c	Eltwise		2048	7x7	2048	7x7	
add	100.35k
activation	100.35k
226	res5c_relu	ReLU		2048	7x7	2048	7x7	
comp	100.35k
activation	100.35k
227	pool5	Pooling		2048	7x7	2048	1x1	
add	100.35k
activation	2.05k
228	fc1000	InnerProduct		2048	1x1	1000	1x1	
macc	2.05M
activation	1000
param	2.05M
229	prob	Softmax		1000	1x1	1000	1x1	
add	1000
div	1000
exp	1000
activation	1000
TOTAL							
macc	3.87G
comp	10.89M
add	16.21M
div	10.59M
exp	1000
activation	46.72M
param	25.56M
