Nagios allows you to monitor the servers and check if they are being sufficiently utilized or if there are any task failures that need to be addressed

Nagios Remote plugin Executor (NPRE) allows you to execute Nagios pluging on Linux machines. You can monitor remote machines metrics

NPRE
    : check_npre   
    : NPRE dameon 


Nagios use port numbers 5666/7/8

Monitoring host on 2 ways 

Actively 
    : Checks are intiated by nagios process == check logic by nagios dameon
    : Checks are run on a regular scheduled basis

Passively
    : Checks are initiated and performed by external application/proccess
    : Checks results are submitted to nagios for processing


