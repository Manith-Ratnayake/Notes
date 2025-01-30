A traditional debugger allows you to inspect the system state once the system is halted
To understand why an event took place, the relavent context has to be restored. This requires tracing 


Tracing is the process of collecting information on the activity in a working system
With tracing, program execute is recorded during run-time, allowing for later analysis of the trace


Tracing provides developers with information useful for debugging
Difference between tracing and logging


jus like logs, tracing data can be read as it
With tracing, information is written about low level-events
These numbers in the hundreds or even thousands


With logging information is written about higher-level events, which are much less frequent.
These includes users logging into the system, application errors database transaction etc

------------------------------------------------------------------------------
ftrace

official tracer in linux kernal. Function call trace
Functional tracer
ex : write a device kernal, debug it, confirm that everything fine 


CONFIG_FTRACE
CONFIG_FUNCTION_TRACER
CONFIG_FUNCTION_GRAPH_TRACER
CONFIG_STACK_TRACER

cat /boot/config-`uname-r` | grep CONFIG_FTRACE
ls /sys/kernel/tracing
cd /sys/kernel/debug 
tracefs   
mount -t tracefs nodev /sys/kernel/tracing

----------------------------------------------------------------------

All manipulations are done with simple operation (echo/cat) in tracefs
ftrace is built around smart lockless ring buffer implementation
This buffer stores all the tracing information and is exposed as a file in tracefs 

available_tracers

nop             - No actions 
functions       - Trace kernel functions entry
functions_graph - Trace kernel functions entry and exit thus allowing to build a call graph
blk             - Block tracer/blktrace
nmiotrace       - Trace interactions between drivers and hardware

Default tracer is nop

---------------------------------------------------------------------------

current_tracer

Enabling a tracer 

ex: cat available_tracers
    echo 'functions' > current_tracer
    cat trace | head -n 20


cat /proc/uptime 

------------------------------------------------------------------------------

Function graph tracer

Function graph tracer is built on top of function tracer.
It also records the return address. By this when a function enters and function exit 
    
Functio_graph tracer 
    - tracks the entry of the function
    - tracks the exit of the function
    - Execution Time 
    - CPU on which it is running 

echo functions_graph > current_tracer 


functions starts with '{' and ends with '}' 
functions do not call othe functions are denoted ';' also known as leaf functions 

time > 10 microseconds      '+'
time > 100 microseconds     '-'
time > 1000 microseconds    '#'
time > 10 milliseconds      '*'
time > 100 milliseconds     '@'
time > 1 second             '$'

cat trace | grep -F '$'

-------------------------------------------------------------

Functions Filtering 


ftace printout can be big, finding exactly what it is you're looking for can be extremely difficult.
filters - only functions we are interested in 

what functions are available for filter -> All the functions in available_filter_functions 


Limiting functions tracing 
    set_ftrace_filter - Only trace these functions
    set_ftrace_notrace - Do not trace these functions

echo function_name > set_ftrace_filter
cat available_filter_functions | grep kmalloc 

______________________________________________________________________


1. what happen if there are two functions with same function name
It will enable both of them 


2. Does available_filter_functions file show only exported symbols or all kernel symbols?
Every function which is present in callsystem, which is basically every single function 


______________________________________________________________________

Starting and stopping the trace 

tracing_on is used to disable the ring buffer writeable or not 
The ring buffer is not recording and will not attempt to write any data, but the calls the tracers make are still perform
To re-enable the ring buffer, simply write '1' into that file








