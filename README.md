3.1.1  修改src/c/pyeclib_c/pyeclib_c.h源码
在该文件中只需要修改一处的源码，即将第35行代码中的“int ec_desc;”修改为“int64_t ec_desc;”。
3.1.2  修改src/c/pyeclib_c/pyeclib_c.c源码
在该文件中涉及到40处源码的修改，具体修改如下：
1）将第68行代码中的“(Py_ssize_t)objlen”修改为“(int64_t)objlen”。
2）将第75行代码中的“uint64_t offset;”修改为“int64_t offset;”。
3）将第76行代码中的“uint64_t length;”修改为“int64_t length;”。
4）将第109行代码中的“void * alloc_and_set_buffer(int size, int value)”修改为“void * alloc_and_set_buffer(int64_t size, int64_t value)”。
5）将第126行代码中的“void * alloc_zeroed_buffer(int size)”修改为“void *alloc_zeroed_buffer(int64_t size)”。
6）将第362行代码中的“int data_len;”修改为“int64_t data_len;”。
7）将第363行代码中的“int segment_size, last_segment_size;”修改为“int64_t segment_size, last_segment_size;”。
8）将第365行代码中的“int fragment_size, last_fragment_size;”修改为“int64_t fragment_size, last_fragment_size;”。
9）将第366行代码中的“int min_segment_size;”修改为“int64_t min_segment_size;”。
10）将第497行代码中的“Py_ssize_t data_len;”修改为“int64_t data_len;”。
11）将第498行代码中的“uint64_t fragment_len;”修改为“int64_t fragment_len;”。
12）将第561行代码中的“int *c_reconstruct_list = NULL;”修改为“int64_t *c_reconstruct_list = NULL;”。
13）将第562行代码中的“int *c_exclude_list = NULL;”修改为“int64_t *c_exclude_list = NULL;”。
14）将第563行代码中的“int num_missing;”修改为“int64_t num_missing;”。
15）将第564行代码中的“int num_exclude;”修改为“int64_t num_exclude;”。
16）将第584行代码中的“(int) PyList_Size”修改为“(int64_t) PyList_Size”。
17）将第585行代码中的“(int *) alloc_zeroed_buffer((num_missing+1) * sizeof(int));”修改为“(int64_t *) alloc_zeroed_buffer((num_missing+1) * sizeof(int64_t));”。
18）将第593行代码中的“long idx = PyLong_AsLong(obj_idx);”修改为“int64_t idx = PyLong_AsLong(obj_idx);”。
19）将第594行代码中的“c_reconstruct_list[i] = (int) idx;”修改为“c_reconstruct_list[i] = (int64_t) idx;”。
20）将第597行代码中的“num_exclude = (int) PyList_Size(exclude_list);”修改为“num_exclude = (int64_t) PyList_Size(exclude_list);”。
21）将第598行代码中的“c_exclude_list = (int *) alloc_zeroed_buffer((num_exclude + 1) * sizeof(int));”修改为“c_exclude_list = (int64_t *) alloc_zeroed_buffer((num_exclude + 1) * sizeof(int64_t));”。
22）将第606行代码中的“long idx = PyLong_AsLong(obj_idx);”修改为“int64_t idx = PyLong_AsLong(obj_idx);”。
23）将第607行代码中的“c_exclude_list[i] = (int) idx;”修改为“c_exclude_list[i] = (int64_t) idx;”。
24）将第665行代码中的“int fragment_len;”修改为“int64_t fragment_len;”。
25）将第707行代码中的“Py_ssize_t len = 0;”修改为“int64_t len = 0;”。
26）将第757行代码中的“int fragment_len;”修改为“ int64_t fragment_len;”。
27）将第761行代码中的“uint64_t range_payload_size = 0;”修改为“int64_t range_payload_size = 0;”。
28）将第762行代码中的“uint64_t orig_data_size =0;”修改为“int64_t orig_data_size =0;”。
29）将第816行代码中的“long begin, end;”修改为“int64_t begin, end;”。
30）将第858行代码中的“Pyssize_t len = 0;”修改为“int64_t len = 0;”。
31）将第989行代码中的“hex_encode_string(char *buf, uint32_t buf_len)”修改为“hex_encode_string(char *buf, int64_t buf_len)”。
32）将第993行代码中的“uint32_t i;”修改为“int64_t i;”。
33）将第1045行代码中的“Py_ssize_t fragment_len;”修改为“int64_t fragment_len;”。
34）将第1046行代码中的“int formatted;”修改为“int64_t formatted;”。
35）将第1047行代码中的“int ret;”修改为“int64_t ret;”。
36）将第1097行代码中的“int num_fragments;”修改为“int64_t num_fragments;”
37）将第1099行代码中的“int size;”修改为“int64_t size;”。
38）将第1134行代码中的“Py_ssize_t len = 0;”修改为“ int64_t len = 0;”。
39）将第1193行代码中的“uint32_t (*hGetVersion)(void);”修改为“int64_t (*hGetVersion)(void);”。
40）将第1214行代码中的“uint32_t version = (*hGetVersion)();”修改为“int64_t version = (*hGetVersion)();”。

