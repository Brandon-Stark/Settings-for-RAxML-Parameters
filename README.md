# Settings-for-RAxML-Parameters
# 设置RAxML允许参数的一般方法

In general you should try to compile the SSE3 version that makes use of capabilities 
on relativiely recent processors (most Intel or AMD chips not older than 3-4 years).
The SSE3 version will run about 40% faster than the non-SSE3 version.

For example, the SSE3 version was called as follows:

**./raxmlHPC-HYBRID-SSE3 -T 10 -f a -s env_roka_controls_aligned.phyx -n bootenv -m GTRCAT -p 12345 -x 12345 -#1000**

##### Note
The explaination for `-T` is as following:
PTHREADS VERSION ONLY! Specify the number of threads you want to run.
Make sure to set "T" to at most the number of CPUs you have on your
machine, otherwise, there will be a huge performance decrease!

If you have a more recently bought processor (within the last 1-2 years), please 
also try to compile the AVX version which once again uses the capabilities of modern
processors better and can be 10-30% faster than the SSE3 version. AVX will work on 
the Intel i7 (sandy-bridge) series processors as well as on the very recently 
released AMD Bulldozer systems.

For example, the AVX version was called as follows:

**./raxmlHPC-AVX -f a -s env_roka_controls_aligned.phyx -n bootenv -m GTRCAT -p 12345 -x 12345 -#1000**
